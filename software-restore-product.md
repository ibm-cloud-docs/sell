---


copyright:
  years: 2021, 2022
lastupdated: "2022-07-15"

keywords: onboard software, third-party software, sell on IBM Cloud, suspend, support, software, partner center, sellers, catalog, restore

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Restoring a deprecated product or version
{: #restore-deprecated-product}

After you deprecate your product or version, your software enters a 90-day deprecation period before it is removed from the {{site.data.keyword.cloud}} catalog. During this deprecation period, you can't make changes to your product, but you can restore your software to its last published state to keep it in the catalog. Your software cannot be restored after the 90-day deprecation period. 
{: shortdesc}

## Restoring a deprecated product or version by using the console
{: #sw-restore-deprecated-ui}
{: ui}

Complete the following steps to restore your product: 

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My Products**.
1. Click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg "Actions") for the product that you want to restore, and select **Restore**. 

Complete the following steps to restore your version: 

1. Go to the [Partner Center](https://cloud.ibm.com/partner-center/sell){: external} in the {{site.data.keyword.cloud_notm}} console, and click **My products**.
1. Select your product. 
1. From the Software tab, click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg "Actions") for the version you want to restore, and select **Restore version**.

## Restoring a deprecated product by using the API
{: #sw-restore-deprecate-api}
{: api}

You can programmatically restore your product by calling the [Partner Center Sell API](/apidocs/partner-center-sell#restore-product){: external} as shown in the following sample request. Specify `reason` to provide details about why you want to restore your deprecated product.

```bash
curl --request POST \
  --url  https://product-
lifecycle.api.cloud.ibm.com/openapi/v1/products/9fab83da-98cb-4f18-
a7ba-b6f0435c9673/restore \
  --header 'Authorization: Bearer TOKEN' \  
  --data '{
       "reason": "I want to restore my deprecated product to keep it in the catalog."
}'
```
{: pre}
{: curl}
