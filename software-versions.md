---


copyright:
  years: 2021
lastupdated: "2021-12-02"

keywords: software, third-party software, sellers, partners, versions, test, partner center, version

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}


# Adding a new version of software
{: #add-version-software}

After onboarding your software, you can add multiple versions of your software to your private catalog.
{: shortdesc}

## Adding a version of a Helm chart
{: #add-version-helm}

The following steps are for adding a new version. If you want to deploy your existing version to a new target, see [Deploying a Helm chart to a new target](/docs/sell?topic=sell-helm-target-new).

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My Products**.
1. Select your product, and select **Software**. 
1. Click **Import a version**.
1. Select **Helm chart** as your deployment method. 
1. Indicate whether your repository type is private or public. 
1. Enter your source url. 
1. Choose your deployment target. 
1. Review the **Summary**. 
1. Click **Add version**. 

To complete the validation process, see [Configure the product details](/docs/sell?topic=sell-sw-validate#sw-validate-cfg-deploy).

## Adding a version of Terraform
{: #add-version-terraform}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My Products**.
1. Select your product, and select **Software**. 
1. Click **Import a version**.
1. Select **Terraform** as your deployment method. 
1. Indicate whether your repository type is private or public. 
1. Enter your source url. 
1. Enter your software version in the format of major version, minor version, and revision, for example, 1.0.0.
1. Review the **Summary**. 
1. Click **Add version**. 

To complete the validation process, see [Configure the product details](/docs/sell?topic=sell-sw-validate#sw-validate-cfg-deploy).

## Adding a version of an Operator from your own repository
{: #add-version-operator-own}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My Products**.
2. Select your product, and select **Software**. 
3. Click **Import a version**.
4. Select **Operator** as your deployment method. 
5. In the source repository menu, select **Import from your repository**.
6. Indicate whether your repository type is private or public. 
7. Enter your source url. 
8. Enter your software version in the format of major version, minor version, and revision, for example, 1.0.0.

   Enter the version of your software and not the version of your operator. For example, you can use operator version 1.3.0 to install software version 3.1.1. The software version field is asking for version number 3.1.1.
   {: important}

9. Review the **Summary**. 
10. Click **Add version**. 

To complete the validation process, see [Configure the product details](/docs/sell?topic=sell-sw-validate#sw-validate-cfg-deploy).

## Adding a version of an Operator from a Red Hat registry
{: #add-version-operator-index}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My Products**.
1. Select your product. 
1. In Software, click **Import a version**.
1. Select **Operator from Red Hat registry** as your deployment method. 
1. Select the Red Hat repository.
1. Select the Operator bundle.
1. Choose the Operator version from the list of available versions in the repository.  
1. Enter the software version that the Operator bundle installs in the format of major version, minor version, and revision. For example, you can use Operator version `1.1.0` to install software version `3.1.1`. 
1. Review the summary of your Operator bundle. 
1. Click **Add version**.

To complete the validation process, see [Configure the product details](/docs/sell?topic=sell-sw-validate#sw-validate-cfg-deploy).

## Adding a version of an OVA image
{: #add-version-ova}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My Products**.
1. Select your product. 
1. In Software, click **Import a version**.
1. Select **OVA image** as your deployment method. 
1. Indicate whether your repository type is private or public. 
1. Enter your source url. 
1. Review the **Summary**. 
1. Click **Add version**. 

To complete the validation process, see [Configure the product details](/docs/sell?topic=sell-sw-validate#sw-validate-cfg-deploy).

## Adding a version of a virtual server image with Terraform
{: #add-version-vsi}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My Products**.
1. Select your product. 
1. In Software, click **Import a version**.
1. Select **Virtual server image with Terraform** as your deployment method. 
1. Indicate whether your repository type is private or public. 
1. Enter your source url. 
1. Enter your software version in the format of major version, minor version, and revision, for example, 1.0.0.
1. Review the **Summary**. 
1. Click **Add version**. 
1. Click the name of your product. 
1. Click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit"). 
1. Select **This Terraform template contains at least one virtual server image.**
1. Click **Save**.

To complete the validation process, see [Configure the product details](/docs/sell?topic=sell-sw-validate#sw-validate-cfg-deploy).
