---

copyright:
  years: 2021, 2024

lastupdated: "2024-02-01"


keywords: onboard software, third-party software, sell on IBM Cloud, partner center, operator, validate, test, Red Hat OpenShift cluster, sample Node-RED Operator, CSV file, CSV, operator bundle

subcollection: sell

content-type: tutorial
services: Registry
account-plan: paid
completion-time: 45m

---

{{site.data.keyword.attribute-definition-list}}

# Onboarding your Operator
{: #operator-onboard}
{: toc-content-type="tutorial"}
{: toc-services="Registry"}
{: toc-completion-time="45m"}

This tutorial walks you through how to onboard a sample Node-RED Operator to your private catalog in {{site.data.keyword.cloud}}. You can onboard an Operator or Operator bundle by using a TGZ file. By completing this tutorial, you learn how to import the Operator, configure the deployment, license, and other details, and validate that the Operator can be installed on a Red Hat OpenShift cluster.
{: shortdesc}

## Before you begin
{: #operator-onboard-prereqs}

1. [Upload your Operator and application images to {{site.data.keyword.registrylong}}](/docs/Registry?topic=Registry-getting-started).
1. [Create your Red Hat OpenShift cluster](/docs/openshift?topic=openshift-getting-started).
1. Upload your source code to your repository.

    Use the [latest release of the sample Node-RED Operator](https://github.com/IBM-Cloud/operator-bundle-sample/releases){: external} as an example of how to set up your directory structure.
    {: tip}

1. Make sure you're assigned the {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) editor role on the Catalog Management and Partner Center - Sell services. See [Assigning access to account management services](/docs/account?topic=account-account-services) for more information.

For Operator bundles, you also need the following {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) roles.

* Administrator on all account management services and all IAM services
* Editor on the software instance service
* Editor on the {{site.data.keyword.registrylong_notm}} service
* Administrator on the {{site.data.keyword.openshiftshort}} cluster

Make sure that you use the same account to access {{site.data.keyword.registrylong_notm}} and to create the {{site.data.keyword.openshiftshort}} cluster.
{: important}

## Import your Operator
{: #operator-onboard-import}
{: step}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My products**.
1. Select the product that you're onboarding.
1. From the Software tab, click **Import a version**.
1. Choose **Operator from GitHub repository** as your deployment method.
1. Confirm that **Public repository** is set as the repository type.
1. Enter `https://github.com/IBM-Cloud/operator-bundle-sample/archive/refs/tags/v0.0.3.tar.gz` as your source URL.

1. Enter the software version in the format of major version, minor version, and revision, for example, `1.0.0`.

   Enter the version of your software and not the version of your Operator. For example, you might be using Operator version 1.3.0 to install software version 3.1.1.
   {: important}

1. Click **Add version**.

## Review your version details
{: #operator-review-version}
{: step}

From the Configure version tab, you can review your version details. After you review your version details, click **Next**.

## Set an image pull secret
{: #operator-image-pull-secret}
{: step}

When you create your {{site.data.keyword.openshiftlong}} cluster, the cluster includes an IAM service ID that is given reader access to {{site.data.keyword.registrylong_notm}}. The service ID credentials are authenticated in a nonexpiring service ID API key that is stored in image pull secrets in your cluster. As part of configuring the deployment details, you set a pull secret that's used to access and pull your images from the private {{site.data.keyword.registrylong_notm}} repository.

1. From the Set an image pull secret section, click **Add image pull secret**.
1. Enter the name and value of the image pull secret.
1. Click **Update**.
1. From the **Image pull secret name** list, select the image pull secret that you just added.
1. Click **Next**.


## Set the license requirements
{: #operator-onboard-cfg-license}
{: step}

If users are required to accept any license agreements beyond the {{site.data.keyword.cloud_notm}} Services Agreement, provide the URL to each agreement.

1. From the Add license agreements tab, click **Add license**.
2. Enter the name and URL, and click **Add license**.
3. After you enter all additional license agreements, click **Next**.

## Review your readme file
{: #operator-onboard-review-readme}
{: step}

When users install the software, they can view product information by clicking the Readme file link. This information is generated from the readme file that you uploaded to your source repository.

1. From the Edit readme tab, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit").
2. Preview how the information in the readme file is displayed to users when they install the Operator.
3. If you need to make changes, edit the information in the source code and import the updated code file to your private catalog.
4. Click **Save**.
5. Click **Next**.

## Validate the software version
{: #operator-onboard-validate}
{: step}

1. From the Validate product tab, select the target cluster and project, and click **Next**.
1. Configure your Schematics workspace by entering the name of your workspace, selecting a resource group, selecting a Schematics region, and optionally adding tags. Then, click **Next**.

    You can accept the default options that are displayed for your workspace name and resource group.
    {: note}

1. Click **Validate**.

{{site.data.content.manage-compliance}}

## Review requirements
{: #operator-review-reqs}

You must complete validation and any other requirements to publish your operator.

## Next steps
{: #operator-onboard-next}

Go to Partner Center and submit your request to publish your Operator to the {{site.data.keyword.cloud_notm}} catalog.
