---

copyright:
  years: 2021
lastupdated: "2021-07-01"

keywords: troubleshooting, Terraform, validate, version, unknown token

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

# Why can't I validate my Terraform template?
{: #ts-validate-terraform}
{: #troubleshoot}

When you try to onboard a Terraform template to the {{site.data.keyword.cloud}} catalog, the validation process fails because the correct version of the Terraform template isn't specified. 
{: shortdesc}

The process to sell third-party software is still under development. With the current release, you can bring your own licenses or deliver your third-party software for free. If you have questions, contact us at cloud.onboarding@ibm.com.
{: beta}

The following error is displayed when you try to validate that the Terraform template can be installed on the target infrastructure:
{: tsSymptoms}

`Error: Error parsing /file-path/main.tf: At 9:14: Unknown token : 9:14 IDENT var.resource_group`

The Terraform version that you specify during the validation process is incorrect. You might be specifying a version of Terraform that's used when you run stand-alone {{site.data.keyword.bplong_notm}}. 
{: tsCauses}  

To specify the Terraform version to use during the validation process, complete the following steps:
{: tsResolve}

1. Add a variable to your Terraform template as shown in the following example:

    ```
    variable "TF_VERSION" {
    description = "terraform version."
    default = 0.13
    }
    ```
    {: codeblock}

2. After you import your Terraform template to your private catalog, add the template version as a deployment value that's hidden from users when they install the software. 
