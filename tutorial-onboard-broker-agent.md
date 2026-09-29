---

copyright:
  years: 2026

lastupdated: "2026-09-29"

keywords: onboard agent, third-party agent, sell on IBM Cloud, partner center, broker, SSO, single sign-on, client ID, redirect URL, authentication

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 15m

---

{{site.data.keyword.attribute-definition-list}}

# Onboarding a broker for your agent
{: #broker-agent-onboard}
{: toc-content-type="tutorial"}
{: toc-completion-time="15m"}

This tutorial walks you through how to set up {{site.data.keyword.cloud_notm}} single sign-on (SSO) and onboard a broker for your agent in Partner Center. The broker manages the lifecycle of your agent's service instances and connects your agent to the applications that developers are building. By completing this tutorial, you learn how to create a client ID for SSO, add redirect URLs, and register your broker.
{: shortdesc}

{{_include-segments/notes.md}}

## Before you begin
{: #broker-agent-prereqs}

Before you can start onboarding your broker, complete the following steps.

1. [Register your agent](/docs/sell?topic=sell-agent-register).
1. [Define the product details of your agent](/docs/sell?topic=sell-agent-define).
1. Build your broker. For an example of how to build your broker, see the [Open Service Broker reference application](https://github.com/IBM/onboarding-osb-node){: external} and the [{{site.data.keyword.cloud_notm}} Open Service Broker API](/docs/apis/resource-controller/ibm-cloud-osb-api).

Broker tasks require a technical member of your team. If you need to invite a technical team member to complete this step, you can do so from the Brokers page in Partner Center by clicking **Invite a team member** in the notification.
{: tip}

## Set up {{site.data.keyword.cloud_notm}} SSO
{: #broker-agent-sso}
{: step}

Setting up {{site.data.keyword.cloud_notm}} SSO creates a client ID that uniquely identifies your agent to {{site.data.keyword.cloud_notm}}'s identity provider. When a user tries to log in to your agent, instead of entering separate credentials, your agent redirects them to the {{site.data.keyword.cloud_notm}} login page. {{site.data.keyword.cloud_notm}} then issues tokens tied to your client ID and client secret, which your agent uses to grant the user access.

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation menu** icon ![Navigation menu icon](../icons/icon_hamburger.svg "Navigation menu") > **Partner Center** > **My products**.
1. Select the agent that you're onboarding.
1. From the **Brokers** page, click **Create Client ID for SSO**.
1. For **Owners**, add any team members who can view and edit the client ID.

   You can't remove yourself from the list of owners.
   {: note}

1. For **Redirect URLs**, click **Add** and enter the host URL that users are redirected to after a successful authorization, for example, `https://examplecorp-agent.com/auth/callback`.
1. Click **Next**.
1. Copy your client ID and secret and save them in a secure location.

   Your secret disappears automatically after 5 minutes and cannot be retrieved after you close this panel. If the secret is lost, you must create a new client ID.
   {: important}

1. Click **Done**.

## Add your broker
{: #broker-agent-add}
{: step}

After you set up SSO, register your broker in Partner Center. The broker handles provisioning and deprovisioning requests from {{site.data.keyword.cloud_notm}} on behalf of your agent.

1. From the **Brokers** page, click **Add broker**.
1. Enter a programmatic name for your broker, for example, `example-corp-agent-broker`. The name must be globally unique.
1. Enter the URL at which your broker is reachable, for example, `https://my-agent-broker.com`.
1. From the **Authentication scheme** list, select the scheme used to verify the identity of the client that interacts with the broker. For this tutorial, select **Bearer CRN**.

   Basic and bearer authentication schemes are deprecated. Use bearer CRN authentication instead.
   {: deprecated}

1. From the **Type** list, select the broker type. For this tutorial, select **provision-through**.

   Most service integrators use the `provision-through` model, where requests go through the resource controller to the service broker. In the `provision-behind` model, the request goes through the service integrator first, then to the resource controller.
   {: tip}

1. Click **Save**.

## Next steps
{: #broker-agent-next}

You can now [add a pricing plan for your agent](/docs/sell?topic=sell-agent-pricing).
