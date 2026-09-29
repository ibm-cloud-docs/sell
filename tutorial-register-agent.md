---

copyright:
  years: 2026, 2026

lastupdated: "2026-09-29"

keywords: onboard agent, third-party agent, sell on IBM Cloud, partner center, register, WXO agent, watsonx

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 5m

---

{{site.data.keyword.attribute-definition-list}}


# Registering an agent in Partner Center
{: #agent-register}
{: toc-content-type="tutorial"}
{: toc-completion-time="5m"}

This tutorial walks you through how to register an agent in {{site.data.keyword.cloud}} Partner Center. By completing this tutorial, you learn how to provide your company details and set up access for your team to help with the onboarding process.
{: shortdesc}

Agents are AI-powered services that you can list in the {{site.data.keyword.wxorchestrate_short}} and {{site.data.keyword.cloud_notm}} catalogs. You can choose between two types:

* **External agents**: Run on your own infrastructure and connect to {{site.data.keyword.wxorchestrate_short}} through an API.
* **Native agents**: Built and deployed directly within {{site.data.keyword.wxorchestrate_short}} by using {{site.data.keyword.IBM_notm}}-managed models and tools.

When you onboard an agent, your solution becomes available to {{site.data.keyword.IBM_notm}} enterprise customers who use {{site.data.keyword.wxorchestrate_short}}. As an independent software vendor (ISV), you can reach those customers directly, as they can discover, purchase, and deploy your agent alongside {{site.data.keyword.IBM_notm}} AI capabilities. Agents in the catalog support enterprise use cases including HR, IT automation, customer service, and collaboration. For more information about the program and onboarding requirements, see [{{site.data.keyword.IBM_notm}} Agent Connect documentation](https://connect.watson-orchestrate.ibm.com/introduction){: external}.

{{_include-segments/notes.md}}

## Before you begin
{: #agent-reg-prereqs}

Before you register your agent, make sure that you complete the following prerequisites.

1. Verify that you're using a Pay-As-You-Go or Subscription account by going to **Manage** > **Account** > **Account settings** in the {{site.data.keyword.cloud_notm}} console.
1. Verify that you're assigned the administrator role on all account management services and all IAM-enabled services. For more information, see [Assigning access to account management services](/docs/iam?topic=iam-account-services&interface=ui) and [Managing access to resources](/docs/iam?topic=iam-assign-access-resources&interface=ui).

## Provide your company name
{: #agent-reg-company}
{: step}

The first time you access Partner Center, you are required to provide your company name. This name is displayed in the catalog and identifies your organization to customers.

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation menu** icon ![Navigation menu icon](../icons/icon_hamburger.svg "Navigation menu") > **Partner Center** > **Overview** > **Get started**.
1. Enter the legal name of your company as you want it to be displayed in the catalog, and click **Save**. For the purpose of this tutorial, enter `Example Corp` as the company name.

## Set up access for your team
{: #agent-reg-access}
{: step}

You can enlist team members to help with the onboarding process by assigning them specific levels of {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) access. Create an access group to streamline the process of assigning access.

1. Click **Assign** in the Assign access section.
1. Enter `Example Corp Agent` as the name of the access group, and click **Assign**.

To review the list of permissions granted to this access group, see [Giving team members access in Partner Center](/docs/sell?topic=sell-iam-access-pc-sell#give-access-pc).

## Next steps
{: #agent-reg-next}

You're ready to start the onboarding process. In the Onboard your product section, click **Let's go**, and [define the product details for your agent](/docs/sell?topic=sell-agent-define).
