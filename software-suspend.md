---


copyright:
  years: 2021, 2022
lastupdated: "2022-07-13"

keywords: onboard software, third-party software, sell on IBM Cloud, suspend, partner center, catalog 

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Suspending your product from the {{site.data.keyword.cloud_notm}} catalog
{: #suspend-product}

If you need to remove a product from the {{site.data.keyword.cloud}} catalog without permanently deleting or deprecating it, you can suspend it for up to 7 days. Suspending a product can be useful if, for example, you discover a bug or a vulnerability in your product that must be investigated before more customers install it. 
{: shortdesc}

Suspending your product will not permanently delete it from the {{site.data.keyword.cloud_notm}} catalog. If you need to permanently delete your product, deprecate it instead. 
{: note}

## Suspend your product from the {{site.data.keyword.cloud_notm}} catalog by using the console
{: #sw-suspend-product-ui}
{: ui}

Complete the following steps to suspend your product: 

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My Products**.
1. Click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg "Actions") for the product that you want to suspend, and select **Suspend**.  
1. Explain why you want to suspend your product.  
1. Click **Suspend**.

After you suspend your product, you must request approval to publish it again within 7 days, or your product will be deprecated. Deprecated products are removed after 90 days. For more information, see [Publishing your software to the {{site.data.keyword.cloud_notm}} catalog](/docs/sell?topic=sell-sw-publish). 

{{site.data.keyword.cloud_notm}} can suspend your product if there's an issue that you need to address. Any updates that you need to make are shared by email. 

## Suspend your product from the {{site.data.keyword.cloud_notm}} catalog by using the API
{: #sw-suspend-product-api}
{: api}

You can programmatically suspend your product by calling the Partner Center Sell API as shown in the following sample request. Specify `reason` to provide details about why you want to suspend your published product.

```bash
curl --request POST \
  --url  https://product-
lifecycle.api.cloud.ibm.com/openapi/v1/products/9fab83da-98cb-4f18-
a7ba-b6f0435c9673/suspend \
  --header 'Authorization: Bearer TOKEN' \  
  --data '{
	      "reason": "There is a bug in the operation of the product that must be fixed. To fix the error, I want to suspend my product."
}'
```
{: pre}
{: curl}

For more information, see [Partner Center Sell API](/apidocs/partner-center-sell#suspend-product){: external}.
 