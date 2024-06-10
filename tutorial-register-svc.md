---

copyright:
  years: 2021, 2024
lastupdated: "2024-06-10"

keywords: onboard service, third-party service, sell on IBM Cloud, partner center, register

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 5m

---

{{site.data.keyword.attribute-definition-list}}


# Register your service
{: #svc-register}
{: toc-content-type="tutorial"}
{: toc-completion-time="5m"}

This tutorial walks you through how to register a service in {{site.data.keyword.cloud}} Partner Center. By completing this tutorial, you learn how to provide your company details, create a test environment, and grant team members access to help with the onboarding process
{: shortdesc}

This tutorial is one of five in a series that demonstrates how to onboard and publish a service to the {{site.data.keyword.cloud_notm}} catalog. It uses a fictitious company that's called *Example Corp*. As you complete the tutorial, adapt each step to fit your needs.

## Before you begin
{: #svc-reg-prereqs}

1. Verify that you're using a Pay-As-You-Go or Subscription account by going to **Manage** > **Account** > **Account settings** in the {{site.data.keyword.cloud_notm}} console.
1. Verify that you're assigned the administrator role on all account management services and all IAM-enabled services. For more information, see [Assigning access to account management services](/docs/account?topic=account-account-services) and [Managing access to resources](/docs/account?topic=account-assign-access-resources).

## Provide your company name
{: #svc-reg-company}
{: step}

1.  In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Overview** > **Get started**.
2. Enter the name of your company as you want it to be displayed in the catalog, and click **Save**. For the purpose of this tutorial, enter `Example Corp` as the company name.

## Create your test environment
{: #svc-reg-test}
{: step}

A test environment is not needed for onboarding services but is needed for any software that you might onboard in the future. You, or a member of your team, uses the test environment to validate that your software is ready for use.

1. Click **Create** in the Create your test environment section.
1. Enter `Example Corp Catalog` as the name of the private catalog, and click **Create**.

## Set up access for your team
{: #svc-reg-ag}
{: step}

You can enlist team members to help with the onboarding process by assigning them specific levels of {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) access. To streamline the process of assigning access, complete the following steps to create your access group:

1. Click **Assign** in the Assign access section.
1. Enter `Example Corp Service` as the name of the access group, and click **Create**. The following roles are assigned to the access group by default:

    * Administrator on the Catalog Management service
    * Editor on the Partner Center - Sell service
    * Editor on the User Management service
    * Editor on the IAM Access Groups service
    * Viewer on all account management services

    For more information about the actions associated with each role, see [Actions and roles for account management services](/docs/account?topic=account-account-services&interface=ui#account-management-actions-roles).

## Next steps
{: #svc-reg-next}

You're now ready to [define your service details](/docs/sell?topic=sell-svc-define). Click **Let's go** to continue.
