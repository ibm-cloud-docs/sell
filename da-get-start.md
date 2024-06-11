---

copyright:
  years: 2023

lastupdated: "2023-10-18"

keywords: onboard deployable architecture, third-party deployable architecture, getting started, deployable architecture, partner, sellers, partner portal, partner center, partner center sell

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 10m

---

{{site.data.keyword.attribute-definition-list}}


# Getting set up to sell deployable architectures
{: #da-getting-started}
{: toc-content-type="tutorial"}
{: toc-completion-time="10m"}

Welcome to {{site.data.keyword.cloud}}! To start onboarding your deployable architecture to our cloud platform, first complete a few tasks: provide your company and product details, create a test environment, set up access for your team to help with the onboarding process, and confirm your legal agreement with {{site.data.keyword.IBM_notm}}.
{: shortdesc}

## Before you begin
{: #da-getstart-prereqs}

* Verify that you're using a Pay-As-You-Go or Subscription account. To check which type of account you're using, go to **Manage > Account > Account settings** in the {{site.data.keyword.cloud_notm}} console.

   It's recommended that you use an account that was created with a [functional ID](/docs/account?topic=account-identity-overview#functionalid-bestpract) to ensure your continued access to the products that are onboarded in the account.
   {: tip}

* Verify that you're assigned the administrator role on all account management services and all IAM-enabled services. See [Assigning access to account management services](/docs/account?topic=account-account-services) and [Managing access to resources](/docs/account?topic=account-assign-access-resources).

* The only supported deployable architecture type is Terraform.

## Provide your company name
{: #da-company-product}
{: step}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center > Overview > Get started**.
1. Enter the name of your company as you want it to be displayed in the {{site.data.keyword.cloud_notm}} catalog.

    The company name doesn't need to be finalized. You can update it later from the My company page in Partner Center if necessary.
    {: tip}

## Create a test environment
{: #da-create-testenv}
{: step}

You, or a member of your team, uses the test environment to onboard your product, and validate that it's ready to be published in the {{site.data.keyword.cloud_notm}} catalog. Your test environment includes a private catalog in which you import your product from an external repository.

1. Click **Create** in the Create your test environment section on the Get started page.
1. Enter the name of your private catalog, and click **Create**. The private catalog and its contents are visible only to the users that you choose.

## Set up team access
{: #da-team-access}
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
{: #da-invite-member}
{: step}

After you create your access group, you can add team members to the group by inviting them to your account.

1. Go to **Partner Center > My team**.
1. Click **Invite users**.
1. Enter the email address of the user that you want to invite.
1. Click the checkbox if the user that you invite is a technical team member who will be doing technical tasks.
1. Click **Invite**.

## Review and submit the digital platform reseller agreement
{: #da-agreement}
{: step}

You are required to review and submit the {{site.data.keyword.IBM_notm}} Digital Platform Reseller Agreement, which sets the terms and conditions under which providers can onboard and sell products in {{site.data.keyword.cloud_notm}}. Or, you can upload a custom digital provider agreement in `.pdf`, `.doc`, or `.docx` file format.

Custom digital provider agreements must be reviewed and approved by {{site.data.keyword.IBM_notm}}, which increases the time it takes for you to complete the onboarding process. The uploaded files are scanned for viruses, which might take a few minutes to complete. If a virus is detected, it is recommended to run another virus scan on your file, and then try uploading it again.
{: note}

Complete the following steps to review and submit the {{site.data.keyword.IBM_notm}} Digital Platform Reseller Agreement:

1. Go to **Partner Center > My company**.
1. Click **Edit**.
1. Choose **I plan to offer usage-based pricing plans** from the Agreements section.
1. Click the **{{site.data.keyword.IBM_notm}} Digital Platform Reseller Agreement** link to review the agreement.
1. Select **I read and agree to the {{site.data.keyword.IBM_notm}} Digital Platform Reseller Agreement**, and click **Save**.

## Next steps
{: #da-getstart-next}

Now that you completed the getting started tasks, you're ready to [continue with the onboarding process](/docs/sell?topic=sell-create-da-product&interface=ui).

To get an overview of all the tasks involved in the process, see the [checklist for selling deployable architectures on {{site.data.keyword.cloud_notm}}](/docs/sell?topic=sell-checklist-da&interface=ui).
{: tip}
