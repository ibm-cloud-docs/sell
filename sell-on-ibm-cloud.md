---


copyright:
  years: 2021, 2023
lastupdated: "2023-03-15"

keywords: onboard software, onboard service, third-party software, sell on IBM Cloud, third-party service, Partner Center, resource management console, RMC, product onboarding, deploy, Onboarding Workbench

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Selling on {{site.data.keyword.cloud_notm}}
{: #selling-clouds}

Are you looking to sell your software or services on {{site.data.keyword.cloud}}? You can use our broad portfolio of managed infrastructure services and developer tools to build your applications on the public cloud and manage authentication, access, self-service creation, metering, and billing. Join our strategic growing network of 70 ISV partners with over 600,000 active monthly users.
{: shortdesc}

## Before you begin
{: #selling-product-requirements}

If you plan to offer products on the {{site.data.keyword.cloud_notm}} platform, you must complete the following requirements:

* Verify that you're using a Pay-As-You-Go or Subscription account. To check your account type, go to **Manage** > **Account** > **Account settings** in the {{site.data.keyword.cloud_notm}} console.

   It's recommended that you use an account that was created with a [functional ID](/docs/account?topic=account-identity-overview#functionalid-bestpract) to ensure your continued access to the products that are onboarded in the account.
   {: tip}

* Verify that you're assigned the administrator role on all account management services and all IAM-enabled services. See [Assigning access to account management services](/docs/account?topic=account-account-services) and [Managing access to resources](/docs/account?topic=account-assign-access-resources).

* To sell services, verify that your company is an approved {{site.data.keyword.cloud_notm}} build partner with a [Direct Embedded Solutions Agreement](https://www-2000.ibm.com/partnerworld/pdfs/IBM_ESA_Technology_Partner_Direct_Application_Guide.pdf){: external}. For more information about being an {{site.data.keyword.Bluemix_notm}} build partner, see the [IBM Build Partner](https://www.ibm.com/partnerworld/public/build){: external} page.

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

## Software or services?
{: #software-or-services}

Do you want to sell your third-party service on {{site.data.keyword.Bluemix_notm}}? Or do you want to onboard your software to our {{site.data.keyword.Bluemix_notm}} platform? You might have a software application that users can manage and install, or a software-based service you can manage for users.

You can use our expanding catalog of software solutions to take advantage of a simplified installation process. You can also bring your own licenses, or offer your third-party software for free. For more information, see [Software](https://cloud.ibm.com/catalog#software).

If you have a service that you want to provide, you can offer it as an integrated billing service. Offering it as an integrated billing service means that users can create an instance of your service automatically. You can onboard your service to {{site.data.keyword.Bluemix_notm}} by defining your service, building pricing plans, and creating brokers. For more information, see [Services](https://cloud.ibm.com/catalog#services).

### Software
{: #software}

Software includes containerized applications or system images that your customers can run on their own infrastructure.

Types of third-party software that {{site.data.keyword.cloud_notm}} supports include:

- Operators for adding services
- Cloud Pak for installing services
- Images through Terraform templates (such as virtual server image or OVA)
- Images for Power Systems (virtual server image)
- Terraform templates for configuration
- Helm charts for working with applications

Your software can be deployed onto specified targets, including {{site.data.keyword.containerlong}}, {{site.data.keyword.openshiftlong}}, {{site.data.keyword.powerSys_notm}}, {{site.data.keyword.bpshort}}, Virtual Private Cloud and vCenter Server.

The process is as simple as selecting the Deployable Software option, providing company information, creating a suitable test environment, setting up team access, and inviting team members to join. For more information, see [Getting set up to sell software](/docs/sell?topic=sell-get-started) and [Onboarding your software](/docs/sell?topic=sell-sw-validate).

### Services
{: #services}

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
