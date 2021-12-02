---

copyright:

  years: 2020, 2021

lastupdated: "2021-12-02"

keywords: OVA images, metadata, YAML, onboard, GitHub, publish

subcollection: sell

content-type: api-docs

---

{{site.data.keyword.attribute-definition-list}}

# Example YAML file for onboarding OVA images
{: #3p-ova-prereqs}

The process to onboard OVA images is the same as onboarding other third-party software except you need to add a YAML file that contains required onboarding information. Manually create the YAML and add it to your GitHub repo that you reference during the onboarding process.
{: shortdesc}

After you complete this prerequisite, you're ready to add your OVA image to the private catalog you're using for onboarding, and validate that it's ready for publishing. See [Onboarding your software](/docs/sell?topic=sell-sw-validate).

## Metadata
{: #ova-metadata}

The following table lists the metadata to include in your YAML file:

| Metadata key  | Description |
|---------------|----------|
| `app_id`      | The programmatic name of the product. Not exposed to the user. |
| `title`       | The name of the product that's externally displayed in the public catalog. |
| `version`     | The version ID of the OVA image. You must update each time that you update the OVA image. This value must be in semantic versioning, for example, `1.0.0`, `1.0.1`, `1.0.2`. |
| `revision`    | The version of the OVA Metadata. You must update each time that you update your metadata. |
| `kind`        | The value is always `ova`. |
| `image`       | The object that contains `url` or `sha256` values. |
| `url`         | A child value of `image`. The URL for the `image` path. |
| `sha256`      | A child value of `image`. The signature of the file referenced in `image`. |
| `eula_url`    | The link to publicly accessible license document. Optional. |
| `eula_label`  | The label for the license link. Optional. |
| `categories`  | The array of {{site.data.keyword.Bluemix_notm}} catalog categories that are used to filter items in the catalog. Optional. |
| `logo`        | The URL path to the product logo that's externally displayed in the public catalog along with the `title` value. |
| `description` | The short description of the OVA image that's externally displayed in the public catalog along with the `title` and `logo` values. |
| `readme`      |  The readme file text for the OVA image. |
| `links`       | Links to product support or documentation. Optional. |
{: caption="Table 1. Required metadata for OVA images" caption-side="top"}


## YAML example
{: #yaml}

The following example shows a YAML file that is formatted with the required metadata.

```yaml
app_id: devName
title: productName
version: 5.4.2-0
revision: 3
kind: ova
image:
  url: https://productURL-5.4.2-0.ova
  sha256: 1aaa22bbb33c44444dd5e66f4g7hh8i99j11kk22ll33m4nn5555o6pp77qq888r
eula_url: https://www.product.org/licenses/LICENSE-2.0.txt
eula_label: Product 2.0
categories:
- network
logo: https://productIcon.net/images.png
description: "Description for OVA image offering."
readme: The full text for the required readme about the ova image.
links:
- id: docs_index
    title: Getting started
    url: https://docs.OVAimage-gettingStarted.com
- id: support_index
    title: Product Support
    url: https://docs.OVAimage-support.com
```
