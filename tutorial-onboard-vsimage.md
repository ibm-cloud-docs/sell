---

copyright:
  years: 2021, 2022

lastupdated: "2022-04-01"


keywords: onboard software, Terraform, third-party software, sell on IBM Cloud, partner center, virtual server image, virtual machine image, image, vm, vsi, validate, test, VSI image, VM image

subcollection: sell

content-type: tutorial
services: cloud-object-storage, vpc
account-plan: paid
completion-time: 45m 

---

{{site.data.keyword.attribute-definition-list}}


# Onboarding a virtual server image with Terraform to a private catalog
{: #vsimage-onboard}
{: toc-content-type="tutorial"}
{: toc-services="cloud-object-storage, vpc"} 
{: toc-completion-time="45m"} 

This tutorial walks you through how to onboard a virtual server image with Terraform to a private catalog. By completing this tutorial, you learn how to import the virtual server image from a GitHub repository, configure the deployment and other details, and validate that you can deploy the image to a target {{site.data.keyword.vpc_full}} (VPC). 
{: shortdesc}

This tutorial is one of four in a series that demonstrates how to onboard and publish a [sample virtual server image with Terraform](https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/tree/v1.0){: external} to {{site.data.keyword.cloud}}. As you complete the tutorial, adapt each step to fit your product's needs.

This tutorial includes deploying the virtual server image to a target VPC. As a result, you will incur associated {{site.data.keyword.cloud_notm}} infrastructure charges. 
{: note}

## Before you begin
{: #vsimage-onboard-prereqs}

1. Create an instance of [{{site.data.keyword.cloud_notm}} Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-getting-started-cloud-object-storage) and upload your image to a bucket.
2. Create your [VPC](/docs/vpc?topic=vpc-getting-started). 
3. [Import your custom image to all regions](https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/tree/main#import-your-custom-image-to-all-supported-regions){: external} in which you want your software to be available. 
4. Create your [Terraform template](/docs/schematics?topic=schematics-create-tf-config). 
5. [Upload your Terraform template and readme file to your GitHub repository](https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/tree/main#upload-your-terraform-template-to-a-github-release){: external}. 

   Use the [latest release of the sample Terraform code](https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/releases/tag/v1.0 ){: external} as an example of how to set up your repository.
   {: tip}
   
6. Make sure you're assigned the {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) editor role on the Catalog Management and Partner Center - Sell services. See [Assigning access to account management services](/docs/account?topic=account-account-services) for more information.
7. Complete the previous tutorials in the series: [Registering a virtual server image in the Partner Center](/docs/sell?topic=sell-vsimage-register) and [Defining the product details of a virtual server image](/docs/sell?topic=sell-vsimage-define). 

## Import the virtual server image to your private catalog
{: #vsimage-onboard-import}
{: step}

Complete the following steps to import your virtual server image from your GitHub repository to a private catalog, which was created for you when you registered the virtual server image in {{site.data.keyword.cloud_notm}} Partner Center.

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My Products**. 
1. Select your product. 
1. From the Software tab, click **Import a version**.
1. Select **Virtual server image with Terraform** as your deployment method. 
1. Confirm that **Public repository** is selected as the repository type.
1. Click **Virtual server image with Terraform** to populate the **Source URL** field.
1. Enter `1.0.0` as the software version. 
1. Click **Add version**.
1. Click the name of your product. 
1. Click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit"). 
1. Confirm that the Delivery method is set to **VPC VSI**.
1. Click **Save**.

## Review the version details
{: #vsi-review-version}
{: step}

From the Configure product tab, you can review your version details. There are no actions that you need to take. When you are ready to move on, click **Next**.

## Configure the deployment values
{: #vsimage-onboard-cfgdeploy}
{: step}

After you review the version details, you're ready to configure the deployment values.

1. From the Configure the deployment details section, click **Add deployment values**. 
1. Select **Parameter** to select all options, and click **Add**.
1. To customize which parameters are required for users to specify during the installation and which ones are hidden  altogether, select a parameter and click **Edit**. For the purposes of this tutorial, configure each parameter as described in the following table.

| Parameter | Description | Required for users to specify? | Hidden from users? |
| --- | ---------- | --- | --- | 
| **`TF_VERSION`** | The version of the Terraform engine that's used in the Schematics workspace. | False | True |
| **`region`** | The region in which the Virtual Private Cloud (VPC) instance is located. | True | False |
| **`ssh_key_name`** | The name of the public SSH key to use when creating the virtual server instance. | True | False |
| **`subnet_id`** | The ID of the subnet within the VPC that the virtual server instance uses. | True | False |
| **`vsi_instance_name`** | The name of the virtual server instance. | True | False |
| **`vsi_profile`** | The profile of the compute CPU and memory resources to use when creating the virtual server instance. | True | False |
| **`vsi_security_group`** | The name of the security group that is created. | True | False |
{: caption="Table 1. Deployment values for a virtual server image" caption-side="top"} 

Next, update the configuration type of the **`region`** parameter:

1. From the Deployment values table, select the **`region`** parameter and click **Edit**.
1. Open the **Value details** menu and select **VPC region**.
1. Click **Save** > **Next**.

## Add your license agreements
{: #vsimage-onboard-eula}
{: step}

Provide the URLs to the license agreements that users are required to accept when they install the product. The license agreements are in addition to the {{site.data.keyword.cloud_notm}} Services Agreement.

1. Click **Add license agreements** > **Add license**. 
2. Enter the name and URL, and click **Update**.
3. After you enter all additional license agreements, click **Next**.

## Review your readme file 
{: #vsimage-onboard-readme}
{: step}

The TGZ file that you imported to your private catalog includes a readme file that provides instructions for installing the virtual server image. If you want to make updates to the readme file, you can edit it directly from your private catalog. For the purposes of this tutorial, the following steps describe how to edit the description of the readme file.

1. Click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit"), and update the description with the following sentence:

    `Create and deploy a virtual server with ease by using a custom image.`

1. Click **Save** > **Next**.

## Manage security and compliance controls
{: #vsimage-onboard-controls}
{: step}

Controls are safeguards that are used to meet security and compliance requirements. Any applicable controls that are included in your readme file are listed in the Security and compliance controls table. You can add controls that are not included in your readme file. 

1. Click **Add controls**. 
1. Choose a profile. 
1. Select the controls that you want to add to your version. 
1. Click **Add** 
1. Click **Next**.

## Validate the virtual server image 
{: #vsimage-onboard-validate}
{: step}

Validate that you can deploy the virtual server image to your VPC. 

1. From the Validate product tab, enter the name of your Schematics workspace, select a resource group, select a Schematics region, and click **Next**.

    In the **Tags** field, you can enter a name of a specific tag to attach to your virtual server image. Tags provide a way to organize, track usage costs, and manage access to the resources in your account.
    {: tip}
  
1. From the Deployment values section, review your parameter values, and click **Next**.
1. In the Validate product section, select **I have read and agree to the following license agreements**. 
1. Click **Validate**.

    You can monitor the progress of the validation process by clicking **View logs**.
    {: tip}

## Next steps
{: #vsimage-onboard-next}

The virtual server image isn't yet publicly available to other accounts. Use a REST API to make the image public so that users can use it to create virtual server instances. For more information, see [Update the visibility of your image](https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample#update-the-visibility-of-your-image-patch-api){: external}.

After you make the virtual server image public, you can return to the Partner Center and publish it to the catalog. For more information, see [Publishing a virtual server image to the {{site.data.keyword.cloud_notm}} catalog](/docs/sell?topic=sell-vsimage-publish).

