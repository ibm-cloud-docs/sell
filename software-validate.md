---


copyright:
  years: 2020, 2021

lastupdated: "2021-12-13"

keywords: software, third-party software, sellers, partners, validate, test, partner center

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Onboarding software to your private catalog
{: #sw-validate}

Onboarding your software includes importing a version to your private catalog, configuring the deployment details, setting any license requirements, and validating that the version can be successfully installed on the target infrastructure that you require. 
{: shortdesc}

## Before you begin
{: #sw-validate-prereqs}

1. Upload your source code to a release in your GitHub repository. See [Setting up your source code repository](https://docs.github.com/en/github/administering-a-repository/managing-releases-in-a-repository). 
2. Verify that you're using a Pay-As-You-Go or Subscription account. See [Viewing your account type](/docs/account?topic=account-account_settings#view-acct-type) for more information.
3. Make sure you're assigned the editor role on the catalog management service. See [Assigning access to account management services](/docs/account?topic=account-account-services).
4. Set up the test environment that was previously created for you:

* Install the {{site.data.keyword.cloud_notm}} CLI and the {{site.data.keyword.cloud_notm}} Schematics plug-in. See [Setting up the CLI](/docs/schematics?topic=schematics-setup-cli).
* Upload a readme file that contains your product installation instructions to your GitHub repository. See [Setting up your source code repository](/docs/sell?topic=sell-source-repo-setup).
* For containerized apps:
   * Create your [Kubernetes cluster](/docs/containers?topic=containers-getting-started) or [Red Hat OpenShift cluster](/docs/openshift?topic=openshift-getting-started).
   * For deployments to {{site.data.keyword.cloud_notm}} Kubernetes Service, [set up your Helm chart](/docs/containers?topic=containers-helm).
   * For deployments to Red Hat OpenShift, set up your [Helm chart](/docs/openshift?topic=openshift-helm) or [Operator](/docs/openshift?topic=openshift-operators).

* For virtual machine images:
   * Review the list of [supported images](/docs/vpc?topic=vpc-about-images).
   * Create your [Terraform template](/docs/schematics?topic=schematics-getting-started).
   * Create an instance of [{{site.data.keyword.cloud_notm}} Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-getting-started-cloud-object-storage) and add your image to a bucket.

## Importing a version to your private catalog
{: #sw-validate-add}

Complete the following steps to import a version of your software to your private catalog. Your private catalog was created for you as part of [Getting set up to sell software](/docs/sell?topic=sell-sw-getting-started). 

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My Products**. 
1. Select the product that you're onboarding.
1. From the Software tab, click **Import a version**.
1. Select your deployment method. 
1. Select whether you are adding your product from a private or public repository. For Operators, select your source repository and then choose private or public repository. 
1. Enter your source URL. 

    If you're importing a version from a public repository, you can review the following list of supported formats per software type:

    * Helm chart: `https://charts.bitnami.com/ibm/apache-8.3.2.tgz`
    * Node-RED Operator: `https://github.com/IBM-Cloud/operator-bundle-sample/archive/refs/tags/v0.0.3.tar.gz`
    * Operator bundle from a {{site.data.keyword.redhat_notm}} {{site.data.keyword.openshiftshort}} registry: For an example, select the `Akka Cluster Operator` from the list of available Operators in the Certified repository.
    * OVA image: `https://github.com/gcatalog/OVA-sample/blob/main/ova-sample.yaml`
    * Terraform template: `https://github.com/IBM-Cloud/terraform-sample/releases/tag/v1.0.0`
    * Virtual server image with Terraform: `https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/releases/download/v1.0/isv-vsi-product-deploy-sample.tar.gz`
  
    If you're adding your product from a private repository, you can choose to provide a personal access token or you can use a secret. Instead of giving users a personal access token, you can give them access to a secret, add the token to a secret, and centrally manage all tokens and access the secret allows.

    * If you're using a personal access token, select **No** to indicate that you aren't using a secret and provide your personal access token.
    * If you're using a secret, select **Yes** and click **Select from Secrets Manager**. Select your service instance, secret group, and secret. If you don't see your secret, make sure you're using the correct secret group and service instance.
    
    The message `No service instance available` might be displayed if you haven't created a secret or if you don't have the correct access to use secrets, even if you have service instances that are created. 
    {: note}

1. If applicable, set your deployment target and add your software version. 
1. Click **Add version**. 

## Configuring the product details
{: #sw-validate-cfg-deploy}

1. From the version list, click the row that contains your software. 
1. Review the version details, and click **Next**.
1. Depending on your software type, there may be additional steps, including setting deployment values. 
1. Click **Next**. 

### Setting deployment values
{: #sw-set-values}

If applicable to your software type, you can set deployment values that users are required to specify when they install the software. You can add new deployment values or import deployment values from an existing version. 

#### Adding new deployment values
{: #sw-add-values}

1. Click **Configure version** > **Next**. 
1. Click **Add deployment values**.
1. In the table, select **Parameter** > **Add**.
1. To customize parameters, select a parameter and click **Edit**.

#### Importing existing values
{: #sw-import-values}

You can import existing values if you previously set deployment values for an existing version and want to import the values to your current version. 

Imported values don't replace any deployment values that you already added to your current version. 
{: important}

1. Click **Configure version** > **Next**. 
1. Click **Add deployment values**.
1. Click **Import values from a previous version**.
1. Select the version that contains the values that you want to import.
1. Click **Import**.
1. To customize parameters, select a parameter and click **Edit**.

## Adding license agreements
{: #sw-validate-add-license}

If users are required to accept any license agreements beyond the {{site.data.keyword.cloud_notm}} Services Agreement when they install the software, provide the URL to each agreement or import licenses from an existing version. 

### Adding new license agreements
{: #sw-add-new-license}

1. Click **Add license agreements** > **Add license**. 
2. Enter the name and URL, and click **Add license**.
3. After entering all additional license agreements, click **Next**.

### Importing license agreements 
{: #sw-import-license}

You can import existing license agreements if you previously set license agreements for an existing version and want to import the licenses to your current version. 

Imported licenses don't replace any license agreements that you already added to your current version. 
{: important}

1. Click **Add license agreements** > **Add license**. 
1. Click **Import licenses from a previous version**.
1. Select the version that contains the licenses that you want to import.
1. Click **Import**.

## Reviewing your readme file
{: #sw-validate-readme-review}

When users access your software from the catalog, they can view installation instructions from the Readme tab of your product's catalog details page. The information on the Readme tab is generated from the readme file that you uploaded to your GitHub repository. 

1. From the Edit readme tab, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit").
2. Preview how the information in the readme file will be displayed to users when they are installing the software.
3. To make updates, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit") next to the Readme section title.
4. Click **Save**.
5. Click **Next**.


## Validating the product
{: #sw-validate-validate-product}

The steps to validate your product can vary based on the type of software that you're onboarding. 

1. From the Validate product tab, configure your validation target, and click **Next**. This step applies only to Helm charts and Operators. 
1. Configure your workspace, and click **Next**. This step applies only to Helm charts, Operators, Terraform templates, and virtual server images with Terraform. 
1. Click **Validate**.  

To monitor the progress of the validation process, click **View logs**.
{: tip}

