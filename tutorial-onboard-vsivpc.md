---

copyright:
  years: 2023, 2024

lastupdated: "2024-04-24"


keywords: onboard software, third-party software, sell on IBM Cloud, partner center, virtual server image, virtual machine image, image, vm, vsi, validate, test, VSI image, VM image, vpc, virtual private cloud

subcollection: sell

content-type: tutorial
services: cloud-object-storage, vpc
account-plan: paid
completion-time: 45m

---

{{site.data.keyword.attribute-definition-list}}


# Onboarding a virtual server image for VPC to a private catalog
{: #vsivpc-onboard}
{: toc-content-type="tutorial"}
{: toc-services="cloud-object-storage, vpc"}
{: toc-completion-time="45m"}

This tutorial walks you through how to onboard a public virtual server image for virtual private cloud (VPC) to a private catalog. By completing this tutorial, you learn how to import the virtual server image, add your license agreements, edit your readme file, and validate that you can deploy the image to a target {{site.data.keyword.vpc_full}} (VPC).
{: shortdesc}

This tutorial is one of four in a series that demonstrates how to onboard and publish a sample virtual server image for VPC to {{site.data.keyword.cloud}}. As you complete the tutorial, adapt each step to fit your product's needs.

## Before you begin
{: #vsivpc-onboard-prereqs}

1. Virtual server images for VPC must first be imported and validated in your VPC. If your virtual server image is already imported and validated in your VPC, you can skip these steps:
   1. Create your [VPC](/docs/vpc?topic=vpc-getting-started).
   1. Create an instance of [{{site.data.keyword.cloud_notm}} Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-getting-started-cloud-object-storage) and upload your image to a bucket.
   1. [Import and validate](/docs/vpc?topic=vpc-importing-custom-images-vpc&interface=ui) your custom image in your VPC. Do this for each region in which you want your software to be available and verify that the SHA or checksum matches for the imported image in each region.
1. Make sure you're assigned the {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) editor role on the Catalog Management and Partner Center - Sell services. See [Assigning access to account management services](/docs/account?topic=account-account-services) for more information.
1. Complete the previous tutorials in the series: [Registering a virtual server image for VPC in Partner Center](/docs/sell?topic=sell-vsivpc-register) and [Defining the product details of a virtual server image for VPC](/docs/sell?topic=sell-vsivpc-define).

## Import the virtual server image to your private catalog
{: #vsivpc-onboard-import}
{: step}

Complete the following steps to import your virtual server image to a private catalog, which was created for you when you registered the virtual server image in {{site.data.keyword.cloud_notm}} Partner Center.

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My products**.
1. Select your product.
1. From the Software page, click **Import a version**.
1. Select **Virtual server image for VPC** as your delivery method.
1. Select the image architecture.
1. Select the region where your image is available.
1. Select the image that you'd like to add.
1. Enter the software version, for example, `1.0.0`.
1. Click **Add version**.

## Review regions
{: #vsivpc-review-regions}
{: step}

From the Configure version tab, you can add an image from another region, or remove an image from a particular region. To add an image from another region, complete the following steps:

1. Click **Add region**.
1. Select the region to where you want to add your image.
1. Click **Add region**.
1. Click **Next**.

To remove an image from a particular region, complete the following steps:

1. Select the image that you want to remove.
1. Click **Delete**, then click **Yes**.
1. Click **Next**.

## Review the version details
{: #vsivpc-review-version}
{: step}

On the Configure version tab, you can also review your version details. After you review your version details, click **Next**.

## Add your license agreements
{: #vsivpc-onboard-eula}
{: step}

If users are required to accept any license agreements beyond the {{site.data.keyword.cloud_notm}} Services Agreement, provide the URL to each agreement.

1. From the Add license agreements page, click **Add license**.
1. Enter the name and URL, and click **Add license**.
1. Enter all additional license agreements, and click **Next**.

## Edit your readme file
{: #vsivpc-onboard-readme}
{: step}

Use the [readme file template](/media/docs/downloads/software/sw-readme-tab-template.md){: external} to document the instructions for installing your software. For the purposes of this tutorial, the following steps describe how to edit the description of the readme file.

1. Click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit").
1. Copy and paste the contents of the [readme file template](/media/docs/downloads/software/sw-readme-tab-template.md){: external} and make updates as needed.
1. Click **Save** > **Next**.

## Validate the virtual server image
{: #vsivpc-onboard-validate}
{: step}

Validating your virtual server image involves running a test deployment of your software. Validating your image proves that it's provisionable with your VPC. The first image that you added to your product is validated. Other regions are not included in this validation.

1. Configure the validation target by selecting a VPC, an SSH key, a subnet, and a profile. Then, click **Next**.
1. Optionally, configure the Schematics workspace by specifying a name and selecting a resource group and a Schematics region. Then, click **Next**.

   In the **Tags** field, you can enter a name of a specific tag to attach to your virtual server image. Tags provide a way to organize, track usage costs, and manage access to the resources in your account.
   {: tip}

1. In the Validation version section, select **I have read and agree to the end user license agreements**.
1. Click **Validate**.
1. Click **Next**.

{{site.data.content.manage-compliance}}

## Review requirements
{: #vsivpc-review-reqs}

Complete validation and any other requirements to publish your virtual server image.

## Next steps
{: #vsivpc-onboard-next}

Go to Partner Center and submit your request to [publish your virtual server image](/docs/sell?topic=sell-vsivpc-publish) to the {{site.data.keyword.cloud_notm}} catalog.
