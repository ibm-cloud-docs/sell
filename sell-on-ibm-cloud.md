---


copyright:
  years: 2021, 2025
lastupdated: "2025-07-01"

keywords: onboard software, onboard service, onboard deployable architecture, third-party software, sell on IBM Cloud, third-party service, Partner Center, product onboarding, deploy, Onboarding Workbench

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Selling on {{site.data.keyword.cloud_notm}}
{: #selling-clouds}

Are you looking to sell your software, services, or deployable architectures on {{site.data.keyword.cloud}}? You can use our broad portfolio of managed infrastructure services and developer tools to build your applications on the public cloud and manage authentication, access, self-service creation, metering, and billing. Join our strategic growing network of 70 ISV partners with over 600,000 active monthly users.
{: shortdesc}

## Before you begin
{: #selling-product-requirements}

If you plan to offer products on the {{site.data.keyword.cloud_notm}} platform, you must complete the following requirements:

* Verify that you're using a Pay-As-You-Go or Subscription account. To check your account type, go to **Manage** > **Account** > **Account settings** in the {{site.data.keyword.cloud_notm}} console.

   It's recommended that you use an account that was created with a [functional ID](/docs/account?topic=account-identity-overview#functionalid-bestpract) to ensure your continued access to the products that are onboarded in the account.
   {: tip}

* Verify that you're assigned the administrator role on all account management services and all IAM-enabled services. See [Assigning access to account management services](/docs/account?topic=account-account-services) and [Managing access to resources](/docs/account?topic=account-assign-access-resources).

* To sell services, verify that your company is an approved {{site.data.keyword.cloud_notm}} build partner with an [Embedded Solutions Agreement (ESA)](https://ibm.seismic.com/app?ContentId=efd7827b-910e-4e91-a5f6-6020730e88c3){: external}. For more information about being an {{site.data.keyword.Bluemix_notm}} build partner, see the [IBM Partner Plus](https://www.ibm.com/partnerplus){: external} page.

* Verify that your product is ready to be publicly listed and sold through the {{site.data.keyword.cloud_notm}} catalog.

* Verify that your product does not include Consulting and Professional Services.

* Be prepared to create and maintain the products that you list in the {{site.data.keyword.cloud_notm}} catalog, which includes being responsive to addressing updates and providing timely support to your customers.

### Requirements for offering services
{: #service-requirements}

Verify that you're hosting your service primarily on {{site.data.keyword.cloud_notm}} or following one of the use cases:

* You must use {{site.data.keyword.IBM_notm}} software, {{site.data.keyword.cloud_notm}} services wherever applicable and host all applications and databases components (for example storage, backup, replication or data recovery, monitoring, logging, vulnerability management, and patching tools) on {{site.data.keyword.cloud_notm}}.

* You must host all of your product's application and database components on {{site.data.keyword.cloud_notm}}, including supporting components like backup, replication, or data recovery. Other services like monitoring, logging, vulnerability management and patching tools can run on-premises or on another cloud, but must send data to the {{site.data.keyword.cloud_notm}} environment for storage and further analysis.

* The migration tooling of your product has {{site.data.keyword.cloud_notm}} as its only destination for migration, but can run on-premises or on another cloud as a migration source.

### Requirements for offering software
{: #software-requirements}

Verify that the following software deployment scripts and package dependencies apply to your product:

* Custom QCOW2 or VHD images with Terraform deployed on VPC infrastructure

* OVA images deployed on VMware Solutions Dedicated - vCenter Server

* OVA images (consisting of OVF and disk image) for {{site.data.keyword.powerSys_notm}}

* Helm charts on Kubernetes and {{site.data.keyword.openshiftshort}} clusters

* Operators or Operator bundles with a TGZ file from GitHub or GitLab repositories

* Operator bundles from {{site.data.keyword.redhat_openshift_notm}} registries

## What kind of product do you want to sell?
{: #selling-software-services}

By using Partner Center Sell to onboard your product, you can create a tile to offer your product in the {{site.data.keyword.cloud_notm}} catalog. You might have a software application that users can manage and install, a software-based service, or a software-based solution (deployable architecture) that combines a set of products that you can offer for customers to solve a business problem or need.

Take advantage of a simplified installation and deployment process for your customers through the {{site.data.keyword.cloud_notm}} catalog. Review the following sections to understand how your product can be offered through {{site.data.keyword.cloud_notm}}.

### Software
{: #selling-sotware}

Software includes containerized applications or system images that your customers can run on their own infrastructure.

Types of third-party software that {{site.data.keyword.cloud_notm}} supports include:

- Operators for adding services
- Cloud Pak for installing services
- Images through Terraform templates (such as virtual server image or OVA)
- Images for Power Systems (virtual server image)
- Terraform templates for configuration
- Helm charts for working with applications
- Virtual server image for VPC

Your software can be deployed onto specified targets, including {{site.data.keyword.containerlong}}, {{site.data.keyword.openshiftlong}}, {{site.data.keyword.powerSys_notm}}, {{site.data.keyword.bpshort}}, Virtual Private Cloud, and vCenter Server.

The process is as simple as selecting the Deployable Software option, providing company information, creating a suitable test environment, setting up team access, and inviting team members to join. For more information, see [Getting set up to sell software](/docs/sell?topic=sell-sw-getting-started) and [Onboarding your software](/docs/sell?topic=sell-sw-validate).

### Services
{: #selling-service}

Managed services help run the infrastructure in your own account and to deploy instances by using the {{site.data.keyword.Bluemix_notm}}. If you have a service that you want to provide, you can offer it as an integrated billing service. Offering it as an integrated billing service means that users can create an instance of your service automatically. You can onboard your service to {{site.data.keyword.cloud_notm}} by defining your service, building pricing plans, and creating brokers.

When you onboard your service, you must select the type of service that you are onboarding. Your service type is used for tax assessment purposes. {{site.data.keyword.cloud_notm}} supports three types of services:

Software as a service
:   A model of software deployment in which the software that includes business processes, enterprise applications, and collaboration tools, are provided as a service to customers through the cloud.

Infrastructure as a service
:   The delivery of a compute infrastructure, including server functionality, networking functionality, data center functionality, and storage functionality as an outsourced service.

Platform as a service
:   The delivery of a computing platform, including applications, optimized middleware, development tools, and Java and Web 2.0 runtime environments, in a cloud-based environment.

Categories of third-party services that fit within the service types include:
- Container services that help build containerized applications
- Storage services for persistent cloud storage and data encryption
- AI and machine learning services (by integrating with IBM Watson)
- Analytics services for analyzing data to deploy in cognitive applications
- Blockchain services for data exchange
- Database services for high availability, enhanced security, and scalable performance
- Developer and migration tool services
- Logging and monitoring services for detecting and troubleshooting issues
- Integration services for faster integration
- Internet of Things services for working with application data
- Security services for enterprise-grade cloud security
- Mobile services for building and starting mobile applications

The process includes registering your service with {{site.data.keyword.cloud_notm}}, defining your product and its pricing plans, and linking a broker. For more information, see [Getting set up to sell services](/docs/sell?topic=sell-get-started).

### Deployable architectures
{: #selling-da}

A deployable architecture is cloud automation for deploying a common architectural pattern that combines one or more cloud resources that are designed for easy deployment, scalability, and modularity that solves a customer-defined problem. A deployable architecture can have one or more architecture variations and multiple configurations for those architectures, based on the customer business needs. Deployable architectures can be onboarded to the {{site.data.keyword.cloud_notm}} catalog and are displayed as tiles in the catalog after you go through the publishing process and get approval in Partner Center.

Categories of third-party deployable architectures that you can select in Partner Center:
* Converged infrastructure
* Enterprise applications

Deployable architectures are different from software in that they require an architecture diagram, and offer the ability to list dependencies. A deployable architecture can have up to three architecture variations. This means that a single deployable architecture tile in the {{site.data.keyword.cloud_notm}} catalog can have different options for a user to try out that might be considered small, medium, or large variations. Or, the different architectures might be based on capability or complexity for running a proof of concept or production workload that uses names like quick start, standard, or advanced.

The only deployable architecture type that {{site.data.keyword.cloud_notm}} supports is Terraform.

For more information, see [What is a deployable architecture?](/docs/secure-enterprise?topic=secure-enterprise-understand-module-da#what-is-da) and [Getting set up to sell deployable architectures](/docs/sell?topic=sell-da-getting-started&interface=ui).
