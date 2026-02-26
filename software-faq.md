---

copyright:

  years: 2020, 2026

lastupdated: "2026-02-26"


keywords: third-party software, faq, product portal, partner portal, partners, sellers, help, third-party, software, partner center, frequently asked questions

subcollection: sell

content-type: faq

---

{{site.data.keyword.attribute-definition-list}}

# FAQ about selling software
{: #thirdparty-sw-faqs}

FAQ about selling third-party software on {{site.data.keyword.cloud}} might include questions about the types of software you can add to the catalog, pricing plans, and updating and restoring software versions.
{: shortdesc}

To find all FAQs for {{site.data.keyword.cloud_notm}}, see our [FAQ library](/docs/faqs).

## What's the difference between onboarding an Operator from my repository and onboarding an Operator from Red Hat?
{: #onboard-operator-GitHub-vs-RedHat}
{: faq}

One major difference is the packaging format: an Operator from a repository and an Operator bundle for an Operator from a Red Hat registry. For more information about the difference in packaging formats, see [Importing a version from your private catalog](/docs/sell?topic=sell-sw-validate#sw-validate-add).

## Can I update an operator that was onboarded from the Red Hat registry?
{: #update-operator-redhat}
{: faq}

Yes, see the FAQ item in this topic, [How do I update my software?](/docs/sell?topic=sell-thirdparty-sw-faqs#update-versions)
* To reload a software version, see [Reloading a software version](/docs/sell?topic=sell-software-reload).
* To add another version of your software, see [Adding a version of your software](/docs/sell?topic=sell-add-version-software).

## What types of software can I add to the {{site.data.keyword.cloud_notm}} catalog?
{: #supported-sw}
{: faq}

See the following list for the types of third-party software that you can currently add to the catalog:
* Helm charts on Kubernetes and {{site.data.keyword.openshiftshort}} clusters
* Terraform templates
* OVA images deployed on VMware Solutions Dedicated - vCenter Server
* Virtual server images with Terraform deployed on VPC infrastructure or {{site.data.keyword.powerSys_notm}}
* Operators with a TGZ file from GitHub or GitLab repositories
* Operator bundles from Red Hat OpenShift registries

## What account do I use to onboard my software?
{: #accountuse-sw}
{: faq}

Use your {{site.data.keyword.cloud_notm}} account to onboard software to the catalog. In some cases an {{site.data.keyword.IBM_notm}} representative, with their own account, might be helping you with the onboarding process. If you want the representative to access your software in your test environment, you can add them to your account. For more details, see [Inviting users to an account](/docs/account?topic=account-iamuserinv).

## How do I upload a version from my GitHub repository?
{: #gh-upload-sw}
{: faq}

See [Managing releases in a repository](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository){: external}.

## How do I view my account ID and type?
{: #accounttype-sw}
{: faq}

Go to **Manage** > **Account** > **Account settings** in the console. Your account ID is the alphanumeric value in the Account section. Your account type is included in the Account type section.

## Can I include a pricing plan with my software?
{: #pricing-sw}
{: faq}

Currently, software products in the {{site.data.keyword.cloud_notm}} catalog don't include pricing plans. You can bring your own licenses or deliver your third-party software for free.

## How do I update my software?
{: #update-versions}
{: faq}

To update your software, you can add a new version of it or update and republish an existing version. For more details, see [Updating your software](/docs/account?topic=account-update-private).

Make sure the version of the software that you're updating in your private catalog is the same as the version that was onboarded in the Partner Center UI.
{: note}

## A sponsored {{site.data.keyword.IBM_notm}} team is helping me onboard. Should I use their {{site.data.keyword.cloud_notm}} account or my {{site.data.keyword.cloud_notm}} account to go through the onboarding process?
{: #choose-account-sw}
{: faq}

Use your own account to onboard your software. If the {{site.data.keyword.IBM_notm}} employee uses their account, the software won’t pass the approval process and the onboarding process must be restarted. If an {{site.data.keyword.IBM_notm}} employee is helping you, you can add them to your account if you feel comfortable doing so.

## Can I restore a deprecated version of software?
{: #restore-versions}
{: faq}

Yes. To restore a deprecated version, validate and publish it again. For more details, see [Restoring a deprecated product or version](/docs/sell?topic=sell-restore-deprecated-product).

Make sure the version of the software that you're restoring in your private catalog is the same as the version that was onboarded in the Partner Center UI.
{: note}

## Can I invite a team member to help onboard software?
{: #invite-team}
{: faq}

Yes, you can add team members to help onboard software. You need to assign them specific levels of access. For more information, see [Inviting users to an account](/docs/account?topic=account-iamuserinv) and [Set up access for your team](/docs/sell?topic=sell-sw-getting-started#sw-team-access).

## Can I remove a team member's access to my account?
{: #remove-team}
{: faq}

Yes, go to **Manage > Access (IAM)** in the console, select **Users**, find the user that you want to remove, select **Remove user** from the **Actions** menu.

Only account owners and users with specific access can remove a user. For more information, see [Removing users from an account](/docs/account?topic=account-iamuserinv&interface=ui#remove-user-acount-ui).

## Can I view my assigned roles and permissions?
{: #access-onboard}
{: faq}

Yes, go to **Manage > Access (IAM)** in the console, and select your name on the **Users** page. Then, depending on the access you're looking for, select the different tabs:

* To determine what access you have through the access groups you are assigned, select **Access groups**.
* To see IAM access policies that are assigned to you, select the **Access policies**.

## Can I delete my product from the catalog?
{: #delete-product}
{: faq}

No, but you can deprecate a software version. When you deprecate a version, users cannot view the product in the catalog nor can they install it. For more information, see [Deprecating software from the {{site.data.keyword.IBM_notm}} catalog](/docs/sell?topic=sell-deprecate-product).

## How long does it take to onboard a product?
{: #time-onboard}
{: faq}

The complete onboarding process for software takes approximately 7 days.

## What do I do if my product is not approved?
{: #approval-denied}
{: faq}

If your product is not approved, you receive feedback in the console. The feedback includes why your product was not approved and what items need to be updated to receive approval. After you update the product, you can resubmit your product for approval.

## Why does Partner Center keep logging me out?
{: #session-time-out}
{: faq}

Your session timed out. Make sure to save your progress where possible to avoid lost progress.

## Why can't I see the product I'm onboarding?
{: #missing-products}
{: faq}

If you can't see the product that you are onboarding, first make sure that you are in the correct account. If you are in the correct account and your product is not listed on the **My products** page, your product was possibly deleted. Unfortunately, if your in-progress product was deleted, you must restart the onboarding process.

## How long does it take for my product to get approved?
{: #approval-time}
{: faq}

It takes approximately one to two business days for your product to be reviewed.

## Can I share my virtual server image with other users as a developer?
{: #share-vsimage}
{: faq}

Yes, you can share your virtual server image with other users. To share with users in your personal or enterprise account, see [Onboarding software to your account](/docs/account?topic=account-create-private-catalog&interface=ui). To share with {{site.data.keyword.cloud_notm}} catalog users, see [Registering a virtual server image for VPC](/docs/sell?topic=sell-vsivpc-register).

## How do I claim a certification or designation for my product?
{: #claim-certs-how}
{: faq}

If you are a third-party provider, you can learn about certifications and designations in Partner Center. Go to [Partner Center](/partner-center/sell){: external}, open your product, and click **Certifications**. Currently, SAP certification and financial services validated are represented in Partner Center.

Third-party products that complete SAP certification are added to [SAP's directory of certified and supported SAP HANA Hardware](https://www.sap.com/dmc/exp/2014-09-02-hana-hardware/enEN/#/solutions?filters=v:deCertified;iaas;ve:28){: external}.
