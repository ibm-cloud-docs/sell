---

copyright:

  years: 2020, 2021

lastupdated: "2021-10-12"

keywords: end-to-end, software onboarding, checklist, third party, requirements, sellers, partner portal, partners, third-party software, partner center

subcollection: sell

---

{:right: .ph data-hd-position='right'}
{:shortdesc: .shortdesc}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:beta: .beta}
{:term: .term}
{:external: target="_blank" .external}
{:video: .video}

# Checklist for selling software on {{site.data.keyword.cloud_notm}}
{: #checklist-software}

Use the following checklist to track all the tasks that are required to successfully onboard and sell your third-party software on {{site.data.keyword.cloud}}.
{: shortdesc}

The process to sell third-party products is still under development. With the current release, you can bring your own licenses or deliver your product for free. If you have questions, contact us at cloud.onboarding@ibm.com.
{: beta}

## Before you begin
{: #sw-software-type}

Review the list of supported software:
  
* Helm charts on Kubernetes and {{site.data.keyword.redhat_notm}} {{site.data.keyword.openshiftshort}} clusters
* Terraform templates
* OVA images deployed on VMware vCenter Server
* Virtual server images with Terraform deployed on VPC infrastructure
* Operators with a CSV file or Operator bundles with a TGZ file from GitHub repositories deployed on Red Hat OpenShift
* Operator bundles from Red Hat OpenShift registries

## Watch and learn
{: #onboard-software}

Onboarding software to {{site.data.keyword.cloud_notm}} involves four major steps: registering in Partner Center, customizing your product details for the {{site.data.keyword.cloud_notm}} catalog, testing and validating your product, and, finally, publishing your product. Check out the following video for a walk-through of the complete process.

![Selling on IBM Cloud](https://video.ibm.com/embed/channel/23952684/video/sell-on-ibm-cloud){: video output="iframe" data-script="#onboard-software-script" id="watsonmediaplayer" width="560" height="315" scrolling="no" allowfullscreen webkitallowfullscreen mozAllowFullScreen frameborder="0" style="border: 0 none transparent;"}

### Video transcript
{: #onboard-software-script}
{: notoc}

By onboarding and selling your product on {{site.data.keyword.cloud_notm}}, you can grow your business and expand your reach to clients globally, by leveraging {{site.data.keyword.IBM_notm}}'s trusted relationships with fortune 500 enterprises. You can accelerate your time to market and gain a competitive edge, all while taking advantage of flexible, secure options across open source and compute technologies. 

Onboarding your product involves four major steps - registering in Partner Center, customizing your product details, testing and validating your product, and, finally, publishing your product. In this demo, we’ll focus on using a Terraform template as the delivery method. 

Get started by heading to Partner Center in the {{site.data.keyword.cloud_notm}} console - your one-stop shop for onboarding your product. [Click **My products** on the Partner Center home page to open the Getting started dashboard] 

First, register your product by providing the name of your company and then creating your test environment. This test environment will house your product during the onboarding process. [In the Create your test environment section, click **Create**]
 
Next, if you want team members to help with the onboarding process, get them set up with access to your account. [In the Assign access section, click **Assign** to assign access. Then, click **Let's go**.] 

Confirm your legal agreement with {{site.data.keyword.IBM_notm}}. You can instantly accept the {{site.data.keyword.IBM_notm}} Digital Provider Agreement, or you can upload your own custom agreement, which will need to be reviewed and approved by {{site.data.keyword.IBM_notm}}. [Click **Provide details** then click **Standard** and confirm that you've read and agree to the {{site.data.keyword.IBM_notm}} Digital Provider Agreement.] 

After confirming your agreement, click **Create**, and add the name of your product. [Click **My products** > **Create**] 

Now you’re ready to customize your product for the catalog. The information that you provide on the Product details tab is displayed in two places: your catalog tile and your detailed product page. For your catalog entry, provide a link to your company or product logo and a description of your product. To help users find your software in the catalog, select the category that best fits your product. [Click **Product details**. Then, click **Add logo** to add a link to your logo. Then, click **Summarize what the product is and its value** to enter a description of your product. Then, click **Select category** and select **Developer tools**.]   
 
Next, select the third-party provider type. You can also enter keywords to help users find your product in the catalog.
For your product page, provide a list of features that users can quickly scan to get an overview of what it’s all about. [Click **Add a list of product features**.]
 
Then, provide a detailed description that explains its value in more detail. [Click **Enter text that explains the product's value and benefits to users**.] 
 
Provide links to high-quality images or videos, and, finally, provide a link to your official documentation. [Click **Add media** to add images or videos. Click **Add your documentation URL** to add a link to your official documentation. ]

Next, define your pricing model. Currently, you can select a free plan or a bring your own license plan. Note that a bring your own license, or BYOL plan requires a URL to the license. [Click **Pricing** and select the Free pricing model.]

Head over to the Support tab and define your support experience. First, provide details that explain how users can get self-help, open support cases, and engage directly in real time with your support team. [Click **Support**. Then, click **Provide URL** to add your support site URL. Click **Describe process for responding to support issues** to describe the support process. Then, click **Provide the countries in which support is available** to add support locations.]
 
Next, explain how {{site.data.keyword.cloud_notm}} Support leaders can contact your support team leaders. [Click **Describe process for {{site.data.keyword.cloud_notm}} response to support issues** and provide a description of the support process. Click **Provide support contact information** to share the support contacts with {{site.data.keyword.IBM_notm}}.]

From the Software tab, import a version of your product to the test environment that you created when you registered your product. [Click **Software**. Then, click **Import a version**.] 
 
Choose your delivery method and select your source repository type – either public or private – and provide the URL to it. Then, enter the version of your product. After importing your product, you're ready to configure it by adding any required deployment values. [Click **Step 2 - Configure the deployment details** to add deployment values.]

Add links to the license agreements that your users are required to accept when they install your product. [Click **Add license agreements**.]  

Now, you’re ready to validate that your product can be successfully installed on the deployment target. [Click **Validate product**. Click **Next > Next > Validate** to validate your product.] 

Head back to Partner Center and check your progress in the Onboarding checklist. [Once validation is complete, click **Go to Partner Center**.]  
 
At this point, you’ve completed all the required tasks and you’re ready to submit your product for publishing approval. [Click **Request approval**.]  
 
Submitting your request automatically notifies our onboarding team that you’re ready to publish your product to the catalog. We’ll review the details that you provided and either approve your product for publishing, or request some updates. You'll get an email with details about any changes that you might need to make. 

After your product is approved, you're ready to return to Partner Center and publish it. Your software is now live and available to users in the {{site.data.keyword.cloud_notm}} catalog. [Click **Publish**. Click **View in {{site.data.keyword.cloud_notm}} catalog** and search for the name of the product to open it.] 

## Register your product
{: #sw-start-checklist}

The following tasks are typically completed by a team member who is familiar with the business case for the product. 

| Task | Description | Environment |
|------|-------------|-------------|
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Provide your company and product details | Specify the names of your company and product.  | {{site.data.keyword.cloud_notm}} console | 
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Create a test environment | The test environment is used to onboard your software and validate it's ready for use. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Assign team access | With the correct {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) access, members of your team can help onboard your software. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Invite team members to your account | Members of your account are assigned the IAM access that you set up in the previous task.  | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Confirm your legal agreement with {{site.data.keyword.IBM}} | Review and accept the {{site.data.keyword.IBM_notm}} Digital Provider Agreement, or upload your custom digital provider agreement to be reviewed and approved by {{site.data.keyword.IBM}}. | {{site.data.keyword.cloud_notm}} console |
{: caption="Table 1. Getting started tasks for selling software" caption-side="top"} 

For more information, see [Getting set up to sell software](/docs/sell?topic=sell-sw-getting-started). 

## Tell us about your product 
{: #sw-details-checklist}

The following tasks are typically completed by a team member familiar with the business case, marketing details, and customer support experience for the product. 

| Task | Description | Environment |
|------|-------------|-------------|
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Verify your partner details | Review the product name that you provided as part of the getting started tasks to make sure that everything is correct. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Define your product details | Add details, such as your product logo, keywords, description, features, and documentation URL, for your product's entry and details page in the {{site.data.keyword.cloud}} catalog. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Define your customer support experience | Provide details about how users can get help with using your software.  | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Define your pricing information | Choose your pricing plan: free or BYOL. If BYOL, provide details about your license.  | {{site.data.keyword.cloud_notm}} console |
{: caption="Table 2. Tasks for defining software details" caption-side="top"} 

For more information, see the following links:


* [Defining your catalog entry and product page](/docs/sell?topic=sell-sw-catalog-details)
* [Defining your support experience](/docs/sell?topic=sell-sw-support-details)

## Onboard your product
{: #sw-validate-checklist}

The following tasks are typically completed by a technical member of your team. 

| Task | Description | Environment |
|------|-------------|-------------|
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Set up your source code repository | Create a release in your source code repository to deliver and manage versions of your software. | Your GitHub repository |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Upload a readme file | Provide a readme file that describes how users can install your software and get customer support. | Your GitHub repository |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Onboard your software| Import a version, configure the deployment details, set any license requirements, and validate that the version can be successfully installed on the infrastructure that you require. | {{site.data.keyword.cloud_notm}} console |
{: caption="Table 3. Tasks for onboarding software" caption-side="top"} 

For more information, see the following links:

* [Setting up your source code repository](/docs/sell?topic=sell-source-repo-setup)
* [Onboarding your software](/docs/sell?topic=sell-sw-validate)

## Publish your product
{: #sw-publish-checklist}

The following tasks are completed by any member of your team. 

| Task | Description | Environment |
|------|-------------|-------------|
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Verify that all tasks are completed | Confirm that you completed the getting started tasks, defined your software details, and onboarded your software. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Request to publish your software | Submit a request for {{site.data.keyword.cloud_notm}} to review your product details and approve it's ready for publishing. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Publish your software | After your publishing request is approved, publish your software to the {{site.data.keyword.cloud_notm}} catalog. | {{site.data.keyword.cloud_notm}} console |
{: caption="Table 4. Tasks for publishing software" caption-side="top"} 

For more information, see [Publishing your software to the {{site.data.keyword.cloud_notm}} catalog](/docs/sell?topic=sell-sw-publish).

As a third-party provider, you're responsible for maintaining all assets of published software in the {{site.data.keyword.cloud}} catalog and deprecating outdated versions.  
{: note}
