---

copyright:
  years: 2021, 2023

lastupdated: "2023-10-19"

keywords: onboard software, third-party software, sell on IBM Cloud, partner center, register, Red Hat OpenShift, cluster, Node-RED Operator, Kubernetes cluster, operator

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 5m

---

{{site.data.keyword.attribute-definition-list}}


# Registering an Operator
{: #operator-register}
{: toc-content-type="tutorial"}
{: toc-completion-time="5m"}

This tutorial walks you through how to register a Node-RED Operator in {{site.data.keyword.cloud}} Partner Center. You can onboard an Operator bundle using a TGZ file or an Operator using a CSV file. By completing this tutorial, you learn how to provide your company details, create a test environment, and set up access for your team to help with the onboarding process.
{: shortdesc}

This tutorial is one of four in a series that demonstrates how to onboard and publish a [sample Node-RED Operator](https://github.com/IBM-Cloud/operator-bundle-sample/releases){: external}. It uses a fictitious company that's called *Example Corp*. As you complete the tutorial, adapt each step to fit your product's needs.

## Before you begin
{: #operator-reg-prereqs}

1. Verify that you're using a Pay-As-You-Go or Subscription account by going to **Manage** > **Account** > **Account settings** in the {{site.data.keyword.cloud_notm}} console.
1. Verify that you're assigned the administrator role on all account management services and all IAM-enabled services. For more information, see [Assigning access to account management services](/docs/account?topic=account-account-services) and [Managing access to resources](/docs/account?topic=account-assign-access-resources).

## Provide your company name
{: #operator-reg-company}
{: step}

1.  In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Overview** > **Get started**.
1. Enter the name of your company as you want it to be displayed in the catalog, and click **Save**. For the purpose of this tutorial, enter `Example Corp` as the company name.

## Create your test environment
{: #operator-reg-test}
{: step}

You, or a member of your team, uses the test environment to onboard the Operator and validate that it can be deployed to a Red Hat OpenShift cluster. Your test environment includes a private catalog in which you import the Operator from an external repository.

1. Click **Create** in the Create your test environment section.
1. Enter `Example Corp Catalog` as the name of the private catalog, and click **Create**.

## Set up access for your team
{: #operator-reg-access}
{: step}

You can enlist team members to help with the onboarding process by assigning them specific levels of {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) access. Create an access group to streamline the process of assigning access.

1. Click **Assign** in the Assign access section.
1. Enter `Example Corp Operator` as the name of the access group, and click **Assign**. The following roles are assigned to the access group by default:

    * Administrator on the Catalog Management service
    * Editor on the Partner Center - Sell service
    * Editor on the User Management service
    * Editor on the IAM Access Groups service
    * Viewer on all account management services

For more information about the actions associated with each role, see [Actions and roles for account management services](/docs/account?topic=account-account-services&interface=ui#account-management-actions-roles).

## Add team members to your account
{: #operators-reg-invite}
{: step}

After you create the `Example Corp Operator` access group, you're ready to add team members to your account and access group. Team members are granted the following editor permissions by default:

* Partner Center - Sell: Complete onboarding tasks, update the visibility of products at the account level, and request approval to publish products to the {{site.data.keyword.cloud_notm}} catalog.
* Private catalog: Onboard products to private catalogs, update the visibility of products at the account and private catalog levels, and restrict the visibility of products in the {{site.data.keyword.cloud_notm}} catalog.

1. Click **Invite** in the Invite team members section.
1. Select the user type:

    * Business: A team member who can provide certain details, such as the product logo, description, and customer support experience.
    * Technical: A team member who can import the product to your test environment, configure the deployment details, and validate it's ready for use.

1. Enter the email address of each team member.
1. Click **Invite**.

## Next steps
{: #operator-reg-next}

You're ready to start the onboarding process. In the Onboard your product section, click **Let's go**, and [define the product details for the Operator](/docs/sell?topic=sell-operator-define).
