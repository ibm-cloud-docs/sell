---

copyright:

  years: 2022

lastupdated: "2022-06-02"

keywords: client ID, authentication flow, OAuth, authentication

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Developing an authentication flow for your service
{: #develop-auth}

When you onboard your product to {{site.data.keyword.cloud}} Partner Center, you can develop an authentication flow as a way to identify and validate customers when they use your services. To develop an authentication flow, you need a client ID and a secret.
{: shortdesc}

## Configuring your client ID and secret
{: #configure-client-id}

To develop an authentication flow, you need a client ID and a secret, and a redirect URL. The client ID is generated to identify your service, along with the secret, which is the password for your service. Your client ID is not confidential since it is publicly identified. However, the secret is confidential and is only known to the application and the authorization server. You can create and manage you client ID in Partner Center. A redirect URL is the host URL for your service that users are redirected to after a successful authentication. 

The following example shows redirect URLs:

```text
https://<myapp>.cloud.ibm.com/integrate/auth/callback
http://localhost:3000/auth/callback <-- for testing locally
```

To generate your client ID, complete the following steps:

1. Go to **Partner Center** > **Sell** > **My products**.
1. Select the product that you're onboarding, and go to the **Brokers** tab. 
1. Click **Set up IBM Cloud SSO**.
1. Add owners who can manage the client ID.

    Only owners are able to view, edit and delete the client ID setup, or add extra redirect URLs. Users who create the client ID are automatically added to the owners list, and not able to remove themselves.
    {: note}

1. Add the redirect URL, and click **Next**. You can add more than one URL and use these as the `redirect_uri` in the upcoming tasks. The `redirect_uri` value refers to the redirect URL.
1. Save your credentials. Copy the password for your service that is generated along with the client ID. You are not able to retrieve your password later.

    If you don't have your password, you can delete and re-create your previously created client ID to generate another one. 
    {: note}

1. Click **Done**.

## Developing your OAuth flow for authentication
{: #develop-oauth}

After you successfully generated your client ID in the previous task, you can start to develop your oAuth flow. 

### Authentication - Step 0
{: #auth-step0}

Find IAM regional endpoint for UI login that is closer to your deployed application by calling the following endpoint:

`https://iam.cloud.ibm.com/identity/.well-known/openid-configuration`

See the following curl command as an example: 

```bash
curl -X GET \
  https://iam.cloud.ibm.com/identity/.well-known/openid-configuration
```

```text
HTTP/1.1 200 OK
Content-Type: application/json
{
  "issuer": "https://iam.cloud.ibm.com/identity",
  "authorization_endpoint": "https://iam-region2.cloud.ibm.com/identity/authorize",
  "token_endpoint": "https://iam-region2.cloud.ibm.com/identity/token",
...
}
```

This request can be done when the application starts, and again if the `authorization_endpoint` fails. You can cache the `authorization_endpoint` value for a short amount of time, and refresh after the cache expires or an error occurs.

### Authentication - Step 1
{: #auth-step1}

When users navigate to your `dashboard_url`, redirect the browser to the following URL to check if they are logged in to your application and have the identity token: 

`<authorization_endpoint>?client_id=<your-client-id>&redirect_uri=<your-redirect-uri>&response-type=code&state=<your-resource-instance-id>`

The `redirect_uri` value refers to the redirect URL that you set up in the [Configure your client ID](#configure-client-id) task.
{: note}

* If a user is logged in, they are immediately redirected. The browser does a callback to redirect the URI with a `code` response parameter and `state` value. 

* If a user is not logged in, a login prompt appears. After a successful login, the browser does a callback to redirect the URI with a `code` response parameter and `state` value.


### Authentication - Step 2
{: #auth-step2}

After the user successfully logged in, exchange the code that you received in Authentication - Step 1 for the identity token of the user.

## Calling the identity token endpoint
{: #post-token}

### POST <token_endpoint>
{: #token-endpoint}

To obtain an identity token, you must include the following headers and parameters:

#### Headers:
{: #header}

- Authorization: Basic *[client id]:[client secret]*
- Content-Type: application/x-www-form-urlencoded
- Accept: application/json

#### Parameters:
{: #parameter}

- client_id=*[client ID]*
- client_secret=*[client secret]*
- grant_type=authorization_code
- response_type=cloud_iam
- redirect_uri=*[this parameter refers to the same URL from Step 1]*
- code=*[code from callback]*

See the required headers and parameters included in the following POST request example:

```bash
curl -k -X POST \
  -u "<your-client-id>:<your-client-secret>" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -H "Accept: application/json" \
  --data-urlencode "client_id=<your-client-id>" \
  --data-urlencode "client_secret=<your-client-secret>" \
  --data-urlencode "grant_type=authorization_code" \
  --data-urlencode "response_type=cloud_iam" \
  --data-urlencode "code=<code-from-the-callback>" \
  --data-urlencode "redirect_uri=<redirect_uri>" \
  "https://iam-region2.cloud.ibm.com/identity/token"
```
{: codeblock}

### Identity token response
{: #access-response}

After you submit a POST request in the previous task, you receive a response with the identity token.

See the following example of a successful identity token response:

```text
{
  "access_token": "eyJraWQiOiI......XmpBTIDdR5w",
  "refresh_token": "SPrXw5tBE3......KBQ+luWQVY=",
  "token_type": "Bearer",
  "expires_in": 3600,
  "expiration": 1473188353
}
```
{: codeblock}


## IAM token scoping for third-party service providers
{: #iam-token-scope}

User identity tokens that are created with your client ID can be used to access only your service APIs. Requests to other {{site.data.keyword.cloud_notm}} APIs that use this token are denied access, even if the user has an appropriate policy configured.

As part of third-party integration, token scoping is being used to ensure that tokens have the minimal access scope that is needed to accomplish the user's goals. To facilitate this, IAM tokens access is based on the client ID that created the token. If an IAM token was created by a third-party service, a user can't run certain APIs and functions, even if the user has an appropriate policy configured.
