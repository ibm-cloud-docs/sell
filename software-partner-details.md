---


copyright:
  years: 2021, 2023
lastupdated: "2023-08-04"

keywords: onboard software, partner details, product details, partner center, third-party, software, company details

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Updating your company and product details
{: #sw-partner-details}

As an account administrator, you can update your company and product details in the {{site.data.keyword.cloud}} Partner Center. The details include the name of the product that you're onboarding and the name and email address of the primary contact for the product.
{: shortdesc}

## Updating your partner information by using the console
{: #sw-details-company}
{: ui}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My products**.
1. Select your product.
1. Click **Dashboard**.
1. To update the company name or primary contact, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit") next to each field.

   To update the primary contact, the user must already be a member of your account. For more information, see [Inviting team members to help onboard software](/docs/sell?topic=sell-sw-invite-team).
   {: tip}

## Updating your partner information by using the API
{: #sw-details-company-api}
{: api}

You can update your partner information only through the UI. To view the steps, go to updating your partner information by using the console.

## Updating your company information by using the console
{: #sw-details-company-name-dpa}
{: ui}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My products**.
1. Select your product.
1. Click **Edit company** in the **Company** section.
1. Click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit").
1. Enter the legal name of your company, and click **Save**.

## Updating your company information by using the API
{: #sw-update-company-api}
{: api}

You can programmatically update your company details by calling the [Partner Center Sell API](/apidocs/partner-center-sell#update-catalog){: external} as shown in the following sample request. The example updates the company name to `My updated company`:

```bash
curl --request PATCH \
  --url  https://product-
lifecycle.api.cloud.ibm.com/openapi/v1/products/9fab83da-98cb-4f18-
a7ba-b6f0435c9673/catalog \
  --header 'Authorization: Bearer TOKEN' \
  --header 'Content-Type: application/json' \
  --data '{
  "provider": "My updated company"
}'
```
{: pre}
{: curl}

## Updating your product information by using the console
{: #sw-details-product}
{: ui}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My products**.
1. Select your product.
1. Click **Dashboard**.
1. To update the name of the product, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit"). Make sure that your product name meets the following requirements:

   * Use 60 characters or less.
   * Do not include the name of the company, any former product names, or details such as deployment target, method, or pricing. You can include this information in your readme file.
   * Do not include "{{site.data.keyword.cloud_notm}}".

## Updating your product information by using the API
{: #sw-update-product-api}
{: api}

You can programmatically update your product details by calling the [Partner Center Sell API](/apidocs/partner-center-sell#update-product){: external} as shown in the following sample request. The example updates the name of the product to `My updated product`:

```bash
curl --request PATCH \
  --url https://product-
lifecycle.api.cloud.ibm.com/openapi/v1/products/9fab83da-98cb-4f18-
a7ba-b6f0435c9673 \
  --header 'Authorization: Bearer TOKEN' \
  --header 'Content-Type: application/json' \
  --data '{
  "productName": "My updated product",
  "materialAgreement": true,
  "taxAssessment": "SOFTWARE",
}'
```
{: pre}
{: curl}

The name of the product (`productName`) is displayed to users when you publish your product in the catalog.
{: note}
