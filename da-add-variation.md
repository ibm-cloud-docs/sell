---


copyright:
  years: 2023
lastupdated: "2023-09-26"

keywords: deployable architecture, third party, product center sell, variation, add variation, add version, deployable architecture version, partner center, partners, deployable architecture variation

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Adding deployable architecture variations
{: #da-variation}

You can add up to three variations to your deployable architecture based on your business needs. This means that a single deployable architecture tile in the {{site.data.keyword.cloud_notm}} catalog can have different options for your customers to try out that might be considered small, medium, or large variations. A variation addresses a common business problem that your deployable architecture solves, but the implementation differs. Also, each deployable architecture variation can have more than one version. Provide a unique display name for the different variations during onboarding, and at least one architecture diagram for each variation. You must specify the same version number during onboarding to connect multiple variations together in a single deployable architecture tile.
{: shortdesc}

## Adding variations to your deployable architecture
{: #da-add-variation}

To add a variation to your deployable architecture, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center > Sell > My products**.
1. Select your product and go to the Variation tab.
1. Click **Add**. This step directs you to Catalog management.
1. Select your delivery method.
1. Select the type of repository. If the source for your deployable architecture is located in a private repository, you need to authenticate with a personal access token.
1. Enter the source URL. This URL must end in `tar.gz`.
1. Enter the variation display name.
1. Enter the version in the format of major version, minor version, and revision, for example `1.0.0`.
1. Click **Add version**.

## Configuring your version
{: #da-config-version}

After you add a version, you can configure it by completing the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center > Sell > My products**.
1. Select your product and go to the Variation tab. Click the **Table expand** icon ![Table expand icon](../icons/table-expand.svg "Table expand") on a variation and click **View details**.
1. On the Configure version page, confirm your version details and add deployment values for your version, then click **Next**.
1. On the Add deployable architecture details page, add architecture diagrams and highlights for your deployable architecture, then click **Next**.
1. On the End user license agreements page, provide the URLs to the license agreements that your customers are required to accept when they install your product. Then, click **Next**.
1. Edit your readme file, and then click **Next**.
1. On the Validate version page, validate that the product version can be successfully deployed to the intended target by clicking **Validate**. Click **Next**.
1. Review the estimated starting cost of your product, and click **Next**.
1. On the Manage compliance page, manage the security and compliance information for your version. Click **Next**.
1. Finalize your version and review whether all requirements are completed. Then click **Go to Partner Center**.

## Next steps
{: #da-next-variation}

[Review the pricing details of your deployable architecture](/docs/sell?topic=sell-da-pricing&interface=ui).

