---

copyright:

  years: 2022, 2023

lastupdated: "2023-10-19"

keywords: third-party service, sell on IBM Cloud, resource management console, integrated billing service

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 60m

---

{{site.data.keyword.attribute-definition-list}}

# Getting set up to sell services
{: #get-started}
{: toc-content-type="tutorial"}
{: toc-completion-time="60m"}

Welcome to {{site.data.keyword.cloud}}! To start onboarding your service to our cloud platform, first complete a few tasks: provide your company and product details, create a test environment, and set up access for your team to help with the onboarding process.
{: shortdesc}

It's recommended that you use an account that was created with a [functional ID](/docs/account?topic=account-identity-overview#functionalid-bestpract) to ensure your continued access to the products that are onboarded in the account.
{: tip}

## Watch and learn
{: #selling-services}

Onboarding your product to {{site.data.keyword.cloud_notm}} involves four major steps: registering in Partner Center, customizing your product details, building a service broker and validating your pricing plan, and, finally, publishing your product. Check out the following video for a walk-through of the complete process.

![Selling services on IBM Cloud](https://video.ibm.com/embed/recorded/132523416){: video output="iframe" data-script="#sell-services-script" id="watsonmediaplayer" width="560" height="315" scrolling="no" allowfullscreen webkitallowfullscreen mozAllowFullScreen frameborder="0" style="border: 0 none transparent;"}

### Video transcript
{: #sell-services-script}
{: notoc}

By building, onboarding, and selling your product on {{site.data.keyword.cloud_notm}}, you can grow your business and expand your reach to clients globally. You'll have the advantage of accelerated time to market, along with flexibility and security options that are available across open source technologies as well as computing resources in the cloud.

Onboarding your product involves four major steps:
* Registering in Partner Center
* Customizing your product details
* Building a service broker and validating your pricing plan
* And, finally, publishing your product

Get started by heading to Partner Center - your one-stop shop for onboarding your product. First, register your product by providing the name of your company and then creating your test environment. [On the Get started dashboard, enter your company name, and click **Save**. In the Create your test environment section, click **Create**]

Next, if you want team members to help with the onboarding process, get them set up with access to your account. For example, add a technical team member to create and add your broker. [In the Assign access section, click **Assign** to create an access group. Then, click **Let's go**.]

Confirm your legal agreement with {{site.data.keyword.IBM_notm}}. Or, you can upload your own custom agreement. [Go to the My company page to confirm your legal agreement]

Go back to the My products page and click **Create**. Enter the name of your product, select the product type, and click **Add**.

First, confirm your product's programmatic name, which is automatically generated for you. Your programmatic name must be approved in order to add a pricing plan or register your service broker. [Click **Edit** to change your programmatic name, save it, and click **Confirm**.]

After your programmatic name is approved, {{site.data.keyword.IBM_notm}} generates a service ID, which is used to identify your service when communicating with other {{site.data.keyword.cloud_notm}} services. You’ll need to create an API key for authentication as well.

Now you’re ready to customize your product for the catalog. The information that you provide on the Product details tab is displayed in two places: your catalog tile and your detailed product page. For your catalog entry, provide a logo and a description of your product, along with a category and keywords to help users find your product in the catalog. Next, provide the URL to the end user license agreement that users must agree to in order to use your product. Finish your product page by adding a detailed description and features that highlight your service’s attributes and the benefits to users. Finally, provide links to high-quality images or videos, and your official documentation. [Click **Product details**. Then, click **Add logo** to add a link to your logo. Then, click the Edit icon for the Short description field to enter a description of your product. Then, click **Select category** and select **Developer tools**. Click **Provide the end user license agreement URL customers must agree with to use your product** and enter the URL to your license agreement. Click the Edit icon for the Detailed description field and provide a more detailed description of your product. Click **Add a list of product features** and add your product features. Click **Add your documentation URL** to add a link to your documentation.]

Head over to the Support tab to define your support experience. You can start by selecting how your product is supported, and completing the support statement field. It’s important to explain how users can get self-help, open support cases, and engage directly with your support team in real time. Next, explain how {{site.data.keyword.cloud_notm}} Support leaders can contact your product’s support team leaders. [Click **Support** and select **Third party** as the support provider for your product. Click the Edit icon for the Statement of support field and provide your statement of support. Click the Edit icon for the support site URL to add your support site. Click the Edit icon for the service status URL and add URL. From the Add support details drop down, add an email address, phone number, or other details that your users can use to reach out to you for support. In the Support escalation process section, provide the number of hours that customers must wait before escalating a case. Add the support contact information so {{site.data.keyword.cloud_notm}} can escalate support cases as needed.]

Define your pricing model on the Pricing tab. First, add the Export Control Classification Number and the United Nations Standard Products and Services Code that applies to your product. Next, define your pricing plan. Currently, you can choose a free or usage-based pricing plan. If you’d like, you can add multiple plans for your product. [Click **Pricing** then click **Add ECCN** to add your Export Control Classification Number. Click **Add UNSPSC** to add the United Nations Standard Products and Services Code for your product. Click **Add plan**, select the plan type, add a name, select how resource instances should be deployed, and click **Save**.]

For usage-based plans, you must submit your tax and EFT information to set up and receive payment disbursements for usage. You’ll also want to add metrics to determine how customers are charged, and submit your updates for approval. [The Payments to me page is highlighted. Click **Add metrics** to add your metrics to the pricing plan. In the Metering approval section, click **Request approval**.]

Building one or more service brokers is needed to manage the lifecycle of your service and metering integration. A broker must be added to complete your pricing plan. Your technical team member can get started with our sample broker. Add your broker by entering a name, a URL, a username, and a password. Or, you can import brokers from your account. After you add your broker, link it to your pricing plan. [Click **Brokers**. In the Onboard brokers to {{site.data.keyword.cloud_notm}} section, click **OK** to open the sample reference broker. Click **Add broker** to add your broker. Click **Pricing**, click the actions icon for your pricing plan, and click **Edit plan** to link your broker to your pricing plan.]

Now that you’ve defined your pricing model, review how customers would understand and experience it. After your metering updates are approved, validate that your metered plans are correctly configured by enabling and submitting a usage test. This usage test includes creating your metering JSON, calling the Usage Metering API, and submitting metering evidence. [Click **Add metrics** for the pricing plan you added. Click **Test estimation and metering** to submit your metering evidence for review.]

The next step is to add features that uniquely identify your product’s attributes and differentiate this pricing plan from others. [Click **Add feature** to add more information about your pricing plan.]

Check your progress in the Onboarding checklist to make sure you’ve completed all the required tasks. At this point, you’re ready to submit your product for publishing approval.
Submitting your request automatically notifies our onboarding team. The team will review the product details you provided to approve it for publishing, or they might request additional updates. [Click the name of your service in the breadcrumb menu, and click **Checklist** to open the Onboarding checklist. Click **Request approval** to request publishing approval for your product.]

You'll get an email with details about any changes that you might need to make.

After your product is approved, return to Partner Center and publish it to the {{site.data.keyword.cloud_notm}} catalog. Congratulations, your service is now ready and available to all users in the {{site.data.keyword.cloud_notm}} catalog! [Click **Publish** to publish your service after you receive approval to do so.]

## Before you begin
{: #prereq}

To onboard your services to the {{site.data.keyword.Bluemix_notm}} platform, you must be an approved {{site.data.keyword.Bluemix_notm}} build partner. You can expand your network by receiving access to {{site.data.keyword.IBM_notm}}’s global ecosystem, receive insights to better engage customers, grow your business, and increase revenue. For more information on being an {{site.data.keyword.Bluemix_notm}} build partner, see the [IBM Build Partner](https://www.ibm.com/partnerworld/public/build){: external} page.

Besides being an {{site.data.keyword.Bluemix_notm}} build partner, service onboarding is limited to providers who meet the following prerequisites due to current processing times:

* Providers who leverage one or more services in the {{site.data.keyword.Bluemix_notm}} catalog.
* Providers who intend on selling their product in the {{site.data.keyword.Bluemix_notm}} catalog.

## Provide your company name
{: #step1-register}
{: step}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center > Overview > Get started**.
1. Enter the name of your company as you want it to be displayed in the {{site.data.keyword.cloud_notm}} catalog.

    The company name doesn't need to be finalized. You can update it later from the My company page in Partner Center if necessary.
    {: tip}

## Create a test environment
{: #step2-testenv}
{: step}

A test environment is not needed for onboarding services but is needed for any software that you might onboard in the future. You, or a member of your team, uses the test environment to validate that your software is ready for use.

1. Click **Create** in the Create your test environment section on the Get started page.
1. Enter the name of your private catalog, and click **Create**. The private catalog and its contents are visible only to the users that you choose.

## Set up team access
{: #step3-team-access}
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
{: #sc-step4-invite-member}
{: step}

After you create your access group, you can add team members to the group by inviting them to your account.

1. Go to **Partner Center > My team**.
1. Click **Invite users**.
1. Enter the email address of the user that you want to invite.
1. Click the checkbox if the user that you invite is a technical team member who will be doing technical tasks.
1. Click **Invite**.

## Next steps
{: #gs-next-steps}

Now that you completed the getting started tasks, you're ready to [define the product details of your service](/docs/sell?topic=sell-svc-define).

To get an overview of all the tasks involved in the process, see [Checklist for selling service on {{site.data.keyword.cloud_notm}}](/docs/sell?topic=sell-checklist).
{: tip}
