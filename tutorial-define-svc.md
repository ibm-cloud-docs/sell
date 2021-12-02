---

copyright:
  years: 2021

lastupdated: "2021-12-02"

keywords: onboard, SaaS, third-party service, sell on IBM Cloud, partner center, product details, catalog entry, support, pricing, catalog, service name, display name, customize, programmatic name

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 10m 

---

{{site.data.keyword.attribute-definition-list}}


# Defining the product details of your service
{: #svc-define}
{: toc-content-type="tutorial"} 
{: toc-completion-time="10m"} 

This tutorial walks you through the steps for defining specific details about your service in {{site.data.keyword.cloud}} Partner Center. By completing this tutorial, you review and sign the {{site.data.keyword.IBM}} Digital Provider Agreement, and customize your catalog entry and product page, and support experience.  
{: shortdesc}

The process to sell third-party products in Partner Center is still under development. With the current release, you can offer your product for free. If you're interested in trying it out, contact us at cloud.onboarding@ibm.com.
{: beta}

This tutorial is one of four in a series that demonstrates how to onboard and publish a service to the {{site.data.keyword.cloud_notm}} catalog. It uses a fictitious company that's called *Example Corp*. As you complete the tutorial, adapt each step to fit your needs.

## Before you begin
{: #svc-define-prereqs}

[Register your service in Partner Center](/docs/sell?topic=sell-svc-register).

## Confirm the digital provider agreement
{: #svc-dpa}
{: step}

As a third-party provider, you're required to sign the {{site.data.keyword.IBM_notm}} Digital Provider Agreement, which sets the terms and conditions under which you can onboard and sell products in {{site.data.keyword.cloud_notm}}. Or, you can upload a custom digital provider agreement in `.pdf`, `.doc`, or `.docx` file format.

Custom digital provider agreements must be reviewed and approved by {{site.data.keyword.IBM_notm}}, which increases the time it takes for you to complete the onboarding process. 
{: note}

For the purposes of this tutorial, complete the following steps to sign the {{site.data.keyword.IBM_notm}} Digital Provider Agreement. 

1. From the My products page in {{site.data.keyword.cloud_notm}} Partner Center, click **Provide details** in the notification that prompts you to complete the DPA requirement.
1. Click **Edit**. 
1. Click **Standard** as the DPA type.
1. Click the **{{site.data.keyword.IBM_notm}} Digital Provider Agreement** link to review the agreement. 
1. Select **I understand and agree to the {{site.data.keyword.IBM_notm}} Digital Provider Agreement**, and click **Save**.

## Provide your product name
{: #svc-name}
{: step}

The value that you enter in this step is the name that is displayed in the catalog when your service is publically available. 

1. Click **My Products** > **Create**. 
1. Enter the name of your product, for example, `Example Corp SaaS Product`. Make sure that the name you enter meets the following requirements:
  
* Use 60 characters or less.
* Don't include "{{site.data.keyword.cloud_notm}}".
* Don't include the name of your company, former product names, or pricing details.

1. Select **SaaS** as the type of product that you're onboarding, and click **Create**.

## Submit your display name and service name for approval
{: #svc-progname-review}
{: step}

Your service name is different than the name that you provided in the previous step. It's automatically generated for you, and the value includes your company name. If your company offers multiple products in {{site.data.keyword.cloud_notm}}, the value of each service name includes both the company name and product name.

You have the option to update your product's display name and service name before you start other specific tasks, like testing pricing plans or registering your service broker. Regardless of whether you update either name, both must be approved by the {{site.data.keyword.cloud_notm}} onboarding team.

Your service name can't be updated once you submit it for review.
{: important}

1. (Optional) From the Dashboard tab, click **Edit** > enter your updates, and click **Save**.
1. Click **Request approval**.  







## Provide custom details about your service
{: #svc-catalog}
{: step}

When your service is published in the catalog, it's represented by a catalog entry that serves as the entry point for users to view your full product details and to start building with it. 

* The contents of your catalog entry include your company or product logo and a short description. 
* The contents of your product page include a list of features, a detailed description, a link to your product's warranted documentation, and a description of your customer support experience. 

1. Click **Product details**, and enter the URL to your company or product logo, such as `http://svgur.com/i/TTP.svg`.
1. Provide a short description about your service.
1. From the **Category** list, select an option that best fits how users might use your product, for example, **Databases**. Categories are used to organize similar products in the catalog based on common solutions, function, or use.
1. Select **Third party** from the **Provider** list.
1. Enter keywords that users might use when they search the catalog for your service.
1. Provide a list of features that highlights your service's attributes and benefits for users.

   Use a descriptive title and 1-2 sentences for each feature. You want the information to be visually scannable for users.
   {: tip}

1. Provide a detailed description of your product that explains its value and what users gain by using it. The detailed description is displayed at the beginning of your product page in the catalog. You can expand on the short description that you provide for your catalog entry, but don't simply repeat it. 
1. Provide links to high-quality images or videos to help illustrate what your product is, its value, and user benefits. The supported media types are images, videos in MP4 or WebM file format, and videos hosted on YouTube or Vimeo.

   Some examples of effective media include an introductory walkthrough of your product, an explanation of what your product is and why users might want to use it, or a comparison of certain features. 
   {: tip}

1. Provide a link to documentation that helps users understand and learn more about how to fully use your service.

## Define your support experience
{: #svc-support}
{: step}

Provide details that help users understand how to get support if they encounter issues when using your service. Also, describe how {{site.data.keyword.cloud_notm}} Support team leaders can collaborate with your support team leaders on customer escalations.

1. Click **Support**, and enter the URL to your support website, for example, `https://support.examplecorp.com/`.
2. For your support response process, describe what users can expect when they contact your support team, for example:

   `Contact Example Corp Support online at https://support.examplecorp.com, by chat at https://support.examplecorp.com/chat, or by phone at https://support.examplecorp.com/phone. Support is available 24 hours a day, 7 days a week, 365 days a year and is provided in English and French.`
  
3. Enter or select all the countries in which support for your product is based.
4. Describe the process that {{site.data.keyword.cloud_notm}} Support follows when customers escalate issues that are handled by your support team, for example: 

   `For client escalations, {{site.data.keyword.cloud_notm}} support representatives should follow the escalation process described at https://support.examplecorp.com/ibmcloudescalations.`
  
5. Describe how {{site.data.keyword.cloud_notm}} Support can contact your support team, for example:

   `For support process discussions, {{site.data.keyword.cloud_notm}} support leaders can reach out to the following Example Corp support leaders: Jane Doe (janedoe@examplecorp.com) and John Doe (johndoe@examplecorp.com).`

## Next steps
{: #svc-define-next}

Create your pricing plan. 
