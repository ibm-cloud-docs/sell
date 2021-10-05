---

copyright:

  years: 2020, 2021

lastupdated: "2021-10-05"


keywords: third-party software, faq, product portal, partner portal, partners, sellers, help, third-party, software, partner center, frequently asked questions

subcollection: sell

content-type: faq

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:external: target="_blank" .external}
{:faq: data-hd-content-type="faq"}
{:support: data-reuse='support'}
{:note: .note}
{:beta: .beta}

# FAQs about selling software
{: #thirdparty-sw-faqs}

FAQs about selling third-party software on {{site.data.keyword.cloud}} might include questions about the types of software you can add to the catalog, pricing plans, and updating and restoring software versions. 
{: shortdesc}

To find all FAQs for {{site.data.keyword.cloud_notm}}, see our [FAQ library](/docs/faqs).

The process to sell third-party software is still under development. With the current release, you can bring your own licenses or deliver your third-party software for free. If you have questions, contact us at cloud.onboarding@us.ibm.com.
{: beta}

## What types of software can I add to the {{site.data.keyword.cloud_notm}} catalog? 
{: #supported-sw}
{: faq}

See the following list for the types of third-party software that you can currently add to the catalog:

* Helm charts on Kubernetes and {{site.data.keyword.redhat_notm}} {{site.data.keyword.openshiftshort}} clusters
* Terraform templates
* OVA images deployed on VMware vCenter Server
* Virtual server images with Terraform deployed on VPC infrastructure
* Operators with a CSV file or Operator bundles with a TGZ file from GitHub repositories deployed on Red Hat OpenShift
* Operator bundles from Red Hat OpenShift registries

## What account do I use to onboard my software? 
{: #accountuse-sw}
{: faq}

Use your {{site.data.keyword.cloud_notm}} account to onboard software to the catalog. In some cases an {{site.data.keyword.IBM_notm}} representative, with their own account, might be helping you with the onboarding process. If you want the representative to access your software in your test environment, you can add them to your account. For more details, see [Inviting users to an account](/docs/account?topic=account-iamuserinv).

## What's the difference between onboarding an Operator from my GitHub repository and onboarding an Operator from Red Hat? 
{: #onboard-operator-GitHub-vs-RedHat}
{: faq}

One major difference is the packaging format: a *ClusterServiceVersion* (CSV) file for an Operator from a GitHub repository and an Operator bundle from a Red Hat registry. For example formats of each option, see [Importing a version from your private catalog](/docs/sell?topic=sell-sw-validate#sw-validate-add).

## Can I update an Operator that was onboarded from the Red Hat registry?
{: #update-operator-redhat}
{: faq}

Yes, see the following links for more information:

* [Adding a new version of software](/docs/sell?topic=sell-add-version-software).
* [Reloading a software version](/docs/sell?topic=sell-software-reload).

## How do I upload a version from my GitHub repository?
{: #gh-upload-sw}
{: faq}

See [Managing releases in a repository](https://docs.github.com/en/github/administering-a-repository/managing-releases-in-a-repository){: external}.

## How do I view my account ID and type? 
{: #accounttype-sw}
{: faq}

Go to **Manage** > **Account** > **Account settings** in the console. Your account ID is the alphanumeric value in the Account section. Your account type is included in the Account type section. 

## Can I include a pricing plan with my software?
{: #pricing-sw}
{: faq}

Currently, software products in the {{site.data.keyword.cloud_notm}} catalog don't include pricing plans. You can bring your own licenses or deliver your third-party software for free. 

## What account do I use to onboard my product?
{: #choose-account-sw}
{: faq}

Use your own account to onboard your software. If an {{site.data.keyword.IBM_notm}} representative is helping you with the onboarding process, you can add them to your account if you feel comfortable doing so. See [Inviting team members](/docs/sell?topic=sell-sw-invite-team) for more information. 

## Can I remove a team member's access to my account?
{: #remove-team}
{: faq}

If you're the account owner, or if you have the required access, you can remove users. For more information, see [Removing users from an account](/docs/account?topic=account-remove).

## Can I view my assigned roles and permissions?
{: #access-onboard}
{: faq}

Yes, go to **Manage > Access (IAM)** in the console, and select your name on the **Users** page. Then, depending on the access you're looking for, select the different tabs:

* To determine what access you have through the access groups you are assigned, select **Access groups**.
* To see IAM access policies that are assigned to you, select the **Access policies**.

## How long does it take to onboard a product? 
{: #time-onboard}
{: faq}

The complete onboarding process for software takes approximately 7 days. 

## What if my product isn't approved for publishing in the catalog?
{: #approval-denied}
{: faq}

If your product is not approved, we'll send you an email with details about what items require updates. After you address the feedback, you can submit another publishing request.

## Why does Partner Center keep logging me out? 
{: #session-time-out}
{: faq}

Your session timed out. Make sure to frequently save your updates to maintain your current progress.

## Why can't I find the product that I'm onboarding? 
{: #missing-products}
{: faq}

* If you can't find your product, make sure that you are in the correct account. 
* If you are in the correct account and your product is not listed on the **My Products**, your product might have been deleted. You will need to start the onboarding process again.

## How soon is my product approved for publishing? 
{: #approval-time}
{: faq}

You can expect your product to be reviewed and approved for publishing in 1 to 2 business days.

