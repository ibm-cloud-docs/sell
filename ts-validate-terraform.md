---

copyright:
  years: 2021, 2022
lastupdated: "2022-12-19"

keywords: troubleshooting, Terraform, validate, version, unknown token

subcollection: sell

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I validate my Terraform template?
{: #ts-validate-terraform}
{: #troubleshoot}

When you try to add a Terraform template to your private catalog, the validation process fails because the correct version of the Terraform template isn't specified.
{: shortdesc}

The following error is displayed when you try to validate that the Terraform template can be installed on the target infrastructure:
{: tsSymptoms}

> Error: Error parsing /file-path/main.tf: At 9:14: Unknown token : 9:14 IDENT var.resource_group

The Terraform version that you specify during the validation process is incorrect. You might be specifying a version of Terraform that's used when you run stand-alone {{site.data.keyword.bplong_notm}}.
{: tsCauses}

To specify the Terraform version to use during the validation process, complete the following steps:
{: tsResolve}

1. Add a variable to your Terraform template as shown in the following example:

    ```terraform
    variable "TF_VERSION" {
    description = "terraform version."
    default = 0.13
    }
    ```
    {: codeblock}

2. After you import your Terraform template to your private catalog, add the template version as a deployment value that's hidden from users when they install the software.
