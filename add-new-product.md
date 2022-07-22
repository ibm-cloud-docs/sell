---


copyright:
  years: 2022
lastupdated: "2022-07-22"

keywords: onboard software, third-party software, sell on IBM Cloud, add product, software, partner, sellers, partner center, name, type, create product

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Creating a product
{: #add-product}

During the onboarding process, you can add a new product or import an existing product. Importing an existing product is limited to software that was previously added to a private catalog.
{: shortdesc}

## Adding a new product by using the console
{: #add-new-product}
{: ui}

1. From the My products page in Partner Center, click **Create**.
1. Enter the name of your product. Make sure that the name meets the following requirements:
    * Use 60 characters or less.
    * Do not include "{{site.data.keyword.cloud_notm}}".
    * Do not include the name of your company, former product names, or details like deployment targets and pricing. You can include this information in your readme file.
1. Select the product type. The product type is used for tax assessment purposes. You can review the following list of product types. For more information, see [Selling on IBM Cloud](/docs/sell?topic=sell-selling-clouds).
    - Software as a service
    - Infrastructure as a service
    - Platform as a service
    - Deployable software
1. Click **Add**.

## Importing an existing product by using the console
{: #import-product}
{: ui}

If you previously onboarded software to your account, you can import the software to Partner Center. For more information about adding software to a private catalog, see [Onboarding software to your account](/docs/account?topic=account-create-private-catalog).

1. From the My products page in Partner Center, click **Create**.
1. Select **Import existing product**.
1. Select the private catalog that contains your product and click **Select catalog**. 
1. Select the product that you would like to import and click **Import**.

## Creating a product by using the API
{: #create-new-product}
{: api}

You can programmatically create a product by calling the [Partner Center Sell API](/apidocs/partner-center-sell#create-product){: external} as shown in the following sample request. The example creates a product that is named `My new product`:

```bash
curl --request POST \
  --url https://product-
lifecycle.api.cloud.ibm.com/openapi/v1/products \
  --header 'Authorization: Bearer TOKEN' \
  --header 'Content-Type: application/json' \
  --data '{
  "productName": "My new product",
  "taxAssessment": "SOFTWARE"
}'
```
{: pre}
{: curl}

The name of the product (`productName`) is displayed to users when you publish your product in the catalog.
{: note}

## Importing an existing product by using the API
{: #import-product-api}
{: api}

You can import an existing product only through the UI. To view the steps, go to importing an existing product by using the console.





