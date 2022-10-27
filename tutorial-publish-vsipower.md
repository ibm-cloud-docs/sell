---

copyright:
  years: 2022
lastupdated: "2022-03-31"

keywords: onboard software, third-party software, sell on IBM Cloud, partner center, virtual server image, virtual machine image, image, vm, vsi, publish, Terraform, tutorial, sample

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 30m

---

{{site.data.keyword.attribute-definition-list}}


# Publishing a virtual server image for Power Systems to the {{site.data.keyword.cloud_notm}} catalog
{: #vsipower-publish}
{: toc-content-type="tutorial"}
{: toc-completion-time="30m"}

This tutorial walks you through how to publish a virtual server image with Terraform to {{site.data.keyword.cloud}}. By completing this tutorial, you submit your publishing request, respond to any review feedback, and then publish the virtual server image to the {{site.data.keyword.cloud_notm}} catalog.
{: shortdesc}

This tutorial is one of four in a series that demonstrates how to onboard and publish a [sample virtual server image for Power Systems Virtual Server](https://github.com/IBM-Cloud/isv-power-vsi-product-deploy-sample){: external}. As you complete the tutorial, adapt each step to fit your product's needs.

## Before you begin
{: #vsipower-publish-prereqs}

1. [Register a virtual server image](/docs/sell?topic=sell-vsipower-register).
1. [Define your product details](/docs/sell?topic=sell-vsipower-define).
1. [Onboard the virtual server image](/docs/sell?topic=sell-vsipower-onboard).
1. [Update the visibility of the virtual server image](https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample#update-the-visibility-of-your-image-patch-api){: external}.

## Submit your publishing request
{: #vsipower-request-publish}
{: step}

The details of any third-party software must be reviewed by {{site.data.keyword.cloud_notm}} before it can be published to the catalog. Complete the following steps to submit a request to publish your virtual server image:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My Products**.
1. Select your virtual server image.
1. From the Onboarding checklist, click **Request Approval**.
1. Select the version > **I affirm that my company is authorized to use all materials**.
1. Click **Request Approval**.

At this point, your publishing request is reviewed by {{site.data.keyword.cloud_notm}} to ensure the required details, such as the product name, catalog entry, product page, pricing model, and support experience are complete and accurate. When your request is approved, you receive an email notifying you that you can publish your product to the catalog.

If updates are required, you'll receive a separate email with details about the required updates. After you address all review feedback, you can submit another publishing request.
{: note}

## Publish the virtual server image
{: #vsipower-publish-submit}
{: step}

1. Navigate to the Partner Center in the {{site.data.keyword.cloud_notm}} console by clicking the link in the email that you received notifying you that your publishing request was approved.
1. Click **Publish to catalog**.

## Next steps
{: #vsipower-publish-next}

Verify that the virtual server image is officially live in the catalog for all users. Go to the [catalog](https://cloud.ibm.com/catalog){: external}, select **Type** > **Software**, and search for the name of your virtual server image.
