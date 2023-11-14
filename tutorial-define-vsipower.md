---

copyright:
  years: 2022, 2023

lastupdated: "2023-11-14"

keywords: onboard software, third-party software, sell on IBM Cloud, partner center, virtual server image, virtual machine image, image, vm, vsi, product details, catalog entry, support, pricing, BYOL, terraform, catalog, power, power vsi, power systems virtual server

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 10m 

---

{{site.data.keyword.attribute-definition-list}}


# Defining the product details of a virtual server image for Power Systems
{: #vsipower-define}
{: toc-content-type="tutorial"} 
{: toc-completion-time="10m"} 

This tutorial walks you through the steps for defining the details of a virtual server image for {{site.data.keyword.powerSys_notm}} in {{site.data.keyword.cloud}} Partner Center. By completing this tutorial, you review and sign the {{site.data.keyword.IBM}} Digital Provider Agreement, and define your catalog entry and product page, pricing model, and support experience. 
{: shortdesc}

This tutorial demonstrates how to onboard and publish a [sample virtual server image for Power Systems Virtual Server](https://github.com/IBM-Cloud/isv-power-vsi-product-deploy-sample){: external}. It uses a fictitious company that's called *Example Corp*. As you complete the tutorial, adapt each step to fit your product's needs.

## Before you begin
{: #vsipower-define-prereqs}

[Register your virtual server image](/docs/sell?topic=sell-vsipower-register).

## Confirm the digital provider agreement
{: #vsipower-dpa}
{: step}

As a third-party provider, you are required to sign the {{site.data.keyword.IBM_notm}} Digital Provider Agreement if you plan to offer bring your own license plans for your product. The {{site.data.keyword.IBM_notm}} Digital Provider Agreement sets the terms and conditions under which providers can onboard and sell products in {{site.data.keyword.cloud_notm}}. Or, you can upload a custom digital provider agreement in `.pdf`, `.doc`, or `.docx` file format.

Custom digital provider agreements must be reviewed and approved by {{site.data.keyword.IBM_notm}}, which increases the time it takes for you to complete the onboarding process. 
{: note}

For the purposes of this tutorial, complete the following steps to sign the {{site.data.keyword.IBM_notm}} Digital Provider Agreement. 

1. From the My products page in the {{site.data.keyword.cloud_notm}} Partner Center, click **Provide details** in the notification that explains that company details are required.
1. Choose **I plan to offer bring your own license pricing plans** from the Agreements section.
1. Click the **{{site.data.keyword.IBM}} Digital Provider Agreement** link to review the agreement.
1. Select **I have read and agree to the {{site.data.keyword.IBM}} Digital Provider Agreement.**, and click **Save**.

## Provide your product name and type
{: #vsipower-name}
{: step}

When you add a product, you can add a new product or import an existing product from a private catalog. For the purposes of this tutorial, add a new product. 

1. From the {{site.data.keyword.cloud_notm}} Partner Center, click **Create**.
1. Enter the name of your virtual server image, for example, `Example Corp Virtual Server Image 1.0.0`. Make sure that the name meets the following requirements:
  
   * Use 60 characters or less.
   * Do not include "{{site.data.keyword.cloud_notm}}".
   * Do not include the name of your company, former product names, or details like deployment targets and pricing. You can include this information in your readme file. 

1. Select the product type. For {{site.data.keyword.powerSys_notm}}, select **Deployable software**. 

    The product type that you select is used for tax assessment purposes.
    {: important}
    
1. Click **Add**.

## Define your catalog entry and product page
{: #vsipower-catalog}
{: step}

Provide details that are displayed on your catalog entry and product page when your virtual server image is published in the {{site.data.keyword.cloud_notm}} catalog.

1. Click **Product details**, and enter the URL to your company or product logo, such as `http://svgur.com/i/TTP.svg`.
1. Provide a short description of your product, which is displayed on your catalog entry. 
1. From the **Category** list, select an option that best fits how users might use your product, for example, **Compute/Virutal Machines**. Categories are used to organize products in the catalog based on common solutions, function, or use.
1. Enter keywords that users might use when they search the catalog for your product, for example, `virtual machine`, `compute`,`terraform`, and `power`.
1. Provide a list of features that highlights your product's attributes and benefits for users.

   Use a descriptive title and 1 - 2 sentences for each feature. You want the information to be visually scannable for users.
   {: tip}

1. Provide a detailed description of your product that explains its value and what users gain by using it. The detailed description is displayed at the beginning of your product page in the catalog. You can expand on the short description that you provide for your catalog entry, but don't simply repeat it. 
1. Provide links to high-quality images or videos to help illustrate what your product is, its value, and user benefits. The supported media types are images, videos in MP4 or WebM file format, and videos hosted on YouTube or Vimeo.

   Some examples of effective media include an introductory walkthrough of your product, an explanation of what your product is and why users might want to use it, or a comparison of certain features. 
   {: tip}

1. Provide a link to your product's warranted documentation.

## Define your pricing model
{: #vsipower-pricing}
{: step}

{{site.data.keyword.cloud_notm}} supports two pricing models: free or bring your own license (BYOL). With the free pricing model, users can deploy as many instances with no additional software charges incurred. With the BYOL pricing model, {{site.data.keyword.cloud_notm}} doesn't charge users for the usage of the software, and the third-party provider is responsible for licensing entitlement and enforcement. 

For the purposes of this tutorial, complete the following steps to add a BYOL pricing plan. 

1. Click **Pricing** > **Pricing plans**.
1. Click **Add plan** > **BYOL**.
1. Enter the name, URL, and description of the license, for example: 

* Name: `BYOL for Example Corp Virtual Server Image 1.0.0`
* URL: `byol.vsimage.examplecorp.html`
* Description: `This BYOL license is required for the installation and use of the Example Corp Virtual Server Image.`

## Define your support experience
{: #vsipower-support}
{: step}

Provide details that help users understand how to get support if they encounter issues when they use the Operator bundle. For more information about providing support information, see [Defining your support experience](/docs/sell?topic=sell-sw-support-details). 

To define your product's support experience, use the following steps:

{{site.data.content.steps-support-experience}}

## Next steps
{: #vsipower-define-next}

[Onboard and validate your virtual server image](/docs/sell?topic=sell-vsipower-onboard). 
