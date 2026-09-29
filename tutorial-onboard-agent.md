---

copyright:
  years: 2026

lastupdated: "2026-09-29"

keywords: onboard agent, third-party agent, sell on IBM Cloud, partner center, native agent, agent development kit, watsonx Orchestrate, package, submit

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 30m

---

{{site.data.keyword.attribute-definition-list}}

# Submitting your agent details
{: #agent-onboard}
{: toc-content-type="tutorial"}
{: toc-completion-time="30m"}

This tutorial walks you through how to submit your agent for listing in the {{site.data.keyword.cloud_notm}} catalog through Partner Center. By completing this tutorial, you learn how to select the agent type, upload your agent package, and request approval.
{: shortdesc}

{{_include-segments/notes.md}}

## Before you begin
{: #agent-onboard-prereqs}

Before you can submit your agent details, complete the following steps.

1. [Register your agent](/docs/sell?topic=sell-agent-register).
1. [Define the product details of your agent](/docs/sell?topic=sell-agent-define).
1. [Onboard a broker for your agent](/docs/sell?topic=sell-broker-agent-onboard).
1. [Add a pricing plan for your agent](/docs/sell?topic=sell-agent-pricing).
1. Build, validate, and package your native agent by following the [Native Agent Onboarding](https://connect.watson-orchestrate.ibm.com/agent/onboard-native){: external} documentation. These steps are completed outside of Partner Center and include installing the Agent Development Kit, building and testing your agent, and packaging it into a ZIP file. The metadata in that package is used to populate your catalog listing.

Make sure that a technical team member is assigned to complete the build and packaging steps. If you need to invite one, go to **Partner Center** > **My team**.
{: tip}

## Select the agent type
{: #agent-onboard-type}
{: step}

You can choose between two agent types. Native agents are built and deployed within {{site.data.keyword.wxorchestrate_short}} by using the Agent Development Kit or Agent Builder. External agents are built outside {{site.data.keyword.wxorchestrate_short}} and hosted on a third-party platform. For the purposes of this tutorial, select **Native agent**.

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation menu** icon ![Navigation menu icon](../icons/icon_hamburger.svg "Navigation menu") > **Partner Center** > **My products**.
1. Select the agent that you're onboarding.
1. In the navigation menu, click **Agent**.
1. In the **Select the type of agent** section, select **Native agent**.

## Submit your agent details
{: #agent-onboard-submit}
{: step}

After you select the agent type, upload your agent package and review the details that are automatically populated from your package file. The maximum file size is 200 MB and the supported file type is `.zip`.

1. In the **Add agent package** section, drag and drop your ZIP package file or click to upload it.
1. Review the fields in the **Agent details** form to confirm that they reflect the values from your package file. The form is populated with the following fields from your package:

   Name
   :   The programmatic identifier for your agent.

   Display name
   :   The name shown to users in the catalog.

   Description
   :   A short description of your agent.

   Domain tags
   :   The domain categories used to classify your agent in the {{site.data.keyword.wxorchestrate_short}} catalog.

   LLM
   :   The language model your agent uses.

   Version
   :   The version of your agent package. The version must be greater than any previously submitted version.

   Channels (optional)
   :   The platforms where your agent operates.

   Style
   :   The interaction style of your agent.

   Language support
   :   The languages your agent supports.

   External protocol
   :   The protocol used for external communication.

1. Click **Save**.

## Next steps
{: #agent-onboard-next}

Submit your [request to publish your agent](/docs/sell?topic=sell-agent-publish) to the {{site.data.keyword.wxorchestrate_short}} and {{site.data.keyword.cloud_notm}} catalogs.
