---

copyright:
  years: 2022, 2025
lastupdated: "2025-09-19"

keywords: onboard software, third-party software, sell on IBM Cloud, partner center, virtual server image, virtual machine image, image, vm, vsi, terraform, register, power, power vsi, power systems virtual server

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 5m

---

{{site.data.keyword.attribute-definition-list}}


# Registering a virtual server image for Power Systems
{: #vsipower-register}
{: toc-content-type="tutorial"}
{: toc-completion-time="5m"}

This tutorial walks you through how to register a public virtual server image for Power Systems in {{site.data.keyword.cloud}} Partner Center. By completing this tutorial, you learn how to provide the company details, create a test environment, and set up access for your team to help with the onboarding process.
{: shortdesc}

This tutorial demonstrates how to onboard and publish a [sample virtual server image for Power Systems Virtual Server](https://github.com/IBM-Cloud/isv-power-vsi-product-deploy-sample){: external}. It uses a fictitious company that's called *Example Corp*. As you complete the tutorial, adapt each step to fit your product's needs.

## Before you begin
{: #vsipower-reg-prereqs}

1. Verify that you're using a Pay-As-You-Go or Subscription account by going to **Manage** > **Account** > **Account settings** in the {{site.data.keyword.cloud_notm}} console.
1. Verify that you're assigned the administrator role on all account management services and all IAM-enabled services. For more information, see [Assigning access to account management services](/docs/account?topic=account-account-services) and [Managing access to resources](/docs/account?topic=account-assign-access-resources).

## Provide the company name
{: #vsipower-reg-company}
{: step}

1.  In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Overview** > **Get started**.
2. Enter the name of your company as you want it to be displayed in the catalog, and click **Save**. For the purpose of this tutorial, enter `Example Corp` as the company name.

## Create your test environment
{: #vsipower-reg-test}
{: step}

You, or a member of your team, uses the test environment to onboard the virtual server image and validate that it can be deployed to your {{site.data.keyword.powerSys_notm}}. Your test environment is a private catalog in which you import the virtual server image from an external repository.

1. Click **Create** in the Create your test environment section.
1. Enter `Example Corp Catalog` as the name of the private catalog, and click **Create**.

## Set up access for your team
{: #vsipower-reg-ag}
{: step}

You can enlist team members to help with the onboarding process by assigning them specific levels of {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) access. To streamline the process of assigning access, complete the following steps to create your access group:

1. Click **Assign** in the Assign access section.
1. Enter `Example Corp Virtual Server Image` as the name of the access group, and click **Assign**.

To review the list of permissions granted to this access group, see the [Giving team members access in Partner Center](/docs/sell?topic=sell-iam-access-pc-sell#give-access-pc) documentation section.

## Invite team members to your account
{: #vsipower-reg-invite}
{: step}

After you create the `Example Corp Virtual Server Image` access group, you're ready to invite team members to your account and add them to your access group. Team members are granted the following editor permissions by default:

* Partner Center - Sell: Complete onboarding tasks, update the visibility of products at the account level, and request approval to publish products to the {{site.data.keyword.cloud_notm}} catalog.
* Private catalog: Onboard products to private catalogs, update the visibility of products at the account and private catalog levels, and restrict the visibility of products in the {{site.data.keyword.cloud_notm}} catalog.

1. Click **Invite** in the Invite team members section.
1. Select the user type:

    * Business: A team member who can provide certain details, such as the product logo, description, and customer support experience.
    * Technical: A team member who can import the product to your test environment, configure the deployment details, and validate it's ready for use.

1. Enter the email address of each team member.
1. Click **Invite**.


## Next steps
{: #vsipower-reg-next}

You're ready to start the onboarding process. In the Onboard your product section, click **Let's go**, and [define the product details the virtual server image for Power Systems](/docs/sell?topic=sell-vsipower-define).
