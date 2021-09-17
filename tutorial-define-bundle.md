---

copyright:
  years: 2021

lastupdated: "2021-09-01"

keywords: onboard software, third-party software, sell on IBM Cloud, partner center, operator, validate, test, Red Hat OpenShift cluster, bundle, Kubernetes cluster, product details, catalog listing, support, pricing, BYOL

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 15m 

---

{:shortdesc: .shortdesc}
{:screen: .screen}  
{:codeblock: .codeblock}  
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:beta: .beta}
{:external: target="_blank" .external}
{:step: data-tutorial-type='step'} 

# Defining the product details of your Operator bundle 
{: #bundle-define}
{: toc-content-type="tutorial"} 
{: toc-completion-time="10m"} 

This tutorial walks you through the steps for defining the details of an Operator bundle in {{site.data.keyword.cloud}} Partner Center. By completing this tutorial, you review and sign the {{site.data.keyword.IBM}} Digital Provider Agreement, and define your catalog entry and product page, pricing model, and support experience. 
{: shortdesc}

The process to sell third-party software is still under development. With the current release, you can bring your own licenses or deliver your third-party software for free. If you have questions, contact us at cloud.onboarding@us.ibm.com.
{: beta}

This tutorial is one of four in a series that demonstrates how to onboard and publish a sample Operator bundle from the {{site.data.keyword.redhat_full}} {{site.data.keyword.openshiftshort}} Certified registry. It uses a fictitious company that's called *Example Corp*. As you complete the tutorial, adapt each step to fit your product's needs.

## Before you begin
{: #bundle-define-prereqs}

[Register your Operator bundle in Partner Center](/docs/sell?topic=sell-bundle-register).

## Confirm the digital provider agreement
{: #bundle-dpa}
{: step}

Third-party providers are required to sign the {{site.data.keyword.IBM_notm}} Digital Provider Agreement, which sets the terms and conditions under which providers can onboard and sell products in {{site.data.keyword.cloud_notm}}. Or, third-party providers can upload a custom digital provider agreement in `.pdf`, `.doc`, or `.docx` file format. 

Custom digital provider agreements must be reviewed and approved by {{site.data.keyword.IBM_notm}}, which increases the time it takes for you to complete the onboarding process. 
{: note}

For the purposes of this tutorial, complete the following steps to sign the {{site.data.keyword.IBM_notm}} Digital Provider Agreement. 

1. From the My Products page in the {{site.data.keyword.cloud_notm}} Partner Center, click **Provide details** in the notification that explains that company details are required.
1. In the Digital provider agreement section, click **Standard**. 
1. Click the **{{site.data.keyword.IBM_notm}} Digital Provider Agreement** link to review the agreement. 
1. Select **I understand and agree to the {{site.data.keyword.IBM_notm}} Digital Provider Agreement**, and click **Save**.

## Enter the name of your Operator bundle
{: #bundle-name}
{: step}

Click **Dashboard**, and enter the name of your Operator bundle as it appears in the {{site.data.keyword.redhat_notm}} registry in the product name field. For example, for the purposes of this tutorial, you can enter `Akka Cluster Operator`. 

## Define your catalog entry and product page
{: #bundle-catalog}
{: step}

Provide details that are displayed on your catalog entry and product page when your Operator bundle is published in the {{site.data.keyword.cloud_notm}} catalog.

1. Click **Product details** > **Add logo**, and enter the URL to your company or product logo, such as `http://svgur.com/i/TTP.svg`.
1. Provide a short description of your product, which is displayed on your catalog entry. For the purposes of this tutorial, you can enter `This Operator is a developer tool.`
1. From the **Category** list, select an option that best fits how users might use your product, for example, **Developer tools**. Categories are used to organize products in the catalog based on common solutions, function, or use. 
1. Select **Third party** as the **Provider** type.
1. Enter keywords that users might use when searching the catalog for your product, for example, `dev tools` and `operator`.
1. Provide a list of features that highlights your product's attributes and benefits for users.

   Use a descriptive title and 1-2 sentences for each feature. You want the information to be visually scannable for users.
   {: tip}

1. Provide a detailed description of your product that explains its value and what users gain by using it. The detailed description is displayed at the beginning of your product page in the catalog. You can expand on the short description that you provide for your catalog entry, but don't simply repeat it. 
1. Provide links to high-quality images or videos to help illustrate what your product is, its value, and user benefits. The supported media types are images, videos in MP4 or WebM file format, and videos hosted on YouTube or Vimeo. 

   Some examples of effective media include an introductory walkthrough of your product, an explanation of what your product is and why users might want to use it, or a comparison of certain features.
   {: tip}

1. Provide a link to your product's warranted documentation. 

## Defining your pricing model
{: #bundle-pricing}
{: step}

{{site.data.keyword.cloud_notm}} supports two pricing models: free or bring your own license (BYOL). With the free pricing model, users can deploy as many instances with no additional charges incurred. With the BYOL pricing model, {{site.data.keyword.cloud_notm}} doesn't charge users for the usage of the product, and third-party providers are responsible for licensing entitlement and enforcement. 

For the purposes of this tutorial, offer your Operator bundle for free by clicking **Pricing**, and selecting **Free**. 

## Define your support experience
{: #bundle-support}
{: step}

Provide details that help users understand how to get support if they encounter issues when using the Operator bundle. Also, describe how {{site.data.keyword.cloud_notm}} Support can collaborate with your support team on customer escalations.

1. Click **Support**, and enter the URL to your support website, for example, `https://support.examplecorp.com/`.
2. For your support response process, describe what users can expect when they contact your support team, for example:

   `Contact Example Corp Support online at https://support.examplecorp.com, by chat at https://support.examplecorp.com/chat, or by phone at https://support.examplecorp.com/phone. Support is available 24 hours a day, 7 days a week, 365 days a year and is provided in English and French.`
  
3. Enter or select all the countries in which support for your product is based.
4. Describe the process that {{site.data.keyword.cloud_notm}} Support follows when customers escalate issues that are handled by your support team, for example:

   `For client escalations, {{site.data.keyword.cloud_notm}} support representatives should follow the escalation process described at https://support.examplecorp.com/ibmcloudescalations.`
  
5. Describe how {{site.data.keyword.cloud_notm}} Support can contact your support team, for example:

   `For support process discussions, {{site.data.keyword.cloud_notm}} support leaders can reach out to the following Example Corp support leaders: Jane Doe (janedoe@examplecorp.com) and John Doe (johndoe@examplecorp.com).`

## Next steps
{: #bundle-define-next}

[Onboard and validate your Operator bundle](/docs/sell?topic=sell-bundle-onboard) 
