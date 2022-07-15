---

copyright:
  years: 2022

lastupdated: "2022-07-15"

keywords: 

subcollection: overview

content-type: conref

---

{{site.data.keyword.attribute-definition-list}}

# Content references for sell subcollection.
{: #conref-example}

The following H2s are going to be reused in several different onboarding topics that need identical support information for Partner Center.
{: shortdesc}

* H2 - **Define your support experience** is used in the following files:
   * tutorial-define-bundle.md
   * tutorial-define-operator.md
   * tutorial-define-svc.md
   * tutorial-define-terraform.md
   * tutorial-define-vsimage.md
   * tutorial-define-vsipower.md
   * tutorial-definevsivpc.md
* H2 - **Define your support experience** - list reuse is used in the following files:
   * service-support.md
   * software-support-details.md
* H2 - **Selecting your product's support provider** is used in the following files:
   * service-support.md
   * software-support-details.md
* H2 - **Providing your product's support information** is used in the following files:
   * service-support.md
   * software-support-details.md
* H2 - **Updating your product's support information** is used in the following files:
   * service-support.md
   * software-support-details.md
* H2 - **Updating your product's support information by using the API** is used in the following file:
   * software-support-details.md

## Define your support experience
{: #define-support-experience}
{: ui}

1. Click **Support**.
1. Select your product's support provider. 
   1. If you select **Community** for your support provider, provide the URL for the support community and provide your product's contact information. The support leader contact information is for internal use only and is not displayed on the product details page.
   1. If you select **Third-party** for your support provider, use the following steps to complete the necessary fields.
1. Click **Add support details** and complete the necessary fields, then click **Save** to add each detail.  You must add at least 1 support detail for your product.
1. After you add all of your product's support details, provide the required URLs for your product. 
1. Add all locations where you provide support for your product. 
1. Add your escalation information. Do not use a personal phone number or email. 
1. Provide your support contact information. This information is for internal use only and is not displayed on the product details page.
{: #steps-support-experience}

## Defining your support experience
{: #shortdesc-support-details}

Making sure that your users understand how to get help and support for your product is key. Defining your support experience includes providing details about how users can contact your support team and escalate issues. To define your product's support experience, you need to select the type of support that is provided, add support details, and then provide information about how users can escalate support cases.
{: shortdesc}
{: #support-experience-shortdesc}

## Selecting your product's support provider
{: #select-support-provider}
{: ui}

Select your product's support provider to add the necessary details that are associated with the third-party or community provider types. 

Third-party products
:  Provided by individual service entities, {{site.data.keyword.IBM_notm}} Business Partners, or independent service vendors (ISV). Support for third-party products is provided by the third-party provider. If the root cause analysis determines that the issue is a defect in a third-party product, {{site.data.keyword.cloud_notm}} isn't required to provide a fix. However, {{site.data.keyword.cloud_notm}} shares analysis with the third-party provider, if needed, and can work with the third-party provider to help solve the issue.

Community products 
:   Provided by open source communities. If a root cause analysis determines that a support issue is a defect in an open source or community product, {{site.data.keyword.cloud_notm}} isn't required to provide a fix. {{site.data.keyword.cloud_notm}} closes the case and refers users to the community or forum for assistance. Users can get community assistance for technical issues through [Stack Overflow](https://stackoverflow.com/questions/tagged/ibm-cloud){: external}.

Use the following steps to select your product's support provider.

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My Products**.
1. Select the product that you're onboarding, and click **Support**. 
1. Select your product's support provider. 
   1. If you select **Community** for your support provider, provide the URL for the support community and your product's support leader contact information. The support leader contact information is for internal use only and is not displayed on the product details page.
   1. If you select **Third-party** for your support provider, use the following steps to complete the necessary fields.

## Providing your product's support information
{: #provide-support-details}
{: ui}

If your product has third-party or {{site.data.keyword.cloud_notm}} provided support, you need to add at least one support detail. The details that you provide are displayed on your product details page in the catalog. At minimum, support must be available 8 hours a day, Monday through Friday. The recommended support coverage is 24 hours a day, 7 days a week, and 365 days a year. 

Don't add details that have personal information, for example, personal emails.
{: important}

Use the following steps to add support details for your product:

1. From the Partner Center Support tab, click **Add support details**, provide your support availability, then click **Save** to add each detail. You must add at least 1 support detail for your product.

   | Support detail | Description |
   |----------------|-------------|
   | Email          | Your company email where users can contact support. |
   | Chat           | The URL for where users can get direct contact with a support representative. |
   | Slack          | The URL for the company Slack channel. |
   | Phone number   | The company phone number where users can get direct contact with a support representative. |
   | Other          | Any additional information, email, URL, or phone number that you want to provide. |
   {: caption="Table 1. Support details" caption-side="bottom"}

1. After you add all of your product's support details, provide the required URLs for your product. 
1. Add all locations where you provide support for your product. 
1. Add your escalation information. Do not use a personal phone number or email. 
1. Provide your support contact information. This information is for internal use only and is not displayed on the product details page. 

## Updating your product's support information
{: #update-support-details}
{: ui}

If your product is already published to the {{site.data.keyword.cloud_notm}} catalog, but you need to update your support details, you can easily do that by editing your published information and requesting an approval for them. 

To update your support information, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My Products**.
1. Select your product and click **Support**. 
1. Click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit") for the field you want to update. 
1. Click **Save**. 

    You can revert to the published state of your support information by clicking **Revert changes**.
    {: note}

1. Click **Request approval** when you're ready with your updates. The approval can take at least five business days. 
1. After your request is reviewed and approved by the {{site.data.keyword.cloud_notm}} team, publish your changes by clicking **Publish approved changes**.

    Any changes that you don't publish are deleted after 60 days.
    {: important}

You can toggle between the updated and the published state of your support information. Toggle the switch on to review your updates, and toggle the switch off for the published state. 

## Updating your product's support information by using the API
{: #update-support-details-api}
{: api}

You can programmatically update the support information of your product by calling the [Partner Center Sell API](/apidocs/partner-center-sell#update-support){: external} as shown in the following sample request. You can update your support site URL, support contacts, or the support escalation process. The example updates the support site URL to `https://my-company.com/support`:

```bash
curl --request PATCH \
  --url  https://product-
lifecycle.api.cloud.ibm.com/openapi/v1/products/9fab83da-98cb-4f18-
a7ba-b6f0435c9673/support \
  --header 'Authorization: Bearer TOKEN'  --header 'Content-Type: 
application/json' \
  --data '{
  "url": "https://my-company.com/support",
  "case": "case",
  "contacts": "JohnSupport@my-company.com",
  "country": "us",
  "escalationProcess": "Customers can escalate support cases via email.",
}'
```
{: pre}
{: curl}

The details that you provide are displayed on your product details page in the catalog.
{: note}
