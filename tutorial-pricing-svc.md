---

copyright:
  years: 2021, 2025

lastupdated: "2025-03-21"

keywords: onboard, SaaS, third-party service, partner center, pricing, usage, metering, plan, free, feature

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 10m

---

{{site.data.keyword.attribute-definition-list}}


# Add a pricing plan for your service
{: #svc-pricing}
{: toc-content-type="tutorial"}
{: toc-completion-time="10m"}

This tutorial walks you through the steps for adding pricing plans and features for your third-party service. By completing this tutorial, you submit required documentation, add your Export Control Classification Number (ECCN) and United Nations Standard Products and Services Code (UNSPSC), define your pricing plan, and add a list of features for your product.
{: shortdesc}

This tutorial is one of five in a series that demonstrates how to onboard and publish a service to the {{site.data.keyword.cloud_notm}} catalog. As you complete the tutorial, adjust each step to fit your needs.

## Before you begin
{: #svc-pricing-prereqs}

1. [Register your service](/docs/sell?topic=sell-svc-register).
1. [Define the product details of your service](/docs/sell?topic=sell-svc-define).
1. [Onboard a broker](/docs/sell?topic=sell-broker-onboard).

## Submit required documentation
{: #required-docs-paid}
{: step}

As part of this tutorial, you add a usage-based pricing plan. To receive disbursements for usage-based pricing plans, you must submit the Electronic Funds Transfer (EFT) form and required tax document.

To provide tax and EFT information, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Payments to me**.
1. Download the relevant EFT form, and complete it.

    A scanned copy of a voided check is required when you submit this form.
    {: important}

1. Download the relevant tax documentation, and complete it.
1. Submit the completed documentation by email to `apremit@us.ibm.com`. You must include `cloud.onboarding@ibm.com` on the email.
1. Select **I confirm that I completed and emailed all of the required documents.**
1. Click **Request approval**.

## Add an ECCN
{: #svc-eccn}
{: step}

You can choose from a list of common ECCNs or search for an ECCN. If you don't know the ECCN that best fits your product, you can use the [Commerce Control List](https://www.bis.doc.gov/index.php/licensing/commerce-control-list-classification/export-control-classification-number-eccn){: external} to determine a suitable ECCN. For the purposes of this tutorial, select a common ECCN.

1. Click **Pricing** > **Add ECCN**.
1. Select **Subject to EAR/not elsewhere specified**.
1. Click **Add**.

## Add a UNSPSC
{: #svc-unspsc}
{: step}

You can choose from a list of common UNSPSCs or search for a UNSPSC. If you need help with selecting the UNSPSC for your service, see [How to select UNSPSC codes?](https://help.ungm.org/hc/en-us/articles/360013132940-How-to-select-UNSPSC-codes){: external} to find the one that applies to your product. For the purposes of this tutorial, select a common UNSPSC.

1. Click **Pricing** > **Add UNSPSC**.
2. Select **Cloud-based software as a service**.
3. Click **Add**.

## Define your pricing plan
{: #svc-plan-details}
{: step}

{{site.data.keyword.cloud_notm}} supports two pricing models: free or usage-based. For the purposes of this tutorial, complete the following steps to add a usage-based plan.

By adding a usage-based pricing plan, you provide your suggested retail pricing information. However, {{site.data.keyword.IBM_notm}} reserves the right to set the final pricing for any product that is offered to customers in the {{site.data.keyword.cloud_notm}} catalog.
{: important}

1. Click **Add plan**.
1. Select **Usage-based** as the type of plan.
1. Enter a name for your plan. For the purposes of this tutorial, enter **Usage-based**.

   Plan names must be in English and can contain only alphanumeric characters, hyphens, spaces, and periods.
   {: note}

1. Enter a description for your plan. Include any limitations that users must know. For example, `The usage-based plan is for our upgraded services. This plan does not include our advanced features.`
1. Select **Per-location** for the deployment location.
1. Select **Specific locations** to restrict deployment.
1. Choose `Dallas - Region`, `London - Region`, and `Osaka - Region`.
1. Select the broker that you want to link to this plan.

    If you haven't added a broker to your account, you can't link a broker to your plan. After you add a broker, you can link it by editing the pricing plan.
    {: note}

1. Click **Save**.
1. Click **Add metrics**.
1. In the Usage metrics section, click **Add metrics**.
1. Enter `1` as the smallest unit that customers pay.
1. Select **Instance** as the unit.
1. Enter `Instance` as the display name for the unit.
1. Select **Per unit** as the charge method.
1. Enter `1` as the USD price.
1. Click **Done**.
1. When you are ready to submit your pricing plan and metering for review, click **Request update**.

## Add features for your service
{: #svc-add-feature}
{: step}

If you completed the steps to define your pricing plan, you can add a list of features for your service. These features uniquely identify your product's attributes and differentiate your pricing plan from others. By providing a list of features for your product, you can help customers choose the most suitable pricing plan for their use case.

You can add up to five features for your product, but you must add at least one. The first feature that you add appears more prominently. Include the most important and differentiating details as the first feature.
{: note}

To add features for your service, complete the following steps:

1. Click **Pricing**.
1. Select a pricing plan from the table that you previously added. After you select a plan, you are redirected to the **Pricing plan details** page.
1. Click **Add features**.
1. Enter a description for each feature.
   - You can remove any feature that you add by clicking **Remove feature**.
1. Click **Save**.

## Review and submit the digital platform reseller agreement
{: #service-pricing-dra}
{: step}

If you plan to offer usage-based pricing plans, it is required to review and submit the {{site.data.keyword.IBM_notm}} Digital Platform Reseller Agreement. This legal agreement sets the terms and conditions under which providers can onboard and sell products in {{site.data.keyword.cloud_notm}}. Or, you can upload a custom digital provider agreement in `.pdf`, `.doc`, or `.docx` file format.

Digital platform reseller agreements and custom digital provider agreements must be reviewed and approved by {{site.data.keyword.IBM_notm}}, which increases the time it takes for you to complete the onboarding process. If you upload a custom digital provider agreement, the uploaded files are scanned for viruses, which might take a few minutes to complete. If a virus is detected, it is recommended to run another virus scan on your file, and then try uploading it again.
{: note}

Complete the following steps to review and submit the {{site.data.keyword.IBM_notm}} Digital Platform Reseller Agreement:

1. From the My products page in the {{site.data.keyword.cloud_notm}} Partner Center, click **Go to My company** in the notification that explains that company details are required.
1. Choose **I plan to offer usage-based pricing plans** from the Agreements section.
1. Click the **{{site.data.keyword.IBM_notm}} Digital Platform Reseller Agreement** to review the agreement.
1. Select **I read and agree to the {{site.data.keyword.IBM_notm}} Digital Platform Reseller Agreement**, and click **Save**.

## Next steps
{: #svc-pricing-next}

Submit your [request to publish your service](/docs/sell?topic=sell-svc-publish) to the {{site.data.keyword.cloud_notm}} catalog.
