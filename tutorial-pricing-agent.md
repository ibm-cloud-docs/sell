---

copyright:
  years: 2026

lastupdated: "2026-09-29"

keywords: onboard agent, third-party agent, sell on IBM Cloud, partner center, pricing, usage, metering, plan, ECCN, UNSPSC, feature, metrics

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 15m

---

{{site.data.keyword.attribute-definition-list}}

# Adding a pricing plan for your agent
{: #agent-pricing}
{: toc-content-type="tutorial"}
{: toc-completion-time="15m"}

This tutorial walks you through the steps for adding a pricing plan and metrics for your agent. By completing this tutorial, you submit the required Electronic Funds Transfer (EFT) and tax forms, and add your Export Control Classification Number (ECCN) and United Nations Standard Products and Services Code (UNSPSC). You also define your pricing plan, add usage metrics, and configure plan features.
{: shortdesc}

{{_include-segments/notes.md}}

## Before you begin
{: #agent-pricing-prereqs}

Before you can add a pricing plan for your agent, complete the following steps.

1. [Register your agent](/docs/sell?topic=sell-agent-register).
1. [Define the product details of your agent](/docs/sell?topic=sell-agent-define).
1. [Onboard a broker for your agent](/docs/sell?topic=sell-broker-agent-onboard).

## Submit EFT and tax forms
{: #agent-pricing-eft}
{: step}

To receive disbursements for usage-based pricing plans, you must submit an Electronic Funds Transfer (EFT) form and a tax form (W-9 for US companies, W-8 for companies outside the US). You must also include a bank document with your submission.

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation menu** icon ![Navigation menu icon](../icons/icon_hamburger.svg "Navigation menu") > **Partner Center** > **Payments to me**.
1. In the **Complete EFT form** section, download the relevant form:
   - For companies based in the United States, click **EFT, US**.
   - For companies based outside of the United States, click **EFT, International**.
1. In the **Complete tax form** section, download the relevant form:
   - For companies based in the United States, click **W-9**.
   - For companies based outside of the United States, click **W-8**.
1. Complete both forms and prepare one of the following bank documents to include with your submission:
   - A scanned copy of a voided check
   - A bank letter that is signed and stamped by the bank
   - An online bank statement (for companies outside the United States only)

   The bank document must include the bank name, account number, routing number (or bank key or ABA), and the account holder's name.
   {: important}

1. Email all completed forms and your bank document to `apremit@us.ibm.com` with `cloud.onboarding@ibm.com` copied, using the subject line `IBM Cloud Partner Center EFT and tax forms`.
1. Select **I confirm that I completed and emailed all of the required documents** and click **Request approval**.

## Add an ECCN
{: #agent-pricing-eccn}
{: step}

An Export Control Classification Number (ECCN) is a five-character alphanumeric key that identifies items based on the nature of the product and its technical parameters. You must provide an ECCN to onboard your agent to the {{site.data.keyword.cloud_notm}} catalog. You can choose from a list of common ECCNs or search for an ECCN. If you don't know the ECCN that best fits your product, use the [Commerce Control List](https://www.bis.gov/licensing/classify-your-item#WhatisanECCN?){: external} to determine a suitable one. For the purposes of this tutorial, select a common ECCN.

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation menu** icon ![Navigation menu icon](../icons/icon_hamburger.svg "Navigation menu") > **Partner Center** > **My products**.
1. Select the agent that you're onboarding.
1. Click **Pricing** > **Add ECCN**.
1. Select a common ECCN, for example, **F1AZ - EAR99: Subject to EAR/not elsewhere specified**.
1. Click **Add**.

## Add a UNSPSC
{: #agent-pricing-unspsc}
{: step}

A United Nations Standard Products and Services Code (UNSPSC) is an eight-digit global classification system that categorizes products and services. You must provide a UNSPSC to onboard your agent to the {{site.data.keyword.cloud_notm}} catalog. You can choose from a list of common UNSPSCs or search for one that applies to your product. If you need help selecting the right code, see [How to select UNSPSC codes](https://help.ungm.org/hc/en-us/articles/360013132940-How-to-select-UNSPSC-codes){: external}. For the purposes of this tutorial, select a common UNSPSC.

1. Click **Add UNSPSC**.
1. Select a common UNSPSC, for example, **Cloud-based software as a service (81162000)**.
1. Click **Add**.

## Define your pricing plan
{: #agent-pricing-plan}
{: step}

{{site.data.keyword.cloud_notm}} supports two pricing models for agents: free or usage-based. For the purposes of this tutorial, add a usage-based plan.

By adding a usage-based pricing plan, you provide your suggested retail pricing information. However, {{site.data.keyword.IBM_notm}} reserves the right to set the final pricing for any product that is offered to customers in the {{site.data.keyword.cloud_notm}} catalog.
{: important}

1. In the **Pricing plans** section, click **Add plan**.
1. Select **Usage-based** as the type of plan.
1. Enter a display name for your plan, for example, `Paid plan`.

   Plan names must be in English and can contain only alphanumeric characters, hyphens, spaces, and periods.
   {: note}

1. Enter a description for your plan, including any limitations that users must know. For example, `Usage-based pricing plan for the Example Corp Agent. Charges are calculated based on the number of tokens consumed per month.`
1. Select how resource instances should be deployed. For the purposes of this tutorial, select **Globally**.
1. Select the broker that you want to link to this plan.

   If you haven't added a broker yet, you can't link one to your plan. After you add a broker, you can link it by editing the pricing plan.
   {: note}

1. Click **Save**.

## Add features for your plan
{: #agent-pricing-features}
{: step}

After you define your pricing plan, you can add a list of features for your agent. Features uniquely identify your plan's attributes and help customers choose the most suitable pricing plan for their use case. You can add up to five features per plan, but you must add at least one. The first feature you add appears most prominently, so include the most important detail first.

1. Click your plan, `Paid plan`, from the pricing plan list.
1. From the plan details page, click **Add feature** in the **Features** section.
1. Click **Add feature** and enter a description for each feature, for example:
   - `Pay only for what you use, based on the number of API calls your agent makes each month.`
   - `No upfront commitment required. Scale up or down as your usage changes.`
1. Click **Save**.

## Add usage metrics
{: #agent-pricing-metrics}
{: step}

After you add your plan, you can add usage metrics to define how customers are charged for using your agent. Metrics must be added to your plan before you can request pricing approval.

1. Click your plan, `Paid plan`, from the pricing plan list.
1. From the plan details page, scroll to the **Usage metrics** section and click **Add metrics**.
1. In the **Add parts** panel, set the smallest unit that customers pay for. For the purposes of this tutorial, enter `1`.
1. Select the charge unit type. For the purposes of this tutorial, click **Make a custom unit** at the bottom of the list and enter `TOKEN` as the custom unit name.
1. Enter how you want to display the unit to customers in the catalog, for example, `Token`.
1. Enter the charge unit name for this metric in your pricing plan, for example, `TOKEN`.
1. Select **Standard Add** as the usage calculation method.
1. Select **Per unit** as the charge method.
1. Enter the USD price per unit, for example, `0.01`.
1. Click **Save**.

## Request pricing approval
{: #agent-pricing-approval}
{: step}

Pricing approval is a two-phase process. First, an approver from {{site.data.keyword.IBM_notm}} reviews your pricing configuration. After that is approved, you submit metering evidence to complete the process.

1. From the plan details page, click **Request approval** in the **Pricing approval** section. The status updates to **Pricing configuration was submitted for approval**.
1. Wait for {{site.data.keyword.IBM_notm}} to approve your pricing configuration. When the pricing configuration is approved, the status updates to **Pricing configuration is approved** and the **Submit metering evidence** button becomes available.
1. Click **Submit metering evidence** and complete the following tasks:
   1. Preview your agent in its draft state in the catalog by clicking **Go to your catalog preview**. Use the estimator to generate a price estimate that incorporates all the metrics you added, and upload the estimate file by clicking **Add file** in the first section.
   1. Generate metered usage for all metrics of this plan using the [Usage Metering API](/docs/apis/usage-metering). After you generate usage and can view it on the Usage page in your account, upload a screen capture of the rated usage by clicking **Add file** in the second section.
   1. Upload a screen capture of the resource usage data that you previously submitted to the {{site.data.keyword.cloud_notm}} Usage Metering API by clicking **Add file** in the third section.
1. Click **Done**.

## Next steps
{: #agent-pricing-next}

[Submit your agent details](/docs/sell?topic=sell-agent-onboard) to complete the onboarding process.
