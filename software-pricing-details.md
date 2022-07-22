---


copyright:
  years: 2021, 2022
lastupdated: "2022-07-15"

keywords: software, pricing, paid, free, third-party, license, BYOL, bring your own license

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Defining your pricing model for software
{: #sw-pricing}

When onboarding your product, you need to define the pricing model for your software. Currently, the {{site.data.keyword.cloud}} catalog supports free plans and bring your own license (BYOL).
{: shortdesc}

## Adding a free plan by using the console
{: #pricing-free}
{: ui}

By adding a free plan, you are indicating that your product does not require any payment or license to use. 

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My products**.
1. Select the product that you're onboarding, and click **Pricing**.
1. Select **Free**. 

## Adding a BYOL plan by using the console
{: #pricing-byol}
{: ui}

By adding a bring your own license plan, you are indicating that customers need to purchase a license to use your product. You are required to provide the name of the license and a URL where customers can purchase the license. 

If you have not imported a version of your software, you can still create a BYOL plan. However, you need to import a version before your product is published. For more information, see [Onboarding your software](/docs/sell?topic=sell-sw-validate).
{: note}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My products**.
1. Select the product that you're onboarding, and click **Pricing**.
1. Select **Pricing plans**. 
1. Click **Add plan**. 
1. Select **BYOL**.
1. In the **Add pricing plan** panel, enter the **Name** of the license. Customers use the license name to find and purchase the license. 
1. Enter the **URL** that customers can use to learn about and purchase the license. 
1. Enter the **Description** of your license. Explain why customers need to purchase the license and what access they will receive. 
1. Click **Add**.

All information that is entered in the **Add pricing plan** panel is displayed to customers in the {{site.data.keyword.cloud_notm}} catalog to help them purchase the required license.
{: note}

## Creating a free plan by using the API
{: #create-free-plan}
{: api}

You can programmatically create a free plan by calling the [Partner Center Sell API](/apidocs/partner-center-sell#update-catalog){: external} as shown in the following sample request.

```bash
curl --request PATCH \
  --url  https://product-
lifecycle.api.cloud.ibm.com/openapi/v1/products/9fab83da-98cb-4f18-
a7ba-b6f0435c9673/catalog \
  --header 'Authorization: Bearer TOKEN' \  
  --header 'Content-Type: application/json' \   
  --data '{
  "pricingModel": "free",
}'
```
{: pre}
{: curl}

## Creating a BYOL plan by using the API
{: #create-byol-plan}
{: api}

You can programmatically create a BYOL plan by calling the [Partner Center Sell API](/apidocs/partner-center-sell#create-plan){: external} as shown in the following sample request. The example creates a BYOL plan that is named `Standard`:

```bash
curl --request POST \
  --url https://product-
lifecycle.api.cloud.ibm.com/openapi/v1/products/9fab83da-98cb-4f18-
a7ba-b6f0435c9673/plans \
  --header 'Authorization: Bearer TOKEN' \
  --header 'Content-Type: application/json' \
  --data '{
        "description": "Purchasing a license is required to use the product.",
	"label": "Standard",
	"type": "byol",
	"url": "https://standard.plan.com/license"
}'
```
{: pre}
{: curl}

