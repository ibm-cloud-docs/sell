---

copyright:
  years: 2026, 2026

lastupdated: "2026-09-29"

keywords: onboard agent, third-party agent, sell on IBM Cloud, partner center, product details, catalog entry, support, WXO agent, watsonx, programmatic name, catalog listing agreement

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 20m

---

{{site.data.keyword.attribute-definition-list}}

# Defining the product details of your agent
{: #agent-define}
{: toc-content-type="tutorial"}
{: toc-completion-time="20m"}

This tutorial walks you through the steps for defining specific details about your agent in Partner Center. By completing this tutorial, you accept the required agreement for agents, create your product, confirm your programmatic name, and define your catalog entry and support experience.
{: shortdesc}

{{_include-segments/notes.md}}

## Before you begin
{: #agent-define-prereqs}

Before you can start defining your agent details, complete the following step.

* [Register your agent](/docs/sell?topic=sell-agent-register).

## Accept the WXO CLA agreement
{: #agent-define-agreement}
{: step}

As a third-party provider offering an agent with a free or usage-based pricing plan, you are required to review and accept the WXO Contributor License Agreement (CLA). This agreement sets the terms under which your agent can be listed in the {{site.data.keyword.cloud_notm}} catalog.

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Navigation menu") > **Partner Center** > **My company**.
1. In the **Your company information** section, enable the **Free and usage-based agents** toggle.
1. In the **Agreement** section, select **I have read and agree to the standard Catalog Listing Agreement**.
1. Click **Save**.

If your company has a custom agreement that has already been approved by {{site.data.keyword.IBM_notm}}, select **I will provide a custom agreement already approved by {{site.data.keyword.IBM_notm}}** instead.
{: note}

## Provide your agent name and type
{: #agent-define-name}
{: step}

To start the onboarding process, create a new product entry in Partner Center and select the agent product type.

1. From the **My products** page, click **Create**.
1. Select **Create a product**, and click **Next**.
1. Click **Start now**.
1. Select **Agent** as the product type, and click **Next**.

   The product type is used for tax assessment purposes. For more information, see [Selling on IBM Cloud](/docs/sell?topic=sell-selling-clouds).
   {: important}

1. Enter the display name of your agent, for example, `Example Corp Agent 1.0.0`. Make sure that the name you enter meets the following requirements:

   * Use 60 characters or less.
   * Don't include "{{site.data.keyword.cloud_notm}}".
   * Don't include the name of your company, former product names, or pricing details.

1. Review the programmatic name that is automatically generated based on your company name and display name. You can clear this field and enter a custom value if you prefer. Click **Next**.

   The programmatic name is the unique ID used to identify your agent within {{site.data.keyword.cloud_notm}} services and tools. You can edit it until you submit your product for approval.
   {: tip}

1. Review your product details and click **Create**.

## Confirm your programmatic name
{: #agent-define-progname}
{: step}

After your product is created, you are prompted to confirm your programmatic name before you can proceed with the onboarding tasks. You can still edit the name at this point. After confirmation, you cannot change it.

For agents, your programmatic name is automatically approved after you confirm it. No manual review by {{site.data.keyword.IBM_notm}} is required.

1. From the **Product details** page, review the programmatic name shown in the notification banner.
1. If you want to make changes, click **Edit**, update the name, and click **Save**.
1. Click **Confirm**.
1. In the confirmation dialog, review the programmatic name and click **Confirm**.

## Note your IAM service ID
{: #agent-define-service-id}
{: step}

After you confirm your programmatic name, an operator IAM service ID is automatically generated for your agent. This service ID is used to authenticate and authorize your agent when it communicates with other {{site.data.keyword.cloud_notm}} services, for example, when submitting metering usage data.

You are also required to create an API key for your IAM service ID. To create your API key, see [Creating an API key for a service ID](/docs/iam?topic=iam-serviceidapikeys#create_service_key).

## Define your catalog entry and product page
{: #agent-define-catalog}
{: step}

Provide details that are displayed on your catalog entry and product page when your agent is published in the {{site.data.keyword.cloud_notm}} catalog.

1. Click **Catalog entry** > **Add logo**, and enter the URL to your company or product logo, for example, `https://svgur.com/i/TTP.svg`.
1. Provide a short description of your agent, which is displayed on your catalog entry. For example, `This agent is a {{site.data.keyword.wxorchestrate_short}} AI product offering that automates complex workflows across your enterprise tools.`
1. From the **Category** list, select **AI / Machine Learning**. Categories are used to organize products in the catalog based on common solutions, function, or use.
1. Review the pre-seeded `ai_agent` keyword and add any additional keywords that users might use when searching the catalog for your agent, for example, `automation`, `watsonx`, `orchestrate`.
1. Provide the URL to the end user license agreement (EULA) that users must agree to before using your agent, for example, `https://examplecorp.com/legal/agent-eula`.
1. Provide a detailed description of your agent that explains its value and what users gain by using it. The detailed description is displayed at the beginning of your product page in the catalog. You can expand on the short description, but don't simply repeat it. For example, `The Example Corp Agent is a {{site.data.keyword.wxorchestrate_short}} AI product. It connects to your existing enterprise tools to automate multi-step workflows without manual intervention. By integrating with platforms such as Salesforce, ServiceNow, and Slack, the agent handles tasks like processing requests, generating reports, and routing approvals end-to-end. Designed for business and operations teams, it reduces repetitive work, improves response times, and lets your team focus on higher-value activities.`

1. Provide a list of features that highlights your agent's attributes and benefits for users.

   Use a descriptive title and 1 - 2 sentences for each feature. You want the information to be visually scannable for users.
   {: tip}

   For the purposes of this tutorial, you can add the following example features:

   * **End-to-end workflow automation**: Automates complex, multi-step business processes across your connected enterprise tools, reducing manual effort and minimizing errors.
   * **Pre-built integrations**: Connects out of the box with popular platforms like Salesforce, ServiceNow, and Slack, so you can get started quickly without custom development.

1. Provide links to high-quality images or videos to help illustrate what your agent does, its value, and user benefits. The supported media types are images, videos in MP4 or WebM format, and videos hosted on YouTube or Vimeo.
1. Provide the URL to your product's documentation.

The product code and product code type fields are provided to you by your {{site.data.keyword.cloud_notm}} onboarding specialist. Contact your onboarding specialist if you have not received these values.
{: note}

## Define your support experience
{: #agent-define-support}
{: step}

Provide details that help users understand how to get support if they encounter issues when they use your agent.

1. Click **Support**.
1. Select who provides support for your product: **Third party** or **Community**.
1. Add a statement of support that describes the support you offer.
1. Provide the URL to your support site where users can learn more about your product and get support information.
1. Provide the URL to your service status page where customers can find information about key product events, such as planned maintenance windows.
1. From the **Add support contact methods** menu, select the ways users can contact you for support.
1. Add the locations and languages in which you provide support.
1. For **Support escalation process**, provide the number of hours that customers need to wait before escalating a case, and the minimum number of hours it takes to update customers about a support escalation.
1. For **Support contacts**, add the direct contact information for {{site.data.keyword.cloud_notm}} support leaders to communicate with your product's support leaders.

   The contact information that you provide in this section is not displayed on your product's details page in the catalog.
   {: note}

## Next steps
{: #agent-define-next}

[Onboard a broker for your agent](/docs/sell?topic=sell-broker-agent-onboard).
