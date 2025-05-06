---

copyright:
  years: 2021, 2025

lastupdated: "2025-05-06"

keywords: third-party, sell on IBM Cloud, partner center, service, broker, pricing plan, regions, location

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 10m

---

{{site.data.keyword.attribute-definition-list}}


# Onboard a broker
{: #broker-onboard}
{: toc-content-type="tutorial"}
{: toc-completion-time="10m"}

This tutorial walks you through how to onboard a broker that you can use to connect a pricing plan to your third-party service. When users create instances of your service from the {{site.data.keyword.cloud}} catalog, the broker manages the lifecycle of those instances, and connects the service to the applications that developers are building.
{: shortdesc}

This tutorial is one of five in a series that demonstrates how to onboard and publish a third-party service to {{site.data.keyword.cloud_notm}}. As you complete the tutorial, adjust each step to fit your product's needs.

## Before you begin
{: #broker-onboard-prereqs}

Before you can start onboarding your broker, complete the following step:

* For an example of how to build your broker, see the [Open Service Broker reference application](https://github.com/IBM/onboarding-osb-node){: external} and the [{{site.data.keyword.cloud_notm}} Open Service Broker API](/apidocs/resource-controller/ibm-cloud-osb-api).

## Authentication schemes for brokers
{: #authentication-scheme-broker}

When you add a broker in Partner Center, you can select from the following three authentication schemes to verify the identity of the client that interacts with the broker:

Bearer CRN
:    In this method, the resource controller generates an IAM token using the cloud resource name (CRN) of the broker it is connecting to. This token includes the broker’s CRN as the identity in the JWT. When the token is used to call a service, the service’s broker application authorizes the request by verifying that the caller’s identity matches the expected broker CRN. This method does not require an API key or API key rotation. The IAM token must be verified by the broker before authorizing the request. The keyset used for verification is available at [https://iam.cloud.ibm.com/identity/keys](https://iam.cloud.ibm.com/identity/keys){: external}. See the following example for a CRN token:

```json
{
  "iam_id": "crn-crn:v1:bluemix:public:resource-controller::a/f71446b6474d45bf81196da45de13940::resource-broker:1f4a9711-e359-4e00-8ad3-c8bfd38446b3",
  "id": "crn-crn:v1:bluemix:public:resource-controller::a/f71446b6474d45bf81196da45de13940::resource-broker:1f4a9711-e359-4e00-8ad3-c8bfd38446b3",
  "realmid": "crn",
  "jti": "86912b78-4b25-482e-9876-665f6cf97978",
  "identifier": "crn:v1:bluemix:public:resource-controller::a/f71446b6474d45bf81196da45de13940::resource-broker:1f4a9711-e359-4e00-8ad3-c8bfd38446b3",
  "sub": "crn:v1:bluemix:public:resource-controller::a/f71446b6474d45bf81196da45de13940::resource-broker:1f4a9711-e359-4e00-8ad3-c8bfd38446b3",
  "sub_type": "CRN",
  "authn": {
    "sub": "crn:v1:bluemix:public:resource-controller::a/f71446b6474d45bf81196da45de13940::resource-broker:1f4a9711-e359-4e00-8ad3-c8bfd38446b3",
    "iam_id": "crn-crn:v1:bluemix:public:resource-controller::a/f71446b6474d45bf81196da45de13940::resource-broker:1f4a9711-e359-4e00-8ad3-c8bfd38446b3",
    "sub_type": "CRN"
  },
  "account": {
    "valid": true,
    "bss": "f71446b6474d45bf81196da45de13940",
    "frozen": true
  },
  "iat": 1746518443,
  "exp": 1746520239,
  "iss": "https://iam.cloud.ibm.com/identity",
  "grant_type": "urn:ibm:params:oauth:grant-type:iam-authz",
  "scope": "ibm openid resource-controller",
  "client_id": "resource-controller",
  "acr": 0,
  "amr": []
}
```
{: codeblock}

Basic
:    Basic authentication involves providing a username and a password, which are passed to the broker where the broker validates the caller's identity and whether the credential is valid. This method is less secure and not recommended as the credentials are sent repeatedly with every request.

    Basic and bearer authentication schemas are deprecated and will no longer be supported in the future due to security reasons. Use bearer CRN authentication for continued access instead.
    {: deprecated}

Bearer
:    In this method, the resource controller generates an IAM token using the provided API key. This is a token-based authentication method where `apikey` is used as the username, and the actual API key value is used as the password. The resource controller exchanges this API key for a JWT token, which is then sent to the broker. The broker validates the token’s authenticity and checks the caller’s identity before authorizing the request. The IAM token must be verified by the broker before authorizing the request. The keyset used for verification is available at [https://iam.cloud.ibm.com/identity/keys](https://iam.cloud.ibm.com/identity/keys){: external}. See the following example for a service ID token:

```json
{
  "iam_id": "iam-ServiceId-c1e45eff-8df9-49b7-af73-d9c6e6f99a69",
  "id": "iam-ServiceId-c1e45eff-8df9-49b7-af73-d9c6e6f99a69",
  "realmid": "iam",
  "jti": "c4810836-2467-49e6-9612-ad3595de4eb1",
  "identifier": "ServiceId-c1e45eff-8df9-49b7-af73-d9c6e6f99a69",
  "name": "My Service ID",
  "sub": "ServiceId-c1e45eff-8df9-49b7-af73-d9c6e6f99a69",
  "sub_type": "ServiceId",
  "authn": {
    "sub": "ServiceId-c1e45eff-8df9-49b7-af73-d9c6e6f99a69",
    "iam_id": "iam-ServiceId-c1e45eff-8df9-49b7-af73-d9c6e6f99a69",
    "sub_type": "ServiceId",
    "name": "My Service ID"
  },
  "account": {
    "valid": true,
    "bss": "f71446b6474d45bf81196da45de13940",
    "frozen": true
  },
  "iat": 1746519454,
  "exp": 1746523054,
  "iss": "https://iam.cloud.ibm.com/identity",
  "grant_type": "urn:ibm:params:oauth:grant-type:apikey",
  "scope": "ibm openid",
  "client_id": "default",
  "acr": 1,
  "amr": [
    "pwd"
  ]
}
```
{: codeblock}

## Add your broker
{: #broker-onboard-cfg}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center > My products**.
1. Select the service that you're onboarding.
1. From the Brokers page, click **Add broker**.
1. Enter the programmatic name for your broker and the URL at which your broker is reachable.
1. Select the authentication scheme to use when verifying the identity of the client that interacts with the broker. You can select from basic, bearer, and bearer CRN schemes.

    Basic and bearer authentication schemas are deprecated and will no longer be supported in the future due to security reasons. Use bearer CRN authentication for continued access instead.
    {: deprecated}

1. Select the broker type.
1. Enter the username for broker authentication. If you selected bearer authentication in the previous step, `apikey` is automatically entered for you as a username.

    For the bearer CRN authentication scheme, username and password information are not needed.
    {: note}

1. Enter the password for broker authentication. If you selected bearer authentication, enter the API key.
1. Click **Save**.

## Set up {{site.data.keyword.cloud_notm}} SSO
{: #broker-sso}

You can enable {{site.data.keyword.cloud_notm}} single sign-on for your service and add any redirect URLs that can handle authentication and authorization.

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center > My products**.
1. Select the service that you're onboarding.
1. From the Brokers page, click **Set up {{site.data.keyword.cloud_notm}} SSO**.
1. Add team members as owners of the Client ID. Owners can view and edit the Client ID.

   You can't remove yourself from the list of owners.
   {: note}

1. Click **Add** to add a redirect URL.
1. Enter the redirect URL that can handle the authentication and authorization of your service.
1. Click **Save**.
1. Copy your Client ID and secret.

    After you close the {{site.data.keyword.cloud_notm}} SSO panel, you can't view your secret. If the secret is lost, you must create a new Client ID.
    {: important}

1. Click **Done**.

    You must copy or show the secret to complete this action.
    {: note}

## Next steps
{: #broker-onboard-next}

You can now add your [pricing plan](/docs/sell?topic=sell-svc-pricing).
