---

copyright:
  years: 2022, 2023

lastupdated: "2023-11-28"

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
   * da-support.md
* H2 - **Selecting your product's support provider** is used in the following files:
   * service-support.md
   * software-support-details.md
   * da-support.md
* H2 - **Providing your product's support information** is used in the following files:
   * service-support.md
   * software-support-details.md
   * da-support.md
* H2 - **Updating your product's support information** is used in the following files:
   * service-support.md
   * software-support-details.md
   * da-support.md
* H2 - **Define IAM access** is used in the following files:
   * tutorial-onboard-terraform.md
   * tutorial-onboard-vsimage.md
   * tutorial-onboard-vsipower.md
   * software-validate.md
* H2 - **Edit output value descriptions** is used in the following files:
   * tutorial-onboard-terraform.md
   * tutorial-onboard-vsimage.md
   * tutorial-onboard-vsipower.md
   * software-validate.md

* H2 - **## Manage compliance** is used in the following files:
   * tutorial-onboard-operator.md

## Define your support experience
{: #define-support-experience}

1. Click **Support**.
1. Select your product's support provider and complete the support statement field. For the support statement, describe the provided support for your product and add any additional support information that isn't provided in the other fields.
   1. If you select **Community** for your support provider, provide the URL for the support community.
   1. If you select **Third-party** for your support provider, use the following steps to complete the necessary fields.
1. Click **Add support details** and complete the necessary fields, then click **Save** to add each detail. You must add at least 1 support detail for your product.
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

Select your product's support provider to add the necessary details that are associated with the third-party or community provider types.

Third-party products
:  Provided by individual service entities, {{site.data.keyword.IBM_notm}} Business Partners, or independent service vendors (ISV). Support for third-party products is provided by the third-party provider. If the root cause analysis determines that the issue is a defect in a third-party product, {{site.data.keyword.cloud_notm}} isn't required to provide a fix. However, {{site.data.keyword.cloud_notm}} shares analysis with the third-party provider, if needed, and can work with the third-party provider to help solve the issue.

Community products
:   Provided by open source communities. If a root cause analysis determines that a support issue is a defect in an open source or community product, {{site.data.keyword.cloud_notm}} isn't required to provide a fix. {{site.data.keyword.cloud_notm}} closes the case and refers users to the community or forum for assistance. Users can get community assistance for technical issues through [Stack Overflow](https://stackoverflow.com/questions/tagged/ibm-cloud){: external}.

Use the following steps to select your product's support provider.

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My products**.
1. Select the product that you're onboarding, and click **Support**.
1. Select your product's support provider.
   1. If you select **Community**, provide the support statement and the URL for the support community, and select the languages in which support is provided.
   1. If you select **Third-party**, use the following steps to complete the necessary fields.

## Providing your product's support information
{: #provide-support-details}

If your product has third-party or {{site.data.keyword.cloud_notm}} provided support, you need to add at least one support detail. The details that you provide are displayed on your product details page in the catalog. At minimum, support must be available 8 hours a day, Monday through Friday. The recommended support coverage is 24 hours a day, 7 days a week, and 365 days a year.

Don't add details that have personal information, for example, personal emails.
{: important}

Use the following steps to add support details for your product:

1. From the Partner Center Support tab, provide your product's support statement.

   For the support statement, describe the provided support for your product and Add any additional support information that isn't provided in the other fields.
   {: note}

1. Click **Add support details**, provide your support availability, then click **Save** to add each detail. You must add at least 1 support detail for your product.

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

If your product is already published to the {{site.data.keyword.cloud_notm}} catalog, but you need to update your support details, you can easily do that by editing your published information and requesting an approval for them.

To update your support information, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My products**.
1. Select your product and click **Support**.
1. Click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit") for the field that you want to update.
1. Click **Save**.

    You can revert to the published state of your support information by clicking **Revert changes**.
    {: note}

1. Click **Request approval** when you're ready with your updates. The approval can take at least five business days.
1. After your request is reviewed and approved by the {{site.data.keyword.cloud_notm}} team, publish your changes by clicking **Publish approved changes**.

    Any changes that you don't publish are deleted after 60 days.
    {: important}

You can toggle between the updated and the published state of your support information. Toggle the switch on to review your updates, and toggle the switch off for the published state.

## Define IAM access
{: #define-IAM-access}
{: step}

After you configure your deployment values, you can add the service access and platform access roles that are required to install your product from the {{site.data.keyword.IBM_notm}} catalog.

Use the following steps to define your product's access:
{: #steps-define-desc-iam-access}

1. Click **Configure version** > **Next** > **Next**.
2. Click **Add**.
3. Select the service and the required service and platform access.
   * The service access role allows access for using the service and performing service API calls.
   * The platform access role enables actions to be performed on platform resources, such as creating an instance, connecting instances to apps, and assigning user access.
4. Click **Save**.
{: #steps-define-IAM-access}


## Edit output value descriptions
{: #output-values}
{: step}

You can improve the descriptions for your Terraform template's output values to help users better understand the purpose of the parameters. The description of any output value that you include in your template can be updated.
{: #description-output-values}

To add output values, you need to include them in a new imported version of your Terraform template.
{: note}
{: #note-output-values}

Complete the following steps to edit the product's output value descriptions:
{: #steps-desc-output-values}

1. Click **Configure version** > **Next**.
1. From the Output value descriptions section, provide a new description for the parameter that you want to update.
1. Click **Next**.
{: #steps-output-value}
