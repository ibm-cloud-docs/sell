---


copyright:
  years: 2021
lastupdated: "2021-12-02"

keywords: software, third-party software, sellers, partners, versions, test, partner center, reload 

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}


# Reloading a software version
{: #software-reload}

You can reload a version of your software in your private catalog to update the version based on your current repository. When you reload a version, you revert it to its default state when you first imported the software. 
{: shortdesc}

## Reloading an unpublished version
{: #software-reload-catalog}

To update a version of your software that isn't published to the catalog, you must reload the version from your source repository and validate it.  

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Catalogs** > **Private catalogs**. 
1. Select the private catalog where your product is located. 
1. Select your product. 
1. Select the version of the software you would like to reload. 
1. Open the **Actions** menu and select **Reload version**.
1. Click **Reload version**. 
1. Configure and validate your software. 

Configuration and validation steps vary based on the type of software.
{: note}

## Reloading a published version
{: #software-reload-published}

To update a published version of your software, you must create a draft, reload the version from your source repository, validate, and merge the changes.  

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Catalogs** > **Private catalogs**. 
1. Select the private catalog where your product is located. 
1. Select your product. 
1. Select the version of the software that you want to reload. 
1. Open the **Actions** menu and select **Edit** to create a draft of your original version.
1. In the draft version, open the **Actions** menu and select **Reload version**.
1. In the Reload version panel, click **Reload version**. 
1. Configure and validate your software. 

   Configuration and validation steps vary based on the type of software.
   {: note}

1. Open the **Actions** menu and select **Merge changes**.
1. Click **Merge** to update your original version.
