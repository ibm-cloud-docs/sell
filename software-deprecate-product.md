---


copyright:
  years: 2021, 2022
lastupdated: "2022-07-15"

keywords: onboard software, third-party software, sell on IBM Cloud, suspend, support, software, partner center, sellers, catalog, remove, delete, deprecate

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Deprecating software from the {{site.data.keyword.cloud_notm}} catalog
{: #deprecate-product}

If you need to permanently delete your product or version from the {{site.data.keyword.cloud}} catalog, deprecate it first. Your product remains available for use during a 90-day deprecation period, and is removed after 90 days.
{: shortdesc}

Deprecating your product or version will permanently delete it from the {{site.data.keyword.cloud_notm}} catalog. If you want to temporarily remove your product from the catalog, suspend it instead.
{: note}

## Deprecating software from the {{site.data.keyword.cloud_notm}} catalog by using the console
{: #sw-deprecate-ui}
{: ui}

Complete the following steps to deprecate your product or version:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My products**.
1. Click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg "Actions") for the product that you want to deprecate, and select **Deprecate**.
1. Optionally, you can include more details, like a link to a deprecation announcement.
1. Click **Deprecate**.

You can deprecate a specific version of your software by clicking the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg "Actions") for the version you want to deprecate on the Software tab. If your software has only one published version, and you deprecate that version, the entire product is deprecated.

## Deprecating software from the {{site.data.keyword.cloud_notm}} catalog by using the API
{: #sw-deprecate-api}
{: api}

You can programmatically deprecate your product by calling the [Partner Center Sell API](/apidocs/partner-center-sell#deprecate-product){: external} as shown in the following sample request. Specify `reason` to provide details about why you want to deprecate your published product:

```bash
curl --request POST \
  --url  https://product-
lifecycle.api.cloud.ibm.com/openapi/v1/products/9fab83da-98cb-4f18-
a7ba-b6f0435c9673/deprecate \
  --header 'Authorization: Bearer TOKEN' \
  --data '{
       "reason": "I need to permanently delete my product from the IBM Cloud catalog."
}'
```
{: pre}
{: curl}
