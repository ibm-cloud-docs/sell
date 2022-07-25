---


copyright:
  years: 2020, 2022
lastupdated: "2022-07-22"

keywords: software, third party, product portal, publish software, promote software, partner portal, partners, sellers

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Publishing your software
{: #sw-publish}

As the last step in the onboarding process, you can submit a request to publish your third-party software to the {{site.data.keyword.cloud}} catalog. When you publish software to the catalog, you can choose to publish your software to all {{site.data.keyword.cloud_notm}} users in the catalog or to only specific accounts. If you choose to publish to specific accounts, your product is available only for users in those accounts.
{: shortdesc}

## Requesting for approval by using the console
{: #sw-request-approval}
{: ui}

Before you can publish your product to the catalog, you must submit your software for approval.

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My products**.
1. Select the product that you are onboarding.
1. Review the details on each tab to ensure that everything is accurate. 
1. Click **Request approval**.

After your publishing request is reviewed by the {{site.data.keyword.cloud_notm}} team, you receive an email with the results of the review. 

If your software is not approved for publishing, the email includes feedback on the items you must update. If you have questions about the feedback, from the My products page click the **Help** icon ![Help icon](../icons/help.svg "Help"), and then click **Contact us**. 
{: tip}

## Publishing to the {{site.data.keyword.cloud_notm}} catalog by using the console
{: #sw-publish-catalog}
{: ui}

To publish your software to the {{site.data.keyword.cloud_notm}} catalog after you receive approval, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My products**.
1. Select your product.
1. Click **Manage publish visibility**.
1. Select **{{site.data.keyword.cloud_notm}} catalog**.
1. Select a version of your product.
1. Click **Publish version**.     

As a third-party provider, you're responsible for maintaining all assets of the published software in the {{site.data.keyword.cloud_notm}} catalog and deprecating outdated versions. For more information, see [Deprecating software from the {{site.data.keyword.cloud_notm}} catalog](/docs/sell?topic=sell-deprecate-product). 
{: note}

## Publishing to specific accounts or enterprises by using the console
{: #sw-publish-account}
{: ui}

If you don't want your product to be publicly available to all users in the {{site.data.keyword.cloud_notm}} catalog, you can choose to publish it to only the accounts that you specify.

To publish your product to specific accounts, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My products**.
1. Select the product that you want to publish.
1. Click **Manage publish visibility**.
1. Select **Accounts**, and then choose the current account or enterprise that you're logged in to. Click **Manage account groups** to select specific account groups within the current enterprise. Additionally, you can specify other accounts that you want to publish to by entering the account ID. 
1. Select a version of your product.     
1. Click **Publish version**.

## Requesting for approval by using the API
{: #sw-request-approval-api}
{: api}

Before you can publish your product to the {{site.data.keyword.cloud_notm}} catalog, you must request an approval for your product. You can programmatically submit your software for approval by calling the [Partner Center Sell API](/apidocs/partner-center-sell#request-product-approval){: external} as shown in the following sample request:

```bash
curl --request POST \
  --url  https://product-
lifecycle.api.cloud.ibm.com/openapi/v1/products/9fab83da-98cb-4f18-
a7ba-b6f0435c9673/approvals \
  --header 'Authorization: Bearer TOKEN'
```
{: pre}
{: curl}

## Publishing to the {{site.data.keyword.cloud_notm}} catalog by using the API
{: #sw-publish-catalog-api}
{: api}

You can programmatically publish your product to the {{site.data.keyword.cloud_notm}} catalog by calling the [Partner Center Sell API](/apidocs/partner-center-sell#publish-product){: external} as shown in the following sample request:

```bash
curl --request POST \
  --url  https://product-
lifecycle.api.cloud.ibm.com/openapi/v1/products/9fab83da-98cb-4f18-
a7ba-b6f0435c9673/publish \
  --header 'Authorization: Bearer TOKEN'
```
{: pre}
{: curl}

## Publishing to specific accounts or enterprises by using the API
{: #sw-publish-account-api}
{: api}

You can publish your product to specific accounts or enterprises only through the UI. To view the steps, go to publishing to specific accounts or enterprises by using the console. 

