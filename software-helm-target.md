---

copyright:
  years: 2020, 2023
lastupdated: "2023-10-19"

keywords: onboard software, third-party software, Helm chart, software, partner, sellers, deploy, partner center, target, deployment target

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}


# Deploying a Helm chart to a new target
{: #helm-target-new}

To deploy a version of a Helm chart to another deployment target, you can copy the configuration of the existing version and deploy it to a new target. The deployment target options for Helm charts are {{site.data.keyword.containerlong_notm}} and {{site.data.keyword.openshiftlong_notm}}.
{: shortdesc}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My products**.
1. Select your product.
1. From the Software tab, click **Import a version**.
1. Select **Helm chart** as your deployment method.
1. Select **Copy the configuration of an existing version and deploy it to a new target.**
1. Select the deployment target.

Your source deployment target is the target that your existing version deploys to.
{: note}

1. Select your existing version.
1. Click **Copy existing version**.

Your copied version is displayed in your version list as a separate entry from your existing version. The two versions have the same version number but different deployment targets.
