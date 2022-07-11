---


copyright:
  years: 2020, 2022
lastupdated: "2022-07-11"

keywords: onboard software, third-party software, sell on IBM Cloud, catalog details, software, partner, sellers, partner center, catalog, logo, catalog entry, about, product page, catalog listing

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Defining your catalog entry and product page
{: #sw-catalog-details}

During the onboarding process, you provide certain details about your product that are displayed in the {{site.data.keyword.cloud}} catalog. The details include your product logo and description, a list of product features, supporting media, and a link to your warranted product documentation. 
{: shortdesc}

## Define your catalog entry by using the console
{: #catalog-entry}
{: ui}

The contents of a catalog entry include the company or product logo, a short description about the product, and other details. Because the catalog entry is visible to users as they browse the {{site.data.keyword.cloud_notm}} catalog, provide clear details that can help users find your product.

### Providing your company or product logo
{: #catalog-logo}
{: ui}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My Products**.
1. Select the product that you're onboarding, and click **Product details**.
1. Click **Add logo**. 
1. Enter the URL for your company or product logo, for example, `http://example.com/ex/ex.svg`, and **Save**.

   Make sure that your logo image is an SVG or PNG file that's a square image roughly sized at 32 x 32 pixels and does not appear blurry or pixelated.
   {: note}

### Providing a short description of your product
{: #catalog-short-desc}
{: ui}

1. Click **Enter description**. 
1. Enter a short description of what your product is, its value, and any other details that you want to be displayed in your catalog entry. 
1. Click **Save**. 

### Selecting your catalog category
{: #catalog-category}
{: ui}

Users can filter the catalog to display similar products based on common solutions, function, or use.  

1. Click **Select category**. 
1. From the list, select the category that best describes your product. For a description of each category, see the following table.

#### Category types
{: #category-types}
{: ui}

The following table describes each type of category that you can select.

| Category | Description |
|----------|------------|
| AI / Machine Learning | Products that enable systems to learn from data rather than through explicit programming. |
| Analytics | Products that facilitate the analysis of data, typically large sets of business data, by the use of mathematics, statistics, and other means. |
| Blockchain | Products that facilitate the process of recording transactions and tracking assets in a business network. |
| Compute | Infrastructure resources that serve as the basis for building apps in the cloud. |
| Containers | A standard unit of software that packages up code, and all its dependencies, so the app runs quickly and reliably from one computing environment to another. |
| Databases | Products that provide some form of access to a database without requiring setting up physical hardware, installing software, or configuring for performance. |
| Developer tools | Products that support developing, testing, and debugging software. |
| Integration | Products that facilitate the connection of data, apps, APIs, and devices across an organization to be more efficient, productive, and agile. |
| Internet of Things | Products that support receiving and transferring data over wireless networks without human intervention. |
| Logging and monitoring | Products that support storing, searching, analyzing, and monitoring log data and events. And, products that support reviewing and managing the operational workflow and processes being logged. |
| Mobile| Products with specific or special utility for users creatings things to be used on mobile devices. |
| Networking | Products that support or augment the linking of computers so they can operate interactively. |
| Security | Products that provide the protection of stored data from theft, leakage, and deletion. |
| Storage | Products that support data to be created, read, updated, and deleted.|
{: caption="Table 1. Category descriptions" caption-side="top"} 

### Adding search keywords
{: #catalog-keywords}
{: ui}

Add relevant keywords that enable your product to appear in search results when users search the catalog. 

1. Click **Enter words, phrases, and other key search terms associated with the product**. 
1. Enter one or more keywords for your product, and click **Save**.

## Define your product page by using the console
{: #catalog-about}
{: ui}

When users select your product from the catalog, they are directed to additional details, including a list of features and supporting media. These details are displayed on the About tab within your product page.

### Providing a list of product features
{: #catalog-features}
{: ui}

Provide a list of features that highlights your product's attributes and benefits for users.

Use a descriptive title and 1-2 sentences for each feature. You want the information to be visually scannable for users.
{: tip}

### Providing a detailed description about your product
{: #catalog-long-desc}
{: ui}

Your detailed description explains the value of your product and what users gain by using it. The detailed description is displayed at the beginning of your product page in the catalog. You can expand on the short description that you provide for your catalog entry, but don't simply repeat it.

### Providing media
{: #catalog-media}
{: ui}

Provide links to high-quality images or videos to help illustrate what your product is, its value, and user benefits. The supported media types are images, videos in MP4 or WebM file format, and videos hosted on YouTube or Vimeo.

Some examples of effective media include an introductory walkthrough of your product, an explanation of what your product is and why users might want to use it, or a comparison of certain features.
{: tip}

### Providing your documentation link
{: #catalog-docs}
{: ui}

Your documentation link is used to direct users to your product's warranted documentation. 

## Define your catalog entry by using the API
{: #catalog-entry-api}
{: api}

You can programmatically provide certain details about your product that are displayed in the {{site.data.keyword.cloud}} catalog by calling the Partner Center Sell API.

### Providing your company or product logo
{: #catalog-logo-api}
{: api}

You can programmatically provide your company or product logo by calling the Partner Center Sell API as shown in the following sample request. In the example the URL of the company or product logo is `https://www.ibm.com/contact/us/en/images/bee.svg`:

```bash
curl --request PATCH \
  --url  https://product-
lifecycle.api.cloud.ibm.com/openapi/v1/products/9fab83da-98cb-4f18-
a7ba-b6f0435c9673/catalog \
  --header 'Authorization: Bearer TOKEN' \ 
  --header 'Content-Type: application/json' \ 
  --data '{
  "iconUrl": "https://www.ibm.com/contact/us/en/images/bee.svg"
}'
```
{: pre}
{: curl}

Make sure that your logo image is an SVG or PNG file that's a square image roughly sized at 32 x 32 pixels and does not appear blurry or pixelated.
{: note}

For more information, see [Partner Center Sell API](/apidocs/partner-center-sell#update-catalog){: external}.

### Providing a short description of your product
{: #catalog-short-desc-api}
{: api}

You can programmatically provide a short description of your product by calling the Partner Center Sell API as shown in the following sample request. The example adds the `This is my product` description to the product:

```bash
curl --request PATCH \
  --url  https://product-
lifecycle.api.cloud.ibm.com/openapi/v1/products/9fab83da-98cb-4f18-
a7ba-b6f0435c9673/catalog \
  --header 'Authorization: Bearer TOKEN' \ 
  --header 'Content-Type: application/json' \ 
  --data '{
  "description": "This is my product"
}'
```
{: pre}
{: curl}

For more information, see [Partner Center Sell API](/apidocs/partner-center-sell#update-catalog){: external}.

### Selecting your catalog category
{: #catalog-category-api}
{: api}

You can programmatically add the category to your product that best describes it by calling the Partner Center Sell API as shown in the following sample request. The example adds the `storage` category type to the product:

```bash
curl --request PATCH \
  --url  https://product-
lifecycle.api.cloud.ibm.com/openapi/v1/products/9fab83da-98cb-4f18-
a7ba-b6f0435c9673/catalog \
  --header 'Authorization: Bearer TOKEN' \ 
  --header 'Content-Type: application/json' \ 
  --data '{
  "category": "storage"
}'
```
{: pre}
{: curl}

For more information, see [Partner Center Sell API](/apidocs/partner-center-sell#update-catalog){: external}.

### Adding search keywords
{: #catalog-keywords-api}
{: api}

You can programmatically add relevant keywords to your product by calling the Partner Center Sell API as shown in the following sample request. The example adds the `[ "virtual machine" ]` keyword to the product:

```bash
curl --request PATCH \
  --url  https://product-
lifecycle.api.cloud.ibm.com/openapi/v1/products/9fab83da-98cb-4f18-
a7ba-b6f0435c9673/catalog \
  --header 'Authorization: Bearer TOKEN' \ 
  --header 'Content-Type: application/json' \ 
  --data '{
  "keywords": "[ "virtual machine" ]"
}'
```
{: pre}
{: curl}

For more information, see [Partner Center Sell API](/apidocs/partner-center-sell#update-catalog){: external}.

## Define your product page by using the API
{: #catalog-about-api}
{: api}

You can programmatically define your product page by calling the Partner Center Sell API. When users select your product from the catalog, they are directed to additional details, including a list of features and supporting media. These details are displayed on the About tab within your product page. 

### Providing a list of product features
{: #catalog-features-api}
{: api}

You can programmatically provide a list of features that highlights your product's attributes and benefits for users by calling the Partner Center Sell API as shown in the following sample request. The example adds a feature to the product that is named `Best feature` with the `This is the best feature of my product` description:

```bash
curl --request PATCH \
  --url  https://product-
lifecycle.api.cloud.ibm.com/openapi/v1/products/9fab83da-98cb-4f18-
a7ba-b6f0435c9673/catalog \
  --header 'Authorization: Bearer TOKEN' \ 
  --header 'Content-Type: application/json' \ 
  --data '{
  "highlights": [{
  "description": "This is the best feature of my product",
  "title": "Best feature"
}],
}'
```
{: pre}
{: curl}

For more information, see [Partner Center Sell API](/apidocs/partner-center-sell#update-catalog){: external}.

### Providing a detailed description about your product
{: #catalog-long-desc-api}
{: api}

You can programmatically add a detailed description to your product by calling the Partner Center Sell API as shown in the following sample request. The example adds the `This is a unique description about my product` description to the product:

```bash
curl --request PATCH \
  --url  https://product-
lifecycle.api.cloud.ibm.com/openapi/v1/products/9fab83da-98cb-4f18-
a7ba-b6f0435c9673/catalog \
  --header 'Authorization: Bearer TOKEN' \ 
  --header 'Content-Type: application/json' \ 
  --data '{
  "longDescription": "This is a unique description about my product"
}'
```
{: pre}
{: curl}

The detailed description is displayed at the beginning of your product page in the catalog.
{: note}

For more information, see [Partner Center Sell API](/apidocs/partner-center-sell#update-catalog){: external}.

### Providing media
{: #catalog-media-api}
{: api}

You can programmatically add links to high-quality images or videos that help illustrate what your product is by calling the Partner Center Sell API as shown in the following sample request. The example adds the `image` media type to your product page, which can be found at the `http://myproduct.com/images/product_image.png` URL:

```bash
curl --request PATCH \
  --url  https://product-
lifecycle.api.cloud.ibm.com/openapi/v1/products/9fab83da-98cb-4f18-
a7ba-b6f0435c9673/catalog \
  --header 'Authorization: Bearer TOKEN' \ 
  --header 'Content-Type: application/json' \ 
  --data '{
  "media": [{
  "caption": "This caption indicates what the media illustrates",
  "type": "image",
  "url": "http://myproduct.com/images/product_image.png"
}],
}'
```
{: pre}
{: curl}

For more information, see [Partner Center Sell API](/apidocs/partner-center-sell#update-catalog){: external}.

### Providing your documentation link
{: #catalog-docs-api}
{: api}

You can provide a link to your product's warranted documentation by calling the Partner Center Sell API as shown in the following sample request. The example adds the `https://myproduct/docs/documentation-of-my-product` documentation link to your product page:

```bash
curl --request PATCH \
  --url  https://product-
lifecycle.api.cloud.ibm.com/openapi/v1/products/9fab83da-98cb-4f18-
a7ba-b6f0435c9673/catalog \
  --header 'Authorization: Bearer TOKEN' \ 
  --header 'Content-Type: application/json' \ 
  --data '{
  "documentationUrl": "https://myproduct/docs/documentation-of-my-product"
}'
```
{: pre}
{: curl}

For more information, see [Partner Center Sell API](/apidocs/partner-center-sell#update-catalog){: external}.

