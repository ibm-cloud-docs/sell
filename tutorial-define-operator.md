---

copyright:
  years: 2021

lastupdated: "2021-11-10"

keywords: onboard software, third-party software, sell on IBM Cloud, partner center, operator, Red Hat OpenShift cluster, sample Node-RED Operator, Kubernetes cluster, product details, catalog listing, support, pricing, BYOL, DPA, digital provider agreement

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 10m 

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


# Defining the product details of an Operator 
{: #operator-define}
{: toc-content-type="tutorial"} 
{: toc-completion-time="10m"} 

This tutorial walks you through the steps for defining the details of a Node-RED Operator in {{site.data.keyword.cloud}} Partner Center. You can onboard an Operator bundle from a TGZ file or an Operator from a CSV file. By completing this tutorial, you review and sign the {{site.data.keyword.IBM}} Digital Provider Agreement, and define your catalog entry and product page, pricing model, and support experience. 
{: shortdesc}

This tutorial is one of four in a series that demonstrates how to onboard and publish a [sample Node-RED Operator](https://github.com/IBM-Cloud/operator-bundle-sample/releases){: external}. It uses a fictitious company that's called *Example Corp*. As you complete the tutorial, adapt each step to fit your product's needs.

## Before you begin
{: #operator-define-prereqs}

[Register your Operator in Partner Center](/docs/sell?topic=sell-operator-register).

## Confirm the digital provider agreement
{: #operator-dpa}
{: step}

Third-party providers are required to sign the {{site.data.keyword.IBM_notm}} Digital Provider Agreement, which sets the terms and conditions under which providers can onboard and sell products in {{site.data.keyword.cloud_notm}}. Or, third-party providers can upload a custom digital provider agreement in `.pdf`, `.doc`, or `.docx` file format. 

Custom digital provider agreements must be reviewed and approved by {{site.data.keyword.IBM_notm}}, which increases the time it takes for you to complete the onboarding process. 
{: note}

For the purposes of this tutorial, complete the following steps to sign the {{site.data.keyword.IBM_notm}} Digital Provider Agreement. 

1. From the My Products page in the {{site.data.keyword.cloud_notm}} Partner Center, click **Provide details** in the notification that explains that company details are required.
1. In the Digital provider agreement section, click **Standard**. 
1. Click the **{{site.data.keyword.IBM_notm}} Digital Provider Agreement** link to review the agreement. 
1. Select **I understand and agree to the {{site.data.keyword.IBM_notm}} Digital Provider Agreement**, and click **Save**.

## Provide the name of your Operator
{: #operator-name}
{: step}

Click **Dashboard**, and enter the name of your Operator, for example, `Example Corp Node-RED Operator 1.0.0`. Make sure the name meets the following requirements:
  
* Use 60 characters or less.
* Do not include "{{site.data.keyword.cloud_notm}}".
* Do not include the name of your company, former product names, or details like deployment targets and pricing. You can include this information in your readme file.

## Define your catalog entry and product page
{: #operator-catalog}
{: step}

Provide details that are displayed on your catalog entry and product page when your Operator is published in the {{site.data.keyword.cloud_notm}} catalog.

1. Click **Product details** > **Add logo**, and enter the URL to your company or product logo, such as `http://svgur.com/i/TTP.svg`.
1. Provide a short description of your product, which is displayed on your catalog entry. For the purposes of this tutorial, you can enter `This Operator is a developer tool.`
1. From the **Category** list, select an option that best fits how users might use your product, for example, **Developer tools**. Categories are used to organize products in the catalog based on common solutions, function, or use. 
1. Select **Third party** as the **Provider** type.
1. Enter keywords that users might use when searching the catalog for your product, for example, `cluster`, `operator`, `node-red`. 
1. Provide a list of features that highlights your product's attributes and benefits for users.

   Use a descriptive title and 1-2 sentences for each feature. You want the information to be visually scannable for users.
   {: tip}

1. Provide a detailed description of your product that explains its value and what users gain by using it. The detailed description is displayed at the beginning of your product page in the catalog. You can expand on the short description that you provide for your catalog entry, but don't simply repeat it. 
1. Provide links to high-quality images or videos to help illustrate what your product is, its value, and user benefits. The supported media types are images, videos in MP4 or WebM file format, and videos hosted on YouTube or Vimeo. 

   Some examples of effective media include an introductory walkthrough of your product, an explanation of what your product is and why users might want to use it, or a comparison of certain features.
   {: tip}

1. Provide a link to your product's warranted documentation. 

## Define your pricing model
{: #operator-pricing}
{: step}

{{site.data.keyword.cloud_notm}} supports two pricing models: free or bring your own license (BYOL). With the free pricing model, users can deploy as many instances with no additional software charges incurred. With the BYOL pricing model, {{site.data.keyword.cloud_notm}} doesn't charge users for the usage of the software, and third-party providers are responsible for licensing entitlement and enforcement. 

For the purposes of this tutorial, complete the following steps to add a BYOL pricing plan. 

1. Click **Pricing** > **Pricing plans**.
1. Click **Add plan** > **BYOL**.
1. Enter the name, URL, and description of the license, for example: 

    * Name: `BYOL for Example Corp Node-RED Operator 1.0.0`
    * URL: `byol.operator.examplecorp.html`
    * Description: `This BYOL license is required for the installation and use of the Example Corp Node-RED Operator.`

## Define your support experience
{: #operator-support}
{: step}

Provide details that help users understand how to get support if they encounter issues when using the Operator. Also, describe how {{site.data.keyword.cloud_notm}} Support can collaborate with your support team on customer escalations.

1. Click **Support**, and enter the URL to your support website, for example, `https://support.examplecorp.com/`.
2. For your support response process, describe what users can expect when they contact your support team, for example:

   `Contact Example Corp Support online at https://support.examplecorp.com, by chat at https://support.examplecorp.com/chat, or by phone at https://support.examplecorp.com/phone. Support is available 24 hours a day, 7 days a week, 365 days a year and is provided in English and French.`
  
3. Enter or select all the countries in which support for your product is based.
4. Describe the process that {{site.data.keyword.cloud_notm}} Support follows when customers escalate issues that are handled by your support team, for example: 

   `For client escalations, {{site.data.keyword.cloud_notm}} support representatives should follow the escalation process described at https://support.examplecorp.com/ibmcloudescalations.`
  
5. Describe how {{site.data.keyword.cloud_notm}} Support can contact your support team, for example:

   `For support process discussions, {{site.data.keyword.cloud_notm}} support leaders can reach out to the following Example Corp support leaders: Jane Doe (janedoe@examplecorp.com) and John Doe (johndoe@examplecorp.com).`

## Next steps
{: #operator-define-next}

[Onboard and validate your Operator](/docs/sell?topic=sell-operator-onboard). 
