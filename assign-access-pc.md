---


copyright:
  years: 2022, 2025
lastupdated: "2025-09-19"

keywords: IAM, access, service, third-party, Partner Center Sell, access group, roles

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Managing access for Partner Center - Sell
{: #iam-access-pc-sell}

When you onboard your product to {{site.data.keyword.cloud}} in Partner Center, you can invite your team members to help you with the onboarding process. Setting up your team from Partner Center creates an access group for your team members, which gives them the required access to complete the onboarding tasks. Managing the access of your team members can be easily done in Partner Center, since the tool automatically assigns all the roles to the members of your access group that are needed for product onboarding.
{: shortdesc}

## Before you begin
{: #prereqs-access-pc}

Before you can create an access group, you must complete the following tasks:

1. [Provide your company name](/docs/sell?topic=sell-get-started&interface=ui#step1-register)
1. [Create a test environment](/docs/sell?topic=sell-get-started&interface=ui#step2-testenv)

## Giving team members access in Partner Center
{: #give-access-pc}

If you’re new to Partner Center and you first start onboarding your product, you can give your team members access to help you with the onboarding process. Partner Center automatically assigns the required list of roles to the members of your access group to complete the onboarding tasks, so you don’t need to take any other action.

To create an access group for your team, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Overview** > **Get started**.
1. Click **Assign** in the Assign access section.
1. Enter the name of the access group, and click **Assign**. Members of this group are assigned the following roles:

    * Administrator on the IAM Identity Service for each of your service IDs that is created through Partner Center.
    * Administrator on the Catalog Management service for your private catalog that you created in Partner Center, or imported to Partner Center.
    * Administrator on the Global Resource Catalog service to change the object metadata or visibility for private services, and restrict visibility of a public service.
    * Editor on the User Management service to view, invite, remove, and update users from your account. With this role, you are also able to view and update user profile settings.
    * Editor on the IAM Identity Service to create new service IDs.
    * Editor on the Partner Center - Sell service to view and update products in Partner Center.
    * Editor on the created IAM access group to add and remove users from the access group.
    * Editor on All Identity and Access enabled services in your default resource group to be able to edit and manage broker registration entries.
    * Viewer on All Account Management services to complete all actions for the account management services.

    For more information about the actions associated with each role, see [Actions and roles for account management services](/docs/account?topic=account-account-services&interface=ui#account-management-actions-roles).

1. Click **Let's go**.

If you're in the middle of onboarding your product in Partner Center, you can still give your team members access to your account by completing the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My team**.
1. Click **Invite users**.
1. Enter the email address of each user.
1. Click **Invite**.

## Managing access in Partner Center
{: #manage-access-in-pc}

If you no longer want users to be part of your team and help you onboard your product, you can remove them by completing the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My team**.
1. Click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg "Actions") for the user that you want to remove, and select **Remove**.
1. Click **Confirm**.

Optionally, you can set a primary contact for your team, who is set as the main email contact of your product and receives the product-related email notifications. Complete the following steps to set a primary contact:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My team**.
1. Click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg "Actions") for the user that you want to make as a primary contact, and select **Set as primary contact**.
1. Click **Confirm**.

## Managing access in {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM)
{: #review-access-in-iam}

The easiest way to manage access for your team is through Partner Center by following the steps in the [Giving team members access in Partner Center](#give-access-pc) section, but you can also add, or remove users in {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM). In IAM, you can review the list of users in your access group and the list of roles that Partner Center assigned your access group automatically. Additionally, you can find the list of service IDs, trusted profiles, and dynamic rules that the access group has.

To manage and review your access group in IAM, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My team**.
1. Click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg "Actions") for any user in your team, and select **Manage access group**. This step takes you to IAM, where you can manage access and review extended information about your access group.
1. Click **Add users** to add a user to your access group.
1. If you want to remove a user from your access group, click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg "Actions") for the user that you want to remove, and select **Remove**.

Don't delete the access group or modify the roles and policies in it. Partner Center uses the access group, and all policies are needed for your team members to be able to manage a successful product onboarding.
{: important}
