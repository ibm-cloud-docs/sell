---

copyright:
  years: 2021, 2024
  
lastupdated: "2024-05-02"

keywords: onboard software, third-party software, sell on IBM Cloud, partner center, virtual server image, virtual machine image, image, vm, vsi, product details, catalog entry, support, pricing, BYOL, terraform, catalog

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 10m 

---

{{site.data.keyword.attribute-definition-list}}


# Defining the product details of a virtual server image
{: #vsimage-define}
{: toc-content-type="tutorial"} 
{: toc-completion-time="10m"}

Onboarding virtual server images with Terraform is deprecated. After 29 March 2024, onboarding virtual server images with Terraform is no longer supported as a delivery method, which means that no new virtual server images with Terraform can be onboarded. Existing VSIs in the {{site.data.keyword.cloud_notm}} catalog will be available to use, but to take advantage of version updates and ensure continued support, onboard virtual server images for Virtual Private Cloud directly. For more information, see [Onboarding a virtual server image for VPC](/docs/account?topic=account-catalog-vsivpc-tutorial).
{: deprecated}

This tutorial walks you through the steps for defining the details of a virtual server image with Terraform in {{site.data.keyword.cloud}} Partner Center. By completing this tutorial, you review and sign the {{site.data.keyword.IBM}} Digital Provider Agreement, and define your catalog entry and product page, pricing model, and support experience. 
{: shortdesc}

This tutorial is one of four in a series that demonstrates how to onboard and publish a [sample virtual server image with Terraform](https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/tree/v1.0){: external}. It uses a fictitious company that's called *Example Corp*. As you complete the tutorial, adapt each step to fit your product's needs.

## Before you begin
{: #vsimage-define-prereqs}

[Register your virtual server image](/docs/sell?topic=sell-vsimage-register).

## Confirm the digital provider agreement
{: #vsimage-dpa}
{: step}

As a third-party provider, you are required to sign the {{site.data.keyword.IBM_notm}} Digital Provider Agreement if you plan to offer bring your own license plans for your product. The {{site.data.keyword.IBM_notm}} Digital Provider Agreement sets the terms and conditions under which providers can onboard and sell products in {{site.data.keyword.cloud_notm}}. Or, you can upload a custom digital provider agreement in `.pdf`, `.doc`, or `.docx` file format.

Custom digital provider agreements must be reviewed and approved by {{site.data.keyword.IBM_notm}}, which increases the time it takes for you to complete the onboarding process. The uploaded files are scanned for viruses, which might take a few minutes to complete. If a virus is detected, it is recommended to run another virus scan on your file, and then try uploading it again.
{: note}

For the purposes of this tutorial, complete the following steps to sign the {{site.data.keyword.IBM_notm}} Digital Provider Agreement.

1. From the My products page in the {{site.data.keyword.cloud_notm}} Partner Center, click **Provide details** in the notification that explains that company details are required.
1. Choose **I plan to offer bring your own license pricing plans** from the Agreements section.
1. Click the **{{site.data.keyword.IBM_notm}} Digital Provider Agreement** link to review the agreement.
1. Select **I have read and agree to the {{site.data.keyword.IBM_notm}} Digital Provider Agreement.**, and click **Save**.

## Provide your product name and type
{: #vsimage-name}
{: step}

You can add a new product or import an existing product from a private catalog. For the purposes of this tutorial, add a product.

1. From the **My products** page in {{site.data.keyword.cloud_notm}} Partner Center, click **Create**.
1. Click **Create a product**, and click **Next > Start now**.
1. Select **Software** as the type of product that you're onboarding, and click **Next**.

    The product type is used for tax assessment purposes. For more information, see [Selling on IBM Cloud](/docs/sell?topic=sell-selling-clouds).
    {: important}

1. Enter the display name of your Operator, for example, `Example Node-RED Operator 1.0.0`. Make sure that the name you enter meets the following requirements:

   * Use 60 characters or less.
   * Don't include "{{site.data.keyword.cloud_notm}}".
   * Don't include the name of your company, former product names, or pricing details.

1. Optionally, enter the programmatic name of your product, and click **Next**.
1. Review your product details and click **Create**.

## Define your catalog entry and product page
{: #vsimage-catalog}
{: step}

Provide details that are displayed on your catalog entry and product page when your virtual server image is published in the {{site.data.keyword.cloud_notm}} catalog.

1. Click **Catalog entry**, and enter the URL to your company or product logo, such as `http://svgur.com/i/TTP.svg`.
1. Provide a short description of your product, which is displayed on your catalog entry. 
1. From the **Category** list, select an option that best fits how users might use your product, for example, **Compute/Virutal Machines**. Categories are used to organize products in the catalog based on common solutions, function, or use.
1. Enter keywords that users might use when they search the catalog for your product, for example, `virtual machine`, `compute`, and `terraform`.
1. Provide a list of features that highlights your product's attributes and benefits for users.

   Use a descriptive title and 1 - 2 sentences for each feature. You want the information to be visually scannable for users.
   {: tip}

1. Provide a detailed description of your product that explains its value and what users gain by using it. The detailed description is displayed at the beginning of your product page in the catalog. You can expand on the short description that you provide for your catalog entry, but don't simply repeat it. 
1. Provide links to high-quality images or videos to help illustrate what your product is, its value, and user benefits. The supported media types are images, videos in MP4 or WebM file format, and videos hosted on YouTube or Vimeo.

   Some examples of effective media include an introductory walkthrough of your product, an explanation of what your product is and why users might want to use it, or a comparison of certain features. 
   {: tip}

1. Provide a link to your product's warranted documentation.

## Define your pricing model
{: #vsimage-pricing}
{: step}

{{site.data.keyword.cloud_notm}} supports two pricing models: free or bring your own license (BYOL). With the free pricing model, users can deploy as many instances with no additional software charges incurred. With the BYOL pricing model, {{site.data.keyword.cloud_notm}} doesn't charge users for the usage of the software, and the third-party provider is responsible for licensing entitlement and enforcement. 

For the purposes of this tutorial, complete the following steps to add a BYOL pricing plan. 

1. Click **Pricing** > **Pricing plans**.
1. Click **Add plan** > **BYOL**.
1. Enter the name, URL, and description of the license, for example: 

* Name: `BYOL for Example Virtual Server Image 1.0.0`
* URL: `byol.vsimage.example.html`
* Description: `This BYOL license is required for the installation and use of the Example Virtual Server Image.`

## Define your support experience
{: #vsimage-support}
{: step}

Provide details that help users understand how to get support if they encounter issues when they use the virtual server image. For more information about providing support information, see [Defining your support experience](/docs/sell?topic=sell-sw-support-details). 

To define your product's support experience, use the following steps:

{{site.data.content.steps-support-experience}}

## Next steps
{: #vsimage-define-next}

[Onboard and validate your Terraform template](/docs/sell?topic=sell-vsimage-onboard). 
