---

copyright:
  years: 2023
lastupdated: "2023-10-19"

keywords: onboard software, third-party software, sell on IBM Cloud, partner center, virtual server image, vpc, vsi, register, virtual private cloud

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 5m

---

{{site.data.keyword.attribute-definition-list}}


# Registering a virtual server image for VPC
{: #vsivpc-register}
{: toc-content-type="tutorial"}
{: toc-completion-time="5m"}

This tutorial walks you through how to register a sample virtual server image for virtual private cloud (VPC) to your account. By completing this tutorial, you learn how to create a private catalog, import the image, validate that it can be installed on a selected deployment target, and make the virtual server image available to users who have access to your account.
{: shortdesc}

This tutorial is one of four in a series that demonstrates how to onboard and publish a sample virtual server image for virtual private cloud (VPC). It uses a fictitious company that's called *Example Corp*. As you complete the tutorial, adapt each step to fit your product's needs.

## Before you begin
{: #vsivpc-reg-prereqs}

Before you register a virtual server image for VPC, make sure that you do the following:

1. Verify that you're using a Pay-As-You-Go or Subscription account by going to **Manage** > **Account** > **Account settings** in the {{site.data.keyword.cloud_notm}} console.
1. Verify that you're assigned the administrator role on all account management services and all IAM-enabled services. For more information, see [Assigning access to account management services](/docs/account?topic=account-account-services) and [Managing access to resources](/docs/account?topic=account-assign-access-resources).

## Provide the company name
{: #vsivpc-reg-company}
{: step}

1.  In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Overview**, then click **Get started**.
2. Enter the name of your company as you want it to be displayed in the catalog, and click **Save**. For this tutorial, enter `Example Corp` as the company name.

## Create your test environment
{: #vsivpc-reg-test}
{: step}

You, or a member of your team, uses the test environment to onboard the virtual server image and validate that it can be deployed to your VPC. Your test environment includes a private catalog in which you import the virtual server image from an external repository.

1. Click **Create** in the Create your test environment section.
1. Enter `Example Corp Catalog` as the name of the private catalog, and click **Create**.

## Set up access for your team
{: #vsivpc-reg-ag}
{: step}

You can enlist team members to help with the onboarding process by assigning them specific levels of {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) access. To streamline the process of assigning access, complete the following steps to create your access group:

1. Click **Assign** in the Assign access section.
1. Enter `Example Corp Virtual Server Image` as the name of the access group, and click **Create**. The following roles are assigned to the access group by default:

    * Administrator on the Catalog Management service
    * Editor on the Partner Center - Sell service
    * Editor on the User Management service
    * Editor on the IAM Access Groups service
    * Viewer on all account management services

    For more information about the actions associated with each role, see [Actions and roles for account management services](/docs/account?topic=account-account-services&interface=ui#account-management-actions-roles).

## Invite team members to your account
{: #vsivpc-reg-invite}
{: step}

After you create the `Example Corp Virtual Server Image` access group, you're ready to invite team members to your account and add them to your access group. Team members are granted the following editor permissions by default:

* Partner Center - Sell: Complete onboarding tasks, update the visibility of products at the account level, and request approval to publish products to the {{site.data.keyword.cloud_notm}} catalog.
* Private catalog: Onboard products to private catalogs, update the visibility of products at the account and private catalog levels, and restrict the visibility of products in the {{site.data.keyword.cloud_notm}} catalog.

To invite team members to your account, complete the following steps:

1. Go to **Partner Center > My team**.
1. Click **Invite users**.
1. Enter the email address of the user that you want to invite.
1. Click the checkbox if the user that you invite is a technical team member who will be doing technical tasks.
1. Click **Invite**.

## Next steps
{: #vsivpc-reg-next}

You're ready to start the onboarding process. In the Onboard your product section, click **Let's go**, and [define the product details of the virtual server image for VPC](/docs/sell?topic=sell-vsivpc-define).
