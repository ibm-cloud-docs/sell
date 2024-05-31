---

copyright:

  years: 2020, 2024

lastupdated: "2024-05-31"

keywords: end-to-end, software onboarding, checklist, third party, requirements, sellers, partner portal, partners, third-party software, partner center

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Checklist for selling software on {{site.data.keyword.cloud_notm}}
{: #checklist-software}

Use the following checklist to track all the tasks that are required to successfully onboard and sell your third-party software on {{site.data.keyword.cloud}}.
{: shortdesc}

## Register your product
{: #sw-start-checklist}

The following tasks are typically completed by a team member who is familiar with the business case for the product.

| Task | Description | Environment |
|------|-------------|-------------|
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Provide your company and product details | Specify the names of your company and product.  | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Create a test environment | The test environment is used to onboard your software and validate it's ready for use. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Assign team access | With the correct {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) access, members of your team can help onboard your software. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Invite team members to your account | Members of your account are assigned the IAM access that you set up in the previous task.  | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Confirm your legal agreement with {{site.data.keyword.IBM_notm}} | Review and submit the {{site.data.keyword.IBM_notm}} Digital Provider Agreement if you plan to offer bring your own license plans, review and submit the {{site.data.keyword.IBM_notm}} Digital Reseller Agreement if you plan to offer free plans, or upload your custom digital provider agreement to be reviewed and approved by {{site.data.keyword.IBM_notm}}. | {{site.data.keyword.cloud_notm}} console |
{: caption="Table 1. Getting started tasks for selling software" caption-side="top"}

For more information, see [Getting set up to sell software](/docs/sell?topic=sell-sw-getting-started).

## Tell us about your product
{: #sw-details-checklist}

The following tasks are typically completed by a team member familiar with the business case, marketing details, and customer support experience for the product.

| Task | Description | Environment |
|------|-------------|-------------|
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Review display name | Review the display name of the product that was generated for you and make any updates to it if needed. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Create and submit programmatic name | Create a programmatic name for your product and submit it for review. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Verify your partner details | Review the Company and Team information and make sure that everything is correct.	| {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Define your product details | Add details, such as your product logo, keywords, description, features, and documentation URL, for your product's entry and details page in the {{site.data.keyword.cloud_notm}} catalog. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Define your support details | Provide your support site URL, contacts, escalation process, and the locations where your support teams are based. | {{site.data.keyword.cloud_notm}} console |
{: caption="Table 2. Tasks for defining software details" caption-side="top"}

For more information, see the following links:

* [Defining your catalog entry and product page](/docs/sell?topic=sell-sw-catalog-details)
* [Defining your support experience](/docs/sell?topic=sell-sw-support-details)

## Define your pricing plan 
{: #software-pricing-define}

| Task | Description | Environment |
|------|-------------|-------------|
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Submit the Electronic Transfer Funds and tax form | To receive payment disbursements for usage-based pricing plans, email the required documents. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Add your ECCN | Add the Export Control Classification Number (ECCN) that applies to your product. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Add your UNSPSC | Add the United Nations Standard Products and Services Code (UNSPSC) that applies to your product. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Define your pricing information | Add pricing plans to your product: free, usage-based, and bring your own license (BYOL). If you choose BYOL, provide details about your license.  | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Add metrics to your pricing plan | Add metrics to your usage-based pricing plan to determine how customers are charged. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Test and submit resource usage | Review how customers understand and experience your pricing plan, and validate that your metered plans are correctly configured by enabling and submitting a usage test. This usage test includes creating your metering JSON, calling the Usage Metering API and submitting metering evidence. For more information, see [Usage Metering API](/apidocs/usage-metering#report-resource-usage){: external}. | Development environment and documentation, {{site.data.keyword.cloud_notm}} console  |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Review and submit the {{site.data.keyword.cloud_notm}}'s Digital Platform Reseller Agreement | Review and submit the {{site.data.keyword.IBM_notm}} Digital Platform Reseller Agreement if you plan to offer free or paid plans, or upload your custom digital provider agreement to be reviewed and approved by {{site.data.keyword.IBM_notm}}. | {{site.data.keyword.cloud_notm}} console |
{: caption="Table 3. Tasks for adding pricing plans for software" caption-side="top"}

Usage-based pricing plans are available only for software that are onboarded with the virtual server image delivery method.
{: note}

For more information, see the following links:

* [Defining your pricing model for software](/docs/sell?topic=sell-sw-pricing)
* [Adding metrics to your software](/docs/sell?topic=sell-software-add-metrics)

## Onboard your product
{: #sw-validate-checklist}

The following tasks are typically completed by a technical member of your team.

| Task | Description | Environment |
|------|-------------|-------------|
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Set up your source code repository | Create a release in your source code repository to deliver and manage versions of your software. | Your GitHub or GitLab repository |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Upload a readme file | Provide a readme file that describes how users can install your software and get customer support. | Your GitHub or GitLab repository |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Onboard your software| Import a version, configure the deployment details, set any license requirements, and validate that the version can be successfully installed on the infrastructure that you require. | {{site.data.keyword.cloud_notm}} console |
{: caption="Table 4. Tasks for onboarding software" caption-side="top"}

For more information, see the following links:

* [Setting up your source code repository](/docs/sell?topic=sell-source-repo-setup)
* [Onboarding your software](/docs/sell?topic=sell-sw-validate)

## Publish your product
{: #sw-publish-checklist}

The following tasks are completed by any member of your team.

| Task | Description | Environment |
|------|-------------|-------------|
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Verify that all tasks are completed | Confirm that you completed the getting started tasks, defined your software details, and onboarded your software. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Request to publish your software | Submit a request for {{site.data.keyword.cloud_notm}} to review your product details and approve it's ready for publishing. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Publish your software | After your publishing request is approved, publish your software to the {{site.data.keyword.cloud_notm}} catalog. | {{site.data.keyword.cloud_notm}} console |
{: caption="Table 5. Tasks for publishing software" caption-side="top"}

For more information, see [Publishing your software to the {{site.data.keyword.cloud_notm}} catalog](/docs/sell?topic=sell-sw-publish).

As a third-party provider, you're responsible for maintaining all assets of published software in the {{site.data.keyword.cloud_notm}} catalog and deprecating outdated versions.
{: note}
