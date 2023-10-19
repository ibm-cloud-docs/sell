---

copyright:
  years: 2021, 2023

lastupdated: "2023-10-19"

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

This tutorial walks you through how to onboard a broker that you use to connect a pricing plan to your third-party service. When users create instances of your service from the {{site.data.keyword.cloud}} catalog, the broker manages the lifecycle of those instances, and connects the service to the applications that developers are building.
{: shortdesc}

This tutorial is one of five in a series that demonstrates how to onboard and publish a third-party service to {{site.data.keyword.cloud_notm}}. As you complete the tutorial, adjust each step to fit your product's needs.

## Before you begin
{: #broker-onboard-prereqs}

1. For an example of how to build your broker, see [IBM Cloud reference broker](https://github.com/IBM-Cloud/onboarding-osb){: external}.

1. Make sure you have the following API keys:
   * An onboarding API key for access to the Global Catalog API.
   * An {{site.data.keyword.cloud_notm}} API key for access to your deployment target.

For more information, see [Managing API keys](/docs/account?topic=account-userapikey).

## Add your broker
{: #broker-onboard-cfg}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My products**.
1. Select the service that you're onboarding.
1. From the Brokers tab, click **Add broker**.
1. Enter the name, URL, username, and password for your broker, and click **Done**.

## Set up {{site.data.keyword.cloud_notm}} SSO
{: #broker-sso}

You can enable {{site.data.keyword.cloud_notm}} single sign-on for your service and add any redirect URLs that can handle authentication and authorization.

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My products**.
1. Select the service that you're onboarding.
1. From the Brokers tab, click **Set up {{site.data.keyword.cloud_notm}} SSO**.
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
