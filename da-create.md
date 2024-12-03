---


copyright:
  years: 2023, 2024
lastupdated: "2024-12-03"

keywords:

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Adding a deployable architecture to Partner Center
{: #create-da-product}

As the first step in the onboarding process, you can either add the deployable architecture to Partner Center, or you can import an existing one from a private catalog.
{: shortdesc}

A deployable architecture is cloud automation for deploying a common architectural pattern that combines one or more cloud resources. It is designed to provide simplified deployment by users, scalability, and modularity. A deployable architecture incorporates one or more modules. Deployable architectures are coded in Terraform, which you configure with input variables to achieve the behavior that you want. For more information, see [What is a deployable architecture?](/docs/secure-enterprise?topic=secure-enterprise-understand-module-da&interface=ui#what-is-da).

## Before you begin
{: #before-begin-da}

Before you can add a deployable architecture in Partner Center, you must go through the steps to plan and design your architecture, decide what type of component to create, and create the automated code that brings the architecture to life.

To create a deployable architecture, you must define the required files, create a release in GitHub, and then onboard it to a private catalog so that you can share it with others inside or outside of your organization.

Complete the following steps to plan and create your deployable architecture before adding it to Partner Center:

1. [Plan and research for designing an architecture](/docs/secure-enterprise?topic=secure-enterprise-starting-da-process).
1. [Decide what type of component to create](/docs/secure-enterprise?topic=secure-enterprise-choose-plan-process).
1. [Create the deployable architecture](/docs/secure-enterprise?topic=secure-enterprise-create-da).

    You can choose to build your own deployable architecture with Terraform by following these instructions, or you can choose to [download the code from an existing architecture](/docs/secure-enterprise?topic=secure-enterprise-customize-from-catalog) to modify it to fit your needs and create a new deployable architecture with your changes.
    {: note}

After creating the deployable architecture, you can start the onboarding process by adding the deployable architecture to Partner Center, providing the catalog entry details, defining the support experience, and adding variations and versions.

## Adding your deployable architecture to Partner Center
{: #add-new-da}

To add your deployable architecture in Partner Center and start onboarding it, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center > My products**.
1. From the **My products** page, click **Create**.
1. Click **Create a product**, and click **Next > Start now**.
1. Select **Deployable architecture** as your product type, and click **Next**.
1. Enter the display name of your product.
1. Optionally, enter the programmatic name of your product, and click **Next**.
1. Review your product details and click **Create**.

## Importing an existing product
{: #import-da}

You can easily import the deployable architecture that your team has created from a private catalog to Partner Center and start defining your product details. To import a product from a private catalog, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center > My products**.
1. From the **My products** page, click **Create**.
1. Select **Import existing product**, and click **Next**.
1. Select the private catalog that contains your product and click **Select catalog**.
1. Select the product that you want to import and click **Import**.

## Next steps
{: #new-da-next}

You're now ready to [define the catalog entry and product page for your deployable architecture](/docs/sell?topic=sell-da-catalog-details&interface=ui).
