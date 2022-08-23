---

copyright:
  years: 2021

lastupdated: "2021-12-02"


keywords: onboard software, third-party software, sell on IBM Cloud, partner center, operator, validate, test, Red Hat OpenShift cluster, bundle, Kubernetes cluster, product details, catalog listing, support, pricing, BYOL

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 15m 

---

{{site.data.keyword.attribute-definition-list}}


# Registering your Operator bundle 
{: #bundle-register}
{: toc-content-type="tutorial"} 
{: toc-completion-time="15m"} 

This tutorial walks you through how to register an Operator bundle in {{site.data.keyword.cloud}} Partner Center as part of the process of onboarding to the {{site.data.keyword.cloud_notm}} catalog. By completing this tutorial, you learn how to provide your company and product information, create a test environment, and set up team access.
{: shortdesc}

This tutorial is one of four in a series that demonstrates how to onboard and publish a sample Certified Operator bundle from the {{site.data.keyword.openshiftshort}} registry. It uses a fictitious company that's called *Example Corp*. As you complete the tutorial, adapt each step to fit your product's needs.

## Before you begin
{: #bundle-reg-prereqs}

1. Go to {{site.data.keyword.redhat_notm}} OperatorHub to confirm that your Operator bundle exists in the {{site.data.keyword.redhat_notm}} registry.
1. Verify that you're using a Pay-As-You-Go or Subscription account by going to **Manage** > **Account** > **Account settings** in the {{site.data.keyword.cloud_notm}} console. 
1. Verify that you're assigned the correct roles. For more information, see [Assigning access to account management services](/docs/account?topic=account-account-services) and [Managing access to resources](/docs/account?topic=account-assign-access-resources).
   * Administrator on all account management services and all Identity and Access Management (IAM) services
   * Editor on the Catalog Management service
   * Editor on the {{site.data.keyword.registrylong_notm}} service
   * Administrator on the {{site.data.keyword.openshiftshort}} cluster
   * Editor on the software instance service

Make sure that you use the same account to access the {{site.data.keyword.registrylong_notm}} and to create the {{site.data.keyword.openshiftshort}} cluster.
{: important}


## Provide your company name
{: #bundle-reg-company}
{: step}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **Get started**.
1. Enter the name of your company as you want it to be displayed in the catalog, and click **Save**. For this tutorial, enter `Example Corp` as the company name. 

## Create your test environment
{: #bundle-reg-test}
{: step}

You, or a member of your team, uses the test environment to onboard the Operator bundle and validate that it can be deployed to a {{site.data.keyword.openshiftshort}} cluster. Your test environment includes a private catalog in which you import the Operator bundle from the {{site.data.keyword.redhat_notm}} Certified registry. 

1. Click **Create** in the Create your test environment section. 
1. Enter `Example Corp Catalog` as the name of the private catalog, and click **Create**.

## Set up access for your team 
{: #bundle-reg-access}
{: step}

You can enlist team members to help with the onboarding process by assigning them specific levels of {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) access. Create an access group to streamline the process of assigning access.

1. Click **Assign** in the Assign access section.
1. Enter `Example Corp Bundle` as the name of the access group, and click **Create**. The following roles are assigned to the access group by default:
  
    * Administrator on the Catalog Management service
    * Editor on the Partner Center - Sell service
    * Editor on the User Management service
    * Editor on the IAM Access Groups service
    * Viewer on all account management services
  
For more information about the actions associated with each role, see [Actions and roles for account management services](/docs/sell?topic=account-account-services#account-management-actions-roles).

## Add team members to your account
{: #bundle-reg-invite}
{: step}

After you create the `Example Corp Bundle` access group, you're ready to add team members to your account and access group. Team members are granted the following editor permissions by default: 

* Partner Center - Sell: Complete onboarding tasks, update the visibility of products at the account level, and request approval to publish products to the {{site.data.keyword.cloud_notm}} catalog.
* Private catalog: Onboard products to private catalogs, update the visibility of products at the account and private catalog levels, and restrict the visibility of products in the {{site.data.keyword.cloud_notm}} catalog.


1. Click **Invite** in the Invite team members section. 
1. Select the user type:

    * Business: A team member who can provide certain details, such as the product logo, description, and customer support experience.
    * Technical: A team member who can import the product to your test environment, configure the deployment details, and validate it's ready for use.

1. Enter the email address of each team member.
1. Click **Invite**.

## Next steps
{: #bundle-reg-next}

You're ready to start the onboarding process. In the Onboard your product section, click **Let's go**, and [define the product details for the Operator bundle](/docs/sell?topic=sell-bundle-define).

