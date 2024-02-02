---

copyright:
  years: 2021, 2024
lastupdated: "2024-02-02"

keywords: onboard software, third-party software, sell on IBM Cloud, partner center, operator, validate, test, sample Red Hat OpenShift operator, operator bundle

subcollection: sell

content-type: tutorial
services: Registry
account-plan: paid
completion-time: 45m

---

{{site.data.keyword.attribute-definition-list}}

# Onboarding your Operator bundle
{: #bundle-onboard}
{: toc-content-type="tutorial"}
{: toc-services="Registry"}
{: toc-completion-time="45m"}

This tutorial walks you through how to onboard a Certified Operator bundle from a {{site.data.keyword.redhat_notm}} registry. By completing this tutorial, you learn how to import the {{site.data.keyword.openshiftshort}} Operator bundle, configure the deployment, license, and other details, and validate that the Operator bundle can be installed on a cluster.
{: shortdesc}

This tutorial is one of four in a series that demonstrates how to onboard and publish a sample Operator bundle from the {{site.data.keyword.openshiftshort}} Certified registry. It uses a fictitious company called *Example Corp*. As you complete the tutorial, adapt each step to fit your product's needs.


## Before you begin
{: #bundle-onboard-prereqs}

1. Go to {{site.data.keyword.redhat_notm}} OperatorHub to confirm that your Operator bundle exists in the {{site.data.keyword.redhat_notm}} Certified registry.
1. [Create your {{site.data.keyword.openshiftshort}} cluster](/docs/openshift?topic=openshift-getting-started).
1. [Upload your Operator bundle and application images to {{site.data.keyword.registrylong_notm}}](/docs/Registry?topic=Registry-getting-started).
1. Verify that you're assigned the correct roles. For more information, see [Assigning access to account management services](/docs/account?topic=account-account-services) and [Managing access to resources](/docs/account?topic=account-assign-access-resources).
   * Administrator on all account management services and all IAM services
   * Editor on the catalog management service
   * Editor on the {{site.data.keyword.registrylong_notm}} service
   * Administrator on the {{site.data.keyword.openshiftshort}} cluster
   * Editor on the software instance service

Make sure that you use the same account to access {{site.data.keyword.registrylong_notm}} and to create the {{site.data.keyword.openshiftshort}} cluster.
{: important}

## Import your Operator bundle
{: #bundle-onboard-import}
{: step}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My products**.
1. Select the product that you're onboarding.
1. From the Software tab, click **Import a version**.
1. Select **Operator from {{site.data.keyword.redhat_notm}} registry** as your deployment method.
1. Select **Certified** as your {{site.data.keyword.redhat_notm}} repository.
1. Select your Operator bundle. For example, for the purposes of this tutorial, you can select **Akka Cluster Operator** as your Operator.
1. Select the Operator bundle version that you want to import.
1. Enter the software version that the Operator bundle installs in the format of major version, minor version, and revision. For example, you can use Operator version `1.1.0` to install software version `3.1.1`.
1. Review the summary of your Operator bundle.
1. Click **Add version**.

## Review your version details
{: #bundle-configure}
{: step}

From the Configure version tab, you can review your version details. After you review your version details, click **Next**.

## Set the license requirements
{: #bundle-onboard-cfg-license}
{: step}

If users are required to accept any license agreements beyond the {{site.data.keyword.cloud_notm}} Services Agreement, provide the URL to each agreement.

1. From the Add license agreements tab, click **Add license**.
2. Enter the name and URL, and click **Add license**.
3. Enter all additional license agreements, and  click **Next**.

## Review your readme file
{: #bundle-onboard-review-readme}
{: step}

When users install the software, they can view product information by clicking the Readme file link. This information is generated from the readme file that you uploaded to your source repository.

1. From the Edit readme tab, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit").
2. Preview how the information in the readme file will be displayed to users when they are installing the Operator bundle.
3. If you need to make changes, edit the information in the source file and import the updated Operator bundle to your private catalog.
4. Click **Save** > **Next**.

## Validate the software version
{: #bundle-onboard-validate}
{: step}

Before you can publish the Operator bundle, you need to validate it to make sure that the version can be deployed to the intended target.

1. From the **Validate product** tab, select the Update channel that you would like to receive updates from.
1. Select whether you want to apply updates automatically or manually.
1. Select a {{site.data.keyword.openshiftshort}} cluster.
1. Select a project.
1. Click **Next**.
1. Confirm or edit your workspace name.
1. Select a resource group.
1. Select a Schematics region.
1. Enter tags for your workspace.
    Tags provide a way to organize, track usage costs, and manage access to the resources in your account.
    {: tip}

1. Click **Next** > **Validate**.

{{site.data.content.manage-compliance}}

## Review requirements
{: #bundle-review-reqs}

You must complete validation and any other requirements to publish your bundle.

## Next steps
{: #bundle-onboard-next}

Go to Partner Center and submit your request to [publish your Operator bundle](/docs/sell?topic=sell-bundle-publish) to the {{site.data.keyword.cloud_notm}} catalog.
