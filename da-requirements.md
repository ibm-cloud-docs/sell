---


copyright:
  years: 2023, 2024
lastupdated: "2024-04-11"

keywords: deployable architecture, third party, product center sell, requirements, onboarding requirements, deployable architecture prereqs

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Preparing to onboard deployable architectures
{: #da-requirements}

Before you can start onboarding a deployable architecture to the {{site.data.keyword.cloud}} catalog in Partner Center, you must complete the following requirements: creating and designing the deployable architecture, creating the required documentation for it and validating the deployable architecture through testing.
{: shortdesc}

## Before you begin
{: #before-onboard-da}

- Review the information in [What is a deployable architecture?](/docs/secure-enterprise?topic=secure-enterprise-understand-module-da#what-is-da) to learn more about deployable architectures.

## Creating the deployable architecture
{: #create-the-da}

Create the deployable architecture based on modules that meet the [module authoring guidelines](https://terraform-ibm-modules.github.io/documentation/#/implementation-guidelines.md){: external}. Complete the following steps to create the deployable architecture:

1. Use the existing curated modules from the [{{site.data.keyword.cloud_notm}} Terraform modules GitHub organization](https://github.com/terraform-ibm-modules){: external}, but make sure that you use only the modules that have the `supported` badge.

1. If you can't find a suitable module, but there is an existing {{site.data.keyword.IBM_notm}} module in the [terraform-ibm-modules (TIM) organization](https://github.com/terraform-ibm-modules){: external} that is provisioning or configuring a specific service and similar to what you need, but is missing some capabilities, consider extending its functions by contributing to it with opening pull requests.
    1. Or, you can build a new module by following the steps in [Contributing to the {{site.data.keyword.cloud_notm}} Terraform modules project](https://terraform-ibm-modules.github.io/documentation/#/contribute-module?id=contributing-to-the-ibm-cloud-terraform-modules-project){: external}.

Make sure to maintain the Terraform modules that you develop and support in your own GitHub organization or repository, but use {{site.data.keyword.IBM_notm}}'s tools, modules, and module template structure. For more information, see the [module authoring guidelines](https://terraform-ibm-modules.github.io/documentation/#/implementation-guidelines.md){: external}.
{: note}

## Designing the deployable architecture
{: #design-da}

The deployable architecture must be designed in a way that it can be deployed in various manners. Design the deployable architecture to meet the following criteria:

* The deployable architecture must be available as a Terraform definition, which means that the deployable architecture must be fully executable through the Terraform command-line interface (CLI). This definition must meet the [module authoring guidelines](https://terraform-ibm-modules.github.io/documentation/#/implementation-guidelines.md){: external}.
* The deployable architecture must be fully executable from {{site.data.keyword.bplong_notm}}, or through using the CLI of the automation technology, for example, Terraform or Ansible. Make sure that you test the deployable architecture through {{site.data.keyword.bpshort}}.

## Creating the required documentation for the deployable architecture
{: #create-required-documentation}

Deployable architectures that are onboarded to the {{site.data.keyword.cloud_notm}} catalog must have the following documentation: a readme file, a reference architecture, and an architecture diagram.

Create the following documentation for the deployable architecture:

Readme file
:   Every repository in the [{{site.data.keyword.cloud_notm}} Terraform modules GitHub organization](https://github.com/terraform-ibm-modules){: external} is created from the module template repository, and has the readme file with embedded information about how to create. For more information on the details that must be included in your readme file, see [Contributing modules](https://terraform-ibm-modules.github.io/documentation/#/contribute-module){: external}.

Reference architecture
:   A reference architecture is a documented opinionated pattern that solves a variation of a customer-defined business problem. The reference architecture includes a summary, an architecture diagram, design decisions and consideration, and a list of components or pre-defined modules that make up the pattern.

:   The reference architecture must be authored in Markdown and saved in the `/reference-architectures` directory in the module repository. All reference architectures that are stored in this location are published in the {{site.data.keyword.cloud_notm}} Docs. Each reference architecture can be found in the [Solution library](/docs?tab=solutions).

Architecture diagram
:   You must create an architecture diagram in `.svg` format. This diagram is included in the reference architecture and also used in the {{site.data.keyword.cloud_notm}} catalog. It must be saved in the `/reference-architectures` directory in the module repository.

:   The [Draw.io app](https://www.drawio.com){: external} is favored by architects for creating architecture diagrams. It comes with standard icons and templates from the [{{site.data.keyword.IBM_notm}} stencils](https://github.com/ibm-cloud-architecture/ibm-cloud-stencils){: external} that you can use as you create your architecture diagram.

## Testing and validating the deployable architecture
{: #test-validate-da}

Test and validate the deployable architecture in your account by completing the following steps:

For the testing purposes, make sure that you use an {{site.data.keyword.cloud_notm}} account in which you have permissions to create new resources.
{: note}

* Implement [validation tests](https://terraform-ibm-modules.github.io/documentation/#/tests.md){: external}.
* Follow the [HashiCorp Terraform module guidelines](https://developer.hashicorp.com/terraform/language/tests#modules){: external}.
* Test whether the deployable architecture is able to run in {{site.data.keyword.bplong_notm}}.
* Make sure that modules that are pushed to the [{{site.data.keyword.cloud_notm}} Terraform modules GitHub organization](https://github.com/terraform-ibm-modules){: external}with findings from the validation pipeline are analyzed and resolved.
* Test the reference architecture by using the common validation pipeline.

## Next steps
{: #onboard-da-next}
   
You're now ready to onboard your deployable architecture in Partner Center. For more information, see [Getting set up to sell deployable architectures](/docs/sell?topic=sell-da-getting-started).

