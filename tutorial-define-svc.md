---

copyright:
  years: 2021, 2022

lastupdated: "2022-05-04"

keywords: onboard, SaaS, third-party service, sell on IBM Cloud, partner center, product details, catalog entry, support, pricing, catalog, service name, display name, customize, programmatic name

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 10m 

---

{{site.data.keyword.attribute-definition-list}}


# Define the product details of your service
{: #svc-define}
{: toc-content-type="tutorial"} 
{: toc-completion-time="10m"} 

This tutorial walks you through the steps for defining specific details about your service in {{site.data.keyword.cloud}} Partner Center. By completing this tutorial, you review and sign the {{site.data.keyword.IBM}} Digital Provider Agreement, customize your catalog entry and product page, and define support experience.  
{: shortdesc}

This tutorial is one of five in a series that demonstrates how to onboard and publish a service to the {{site.data.keyword.cloud_notm}} catalog. It uses a fictitious company that's called *Example Corp*. As you complete the tutorial, adapt each step to fit your needs.

## Before you begin
{: #svc-define-prereqs}

[Register your service in Partner Center](/docs/sell?topic=sell-svc-register).

## Confirm the digital provider agreement
{: #svc-dpa}
{: step}

As a third-party provider who offers a free plan, you're required to sign the {{site.data.keyword.IBM_notm}} Digital Provider Agreement, which sets the terms and conditions under which you can onboard and sell products in {{site.data.keyword.cloud_notm}}. Or, you can upload a custom digital provider agreement in `.pdf`, `.doc`, or `.docx` file format.

Custom digital provider agreements must be reviewed and approved by {{site.data.keyword.IBM_notm}}, which increases the time it takes for you to complete the onboarding process. The uploaded files are scanned for viruses, which might take a few minutes to complete. If a virus is detected, it is recommended to run another virus scan on your file, and then try uploading it again.
{: note}

For the purposes of this tutorial, complete the following steps to sign the {{site.data.keyword.IBM_notm}} Digital Provider Agreement. 

1. From the My products page in {{site.data.keyword.cloud_notm}} Partner Center, click **Provide details** in the notification that prompts you to complete the Digital Provider Agreement requirement.
1. Click **Edit**. 
1. Click **I plan to offer free pricing plans**.
1. Click the **{{site.data.keyword.IBM_notm}} Digital Provider Agreement** link to review the agreement. 
1. Select **I understand and agree to the {{site.data.keyword.IBM_notm}} Digital Provider Agreement**, and click **Save**.

## Provide your service name and type
{: #svc-name}
{: step}

When you add a product, you can add a new product or import an existing product from a private catalog. For the purposes of this tutorial, add a new product.  

1. Click **My Products** > **Create**. 
1. Enter the name of your product, for example, `Example Corp SaaS Product`. Make sure that the name you enter meets the following requirements:
  
   * Use 60 characters or less.
   * Don't include "{{site.data.keyword.cloud_notm}}".
   * Don't include the name of your company, former product names, or pricing details.

1. Select **Software as a Service** as the type of product that you're onboarding, and click **Add**.

    The product type that you select is used for tax assessment purposes. 
    {: important}

## Confirm your display name and programmatic name for approval
{: #svc-progname-review}
{: step}

Your programmatic name is different than the name that you provided in the previous step. It's automatically generated for you and includes your company name. If your company offers multiple products in {{site.data.keyword.cloud_notm}}, the value of each service name includes both the company name and product name.

Your programmatic name must be approved to create your pricing plans or registering your service broker. You can review and make updates to your programmatic name before you submit it for approval. 

Your programmatic name can't be updated after you submit it for review.
{: important}

1. From the Dashboard tab, click **Edit**, enter your updates, and click **Save**.
1. Click **Confirm**.  

## Create your service ID
{: #svc-service-id}
{: step}

After your programmatic name is review, you can create your service ID. A service ID is used to identify your service when you communicate with other {{site.data.keyword.cloud_notm}} services, for example, when you submit metering usage data for your service. For more information, see [Creating and working with service IDs](/docs/account?topic=account-serviceids&interface=ui).

You're also required to create an API key for your service ID. To create your API key, see [Creating an API key for a service ID](/docs/account?topic=account-serviceidapikeys&interface=ui#create_service_key).


## Provide details for your product
{: #svc-catalog}
{: step}

When your service is published in the catalog, it's represented by a catalog entry and a product page. The contents of your catalog entry include your company or product logo, and a short description. The contents of your product page include a list of features, a detailed description, a link to your product's warranted documentation, and a description of your customer support experience. 

1. Click **Product details**, and enter the URL to your company or product logo, for example `http://svgur.com/i/TTP.svg`.
1. Add a company logo.
1. Provide a short description about your service.
1. From the **Category** list, select the option that best fits how users might use your product, for example, **Databases**. Categories are used to organize similar products in the catalog based on common solutions, function, or use.
1. Select **Third party** from the Provider list.
1. Enter keywords that users might use when they search the catalog for your service.
1. Provide the URL to the end user license agreement (EULA) that users must agree with to use your product.
1. Provide a list of features that highlights your service's attributes and benefits for users.

   Use a descriptive title and 1 - 2 sentences for each feature. You want the information to be visually scannable for users.
   {: tip}

1. Provide a detailed description of your product that explains its value and what users gain by using it. The detailed description is displayed at the beginning of your product page in the catalog. You can expand on the short description that you provide for your catalog entry, but don't repeat it. 
1. Provide links to high-quality images or videos to help illustrate what your product is, its value, and user benefits. The supported media types are images, videos in MP4 or WebM file format, and videos hosted on YouTube or Vimeo.

   Some examples of effective media include an introductory walkthrough of your product, an explanation of what your product is and why users might want to use it, or a comparison of certain features. 
   {: tip}

1. Provide a link to documentation that helps users understand and learn more about how to use your service.

## Define your support experience
{: #svc-support}
{: step}

Provide details that help users understand how to get support if they encounter issues when they use the service. Also, describe how customers can contact your support team to escalate issues that are not handled by the standard support process.

1. Click **Support**, and enter the URL to your support website, for example, `https://support.examplecorp.com/`.
2. For your support contact and response process, describe what users can expect when they contact your support team, for example:

   `Contact Example Corp Support online at https://support.examplecorp.com, by chat at https://support.examplecorp.com/chat, or by phone at https://support.examplecorp.com/phone. Support is available 24 hours a day, 7 days a week, 365 days a year and is provided in English and French.`
  
3. Enter or select all the countries in which support for your product is based.
4. Describe the process that customers follow when they need to escalate issues, for example:

   `For escalation discussions, IBM Cloud customers should follow the escalation process described at https://support.examplecorp.com/ibmcloudescalations.`
  
5. Describe how customers can contact your support team when they escalate an issue, for example:

   `For escalation discussions, {{site.data.keyword.cloud_notm}} support leaders can reach out to the following Example Corp support leaders: Jane Doe (janedoe@examplecorp.com) and John Doe (johndoe@examplecorp.com).`

## Next steps 
{: #svc-pricing-next}

You can now [add your broker](/docs/sell?topic=sell-broker-onboard). 
