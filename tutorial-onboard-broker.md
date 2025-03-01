---

copyright:
  years: 2021, 2024

lastupdated: "2025-01-15"

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

* For an example of how to build your broker, see the [{{site.data.keyword.cloud_notm}} reference broker](https://github.com/IBM-Cloud/onboarding-osb){: external} and the [{{site.data.keyword.cloud_notm}} Open Service Broker API](/apidocs/resource-controller/ibm-cloud-osb-api).

## Authentication schemes for brokers
{: #authentication-scheme-broker}

When you add a broker in Partner Center, you can select from the following three authentication schemes to verify the identity of the client that interacts with the broker:

Bearer CRN
:    In this method, the resource controller generates an IAM token with the identity of the broker CRN it is connecting to. Services authorize the call in their broker application by verifying that the identity of the caller matches the CRN of their respective broker. No API key and API key rotation are required in this method.

    Basic and bearer authentication schemas are deprecated and will no longer be supported in the future due to security reasons. Use bearer CRN authentication for continued access instead.
    {: deprecated}

Basic
:    Basic authentication involves providing a username and a password, which are passed to the broker where the broker validates the caller's identity and whether the credential is valid. This method is less secure and not recommended as the credentials are sent repeatedly with every request.

Bearer
:    This is a token-based authentication method, in which you provide `apikey` as the username, and the API key value as the password. After providing this information, the resource controller exchanges the API key to a JWT token. Then, the token gets passed to the broker where the broker validates the caller's identity and whether the token is valid.

## Add your broker
{: #broker-onboard-cfg}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center > My products**.
1. Select the service that you're onboarding.
1. From the Brokers page, click **Add broker**.
1. Enter the programmatic name for your broker and the URL at which your broker is reachable.
1. Select the authentication scheme to use when verifying the identity of the client that interacts with the broker. You can select from basic, bearer, and bearer cloud resource name (CRN) schemes.

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
