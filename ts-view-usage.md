---

copyright:
  years: 2021
lastupdated: "2021-10-14"

keywords: troubleshooting, usage, offers, rewards, partner center, viewer, billing service, IAM, offers, account management

subcollection: sell

content-type: troubleshoot

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:beta: .beta}
{:note:.deprecated}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Why can't I view any usage or rewards details in Partner Center?
{: #ts-view-usage}
{: #troubleshoot}

When you're working in an {{site.data.keyword.cloud}} account that you've been added to, you can't view or access details about usage or rewards in Partner Center. Specifically, the chart on the Usage and offers page doesn't display any data. And, the following error message is displayed in the Your rewards section.
{: tsSymptoms}

`Oops! Your incentives details are currently unavailable.`

By default, only account owners can view usage and rewards details. For users of an account to view this information, specific IAM access is required: [viewer role on the Billing service](/docs/sell?topic=account-account-services#pc-buildgrow-account-management). 
{: tsCauses}  

Contact your account owner and request viewer access to usage and rewards details. 
{: tsResolve}
