---

copyright:
  years: 2020, 2023

lastupdated: "2023-10-19"

keywords: onboard software, third-party software, getting started, software, partner, sellers, partner portal, partner center

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 10m

---

{{site.data.keyword.attribute-definition-list}}


# Getting set up to sell software
{: #sw-getting-started}
{: toc-content-type="tutorial"}
{: toc-completion-time="10m"}

Welcome to {{site.data.keyword.cloud}}! To start onboarding your software to our cloud platform, first complete a few tasks: provide your company and product details, create a test environment, and set up access for your team to help with the onboarding process.
{: shortdesc}

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

## Before you begin
{: #sw-getstart-prereqs}

* Verify that you're using a Pay-As-You-Go or Subscription account. To check which type of account you're using, go to **Manage > Account > Account settings** in the {{site.data.keyword.cloud_notm}} console.

   It's recommended that you use an account that was created with a [functional ID](/docs/account?topic=account-identity-overview#functionalid-bestpract) to ensure your continued access to the products that are onboarded in the account.
   {: tip}

* Verify that you're assigned the administrator role on all account management services and all IAM-enabled services. See [Assigning access to account management services](/docs/account?topic=account-account-services) and [Managing access to resources](/docs/account?topic=account-assign-access-resources).
* Review the list of supported software:

    * Helm charts on Kubernetes and {{site.data.keyword.openshiftshort}} clusters
    * Terraform templates
    * OVA images deployed on VMware Solutions Dedicated - vCenter Server
    * Virtual server images with Terraform deployed on VPC infrastructure
    * Custom virtual server images deployed on VPC infrastructure

       Onboarding Virtual Server Images for VPC with {{site.data.keyword.IBMz}} deployment support is available in private catalogs. The onboarding experience for {{site.data.keyword.IBMz_notm}}-supported Virtual Server Images is the same as how you onboard other Virtual Server Images in your private catalog.
       {: note}

    * Operators with a TGZ file from GitHub or GitLab repositories
    * Operator bundles from Red Hat OpenShift registries

## Provide your company name
{: #sw-company-product}
{: step}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center > Overview > Get started**.
1. Enter the name of your company as you want it to be displayed in the {{site.data.keyword.cloud_notm}} catalog.

    The company name doesn't need to be finalized. You can update it later from the My company page in Partner Center if necessary.
    {: tip}

## Create a test environment
{: #sw-create-testenv}
{: step}

You, or a member of your team, uses the test environment to onboard your product, and validate that it's ready to be published in the {{site.data.keyword.cloud_notm}} catalog. Your test environment includes a private catalog in which you import your product from an external repository.

1. Click **Create** in the Create your test environment section on the Get started page.
1. Enter the name of your private catalog, and click **Create**. The private catalog and its contents are visible only to the users you choose.

## Set up team access
{: #sw-team-access}
{: step}

If you want to enlist team members to help with the onboarding process, you need to assign them specific levels of {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) access. To streamline the process, you can organize your team members into a single entity by adding them to an access group.

1. Click **Assign** in the Assign access section on the Get started page.
1. Enter the name of the access group, and click **Create**. Members of this group are assigned the following roles by default:

    * Administrator on the catalog management service
    * Editor on the Partner Center - Sell service
    * Editor on the user management service
    * Editor on the IAM access groups service
    * Viewer on all account management services

    For more information about the actions associated with each role, see [Actions and roles for account management services](/docs/account?topic=account-account-services&interface=ui#account-management-actions-roles).

1. Click **Let's go**.

## Invite team members to your account
{: #sw-invite-member}
{: step}

After you create your access group, you can add team members to the group by inviting them to your account.

1. Go to **Partner Center > My team**.
1. Click **Invite users**.
1. Enter the email address of the user that you want to invite.
1. Click the checkbox if the user that you invite is a technical team member who will be doing technical tasks.
1. Click **Invite**.

## Next steps
{: #sw-getstart-next}

Now that you completed the getting started tasks, you're ready to [continue with the onboarding process](/docs/sell?topic=sell-sw-partner-details).

To get an overview of all the tasks involved in the process, see [Checklist for selling software on {{site.data.keyword.cloud_notm}}](/docs/sell?topic=sell-checklist-software).
{: tip}
