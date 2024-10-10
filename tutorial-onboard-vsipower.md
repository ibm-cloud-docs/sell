---

copyright:
  years: 2022, 2024

lastupdated: "2024-04-22"


keywords: onboard software, Terraform, third-party software, sell on IBM Cloud, partner center, virtual server image, virtual machine image, image, vm, vsi, validate, test, VSI image, VM image, power, power vsi, power systems virtual server

subcollection: sell

content-type: tutorial
services: cloud-object-storage, vpc
account-plan: paid
completion-time: 45m

---

{{site.data.keyword.attribute-definition-list}}


# Onboarding a virtual server image for Power Systems to a private catalog
{: #vsipower-onboard}
{: toc-content-type="tutorial"}
{: toc-services="cloud-object-storage, vpc"}
{: toc-completion-time="45m"}

This tutorial walks you through how to onboard a public virtual server image for {{site.data.keyword.powerSys_notm}} to a private catalog. By completing this tutorial, you learn how to import the virtual server image from a GitHub repository, configure the deployment and other details, and validate that you can deploy the image to a target {{site.data.keyword.powerSys_notm}} instance.
{: shortdesc}

This tutorial demonstrates how to onboard and publish a [sample virtual server image for Power Systems Virtual Server](https://github.com/IBM-Cloud/isv-power-vsi-product-deploy-sample){: external} to {{site.data.keyword.cloud}}. As you complete the tutorial, adapt each step to fit your product's needs.

This tutorial includes deploying the virtual server image to a target {{site.data.keyword.powerSys_notm}}. As a result, you will incur associated {{site.data.keyword.cloud_notm}} infrastructure charges.
{: note}

## Before you begin
{: #vsipower-onboard-prereqs}

1. Create your {{site.data.keyword.powerSys_notm}} instance [and convert it into a public image](/docs/power-iaas?topic=power-iaas-virtual-appliances#onboard-vsi).
1. After your image is converted into a public image, create your [Terraform template](/docs/schematics?topic=schematics-create-tf-config).
1. Upload your Terraform template and readme file to your [GitHub repository](https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/tree/main#upload-your-terraform-template-to-a-github-release){: external}.

   Use the latest release of the [sample code](https://github.com/IBM-Cloud/isv-power-vsi-product-deploy-sample ){: external} as an example of how to set up your repository.
   {: tip}

1. Make sure you're assigned the {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) editor role on the Catalog Management and Partner Center - Sell services. For more information, see [Assigning access to account management services](/docs/account?topic=account-account-services).
1. Complete the previous tutorials in the series: [Registering a virtual server image for Power Systems in the Partner Center](/docs/sell?topic=sell-vsipower-register) and [Defining the product details of a virtual server image for Power Systems](/docs/sell?topic=sell-vsipower-define).

## Import the virtual server image to your private catalog
{: #vsipower-onboard-import}
{: step}

Complete the following steps to import your virtual server image from your GitHub repository to a private catalog, which was created for you when you registered the virtual server image in {{site.data.keyword.cloud_notm}} Partner Center.

You can onboard only stock virtual server images for {{site.data.keyword.powerSys_notm}}.
{: important}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My products**.
1. Select your product.
1. From the Software page, click **Import a version**.
1. Select **Virtual server image for Power Systems** as your deployment method.
1. Confirm that **Public repository** is selected as the repository type.
1. Click **Virtual server image for Power Systems** to populate the **Source URL** field.

    Alternatively, you can copy and paste `https://github.com/IBM-Cloud/isv-power-vsi-product-deploy-sample` in the field.

1. Enter `1.0.0` as the software version.
1. Click **Add version**.
1. Click the name of your product.
1. In Catalog entry details, verify that the Delivery method is set to **Power VSI**.
    If **Power VSI** is not selected as the Delivery method, click **Edit** and select **Power VSI** as the Delivery method, then click **Save**.

## Review the version details
{: #vsipower-review-version}
{: step}

From the Configure product tab, you can review your version details. When you are ready to move on, click **Next**.


## Configure the deployment values
{: #vsipower-onboard-cfgdeploy}
{: step}

After you review the version details, you're ready to configure the deployment values.

1. If you need to specify the Terraform runtime version that you want Schematics to use, click the **Override the default Terraform runtime version** checkbox and enter a version.
1. From the Configure the deployment details section, click **Add deployment values**.
1. Select the **Parameter** checkbox to select all options, and click **Add**.
1. To customize which parameters are required for users to specify during the installation and which ones are hidden from users altogether, select a parameter and click **Edit**. Mark the checkboxes to configure the values and click **Save**. For the purposes of this tutorial, configure each parameter as described in the following table.

| Parameter | Description | Required for users to specify? | Hidden from users? |
| --- | ---------- | --- | --- |
| **`crn`** | The {{site.data.keyword.powerSys_notm}} CRN | True | False |
| **`instance_name`** | The name of the virtual server instance. | True | False |
| **`memory`** | The amount of memory that you want to assign to your instance in gigabytes. | False | False |
| **`network_name`** | The network ID or name to assign to the instance, as defined for the selected {{site.data.keyword.powerSys_notm}} CRN. | True | False |
| **`processor_type`** | The type of processor mode in which the VM will run. Specify `shared`, `capped`, or `dedicated`. | False | False |
| **`processors`** | The number of vCPUs to assign to the VM as visible within the guest OS. | False | False |
| **`ssh_key_name`** | The name of the public SSH RSA key to use when creating the instance, as defined for the selected {{site.data.keyword.powerSys_notm}} CRN. | True | False |
| **`sys_type`** | The type of system on which to create the VM: `s922`, `e880`, `e980`, `e1080`, or `s1022`. | False | False |
{: caption="Table 1. Deployment values for a virtual server image" caption-side="top"}

Next, update the configuration type of the **`crn`** and **`processors`** parameters:

1. From the Deployment values table, select the **`crn`** parameter and click **Edit**.
1. Open the **Value details** menu and select **Power Systems Virtual Server**.
1. Click **Save**.
1. From the Deployment values table, select the **`processors`** parameter and click **Edit**.
1. Open the **Value details** menu and select **float**.
1. Click **Next**.

{{site.data.content.output-values}}

{{site.data.content.define-IAM-access}}

## Add your license agreements
{: #vsipower-onboard-eula}
{: step}

If users are required to accept any license agreements beyond the {{site.data.keyword.cloud_notm}} Services Agreement, provide the URL to each agreement.

1. From the Add license agreements tab, click **Add license**.
2. Enter the name and URL, and click **Add license**.
3. Enter all additional license agreements, and click **Next**.

## Review your readme file
{: #vsipower-onboard-readme}
{: step}

The TGZ file that you imported to your private catalog includes a readme file that provides product information for the virtual server image. If you want to make updates to the readme file, you can edit it directly from your private catalog. For the purposes of this tutorial, the following steps describe how to edit the description of the readme file.

1. Click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit"), and update the description with the following sentence:

    `Create and deploy a virtual server with ease by using a custom image.`

1. Click **Save**.
1. Click **Next**.

## Validate the virtual server image
{: #vsipower-onboard-validate}
{: step}

Validate that you can deploy the virtual server image to your {{site.data.keyword.powerSys_notm}} instance.

1. From the Validate product tab, enter the name of your Schematics workspace, select a resource group, select a Schematics region, and click **Next**.

    In the **Tags** field, you can enter a name of a specific tag to attach to your virtual server image. Tags provide a way to organize, track usage costs, and manage access to the resources in your account.
    {: tip}

1. From the Deployment values section, review your parameter values, and click **Next**.
1. In the Validate product section, select **I have read and agree to the following license agreements**.
1. Click **Validate**.

    You can monitor the progress of the validation process by clicking **View logs**.
    {: tip}

{{site.data.content.manage-compliance}}

## Review requirements
{: #vsipower-review-reqs}

You must complete validation and any other requirements to publish your virtual server image.

## Next steps
{: #vsipower-onboard-next}



Go to the Partner Center and publish it to the catalog. For more information, see [Publishing a virtual server image to the {{site.data.keyword.cloud_notm}} catalog](/docs/sell?topic=sell-vsipower-publish).
