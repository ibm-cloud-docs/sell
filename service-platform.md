---

copyright:

  years: 2018, 2025

lastupdated: "2025-12-02"

keywords: IBM Cloud platform, integrated billing services, lifecycle of IBM Cloud resources, provisioning layer

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# How third-party services use the {{site.data.keyword.cloud_notm}} platform
{: #how-it-works}

A third-party service uses the {{site.data.keyword.cloud_notm}} platform for authentication, access, self-service instance creation, metering, and billing. This topic provides a high-level overview of the platform components that your service uses, and pulls these concepts together into an end-to-end provisioning scenario.
{: shortdesc}


## The {{site.data.keyword.cloud_notm}} provisioning layer
{: #provisioning-layer}

The provisioning layer manages the lifecycle of {{site.data.keyword.cloud_notm}} resources. The provisioning layer is responsible for controlling and tracking the lifecycle of resources in a customer account. *Resources* are physical or logical components that can be created or reserved for an application or service instance. Examples of resources include database, accounts, processor, memory, and storage limits. In general, resources that are tracked by the provisioning layer are intended to associate usage metrics and billing, but that isn’t always the case. In some cases, the resource might be associated to the provisioning layer to ensure that the resource lifecycle can be managed along with the account lifecycle.

### Resource lifecycle management
{: #lifecycle}

The provisioning layer provides common APIs to control the lifecycle of resources from creation (creating an instance) to service credentials (creating and removing access credentials) to deletion (deleting an instance). Additionally, the {{site.data.keyword.cloud_notm}} platform provides CLIs and a UI that can manage the lifecycle of these resources that don’t require you to create your own facilities.

The provisioning layer provides APIs to help you manage the following elements of your resource lifecycle:
* Creating a resource instance
* Updating a resource instance
* Creating service credentials
* Removing service credentials
* Resource keys
* Deleting a resource instance

## {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM)
{: #iam}

Identity Access Management (IAM) enables you to securely authenticate users and control access to all cloud resources consistently across {{site.data.keyword.cloud_notm}}. The {{site.data.keyword.cloud_notm}} provisioning layer adopted IAM for authentication and authorization of actions that are taken against the provisioning layer. Third-party product providers use IAM to create an authentication flow (OAuth). See [What is IAM?](/docs/account?topic=account-iamoverview) for more information.

If your product uses OpenID Connect (OIDC) libraries, IAM supports OIDC integration. OIDC is an authentication layer built on OAuth 2.0, an authorization framework and can help simplify the onboarding process. For more information on OIDC, see [Open ID Connect](https://openid.net/developers/how-connect-works/){: external}.

## {{site.data.keyword.cloud_notm}} catalog
{: #catalog}

The {{site.data.keyword.cloud_notm}} catalog stores and displays the product definitions (descriptions, features, images, URLs, keywords, and other product definitions) of the product that you onboard. {{site.data.keyword.cloud_notm}} Partner Center provides a way to define all aspects of your service's required metadata. You can find detailed information about the required and optional metadata fields on the Dashboard, Product details, and Pricing tabs in Partner Center. This metadata is published and displayed in the catalog. Take a look at the following key items to jumpstart your understanding:

Programmatic name
:   The programmatic name is your product's unique ID and is used within all IBM services and tools. This name is not the display name of your product that customers see in the {{site.data.keyword.cloud_notm}} catalog. The programmatic name is automatically generated from your company name and the display name of your product.

Display name
:   A name for your service. This name is publicly displayed in the {{site.data.keyword.cloud_notm}} catalog. For example, `Compose Redis`

Service ID
:   A service ID is used to identify your service when it communicates with other {{site.data.keyword.cloud_notm}} services. You're also required to create an API key for your service ID.

Company or product logo
:   An SVG file with your product logo.

Short description
:   The short description of what your product is, its value, and any other details that you want to be displayed in your {{site.data.keyword.cloud_notm}} catalog entry. You can add a single sentence or phrase as the description.

Detailed description
:   This description is displayed at the beginning of your product page in the catalog. Include relevant keywords and consider at least two sentences for a detailed description.

Documentation URL
:   A link to your {{site.data.keyword.cloud_notm}} documentation.

End User License Agreement (EULA) URL
:   A link to the end user license agreement that users must agree with to use your product. Do not include billing, payment, or tax terms in this agreement.

Category
:   Selection of available {{site.data.keyword.cloud_notm}} categories that best describe your product. Only one category can be selected.

Keywords
:   Words, phrases, and other key search terms associated with your product.

Features
:   Short descriptive unique identifiers about your product's attributes.

Media
:   Screen captures and videos that show off your product.

Plan name
:   A name for your pricing plan that doesn't include your company or product name. This information is displayed to customers in the {{site.data.keyword.cloud_notm}} catalog. For example, `Gold`

Plan description
:   The description of the pricing plan. This information is displayed to customers in the {{site.data.keyword.cloud_notm}} catalog.

Programmatic name of the plan
:   The technical name of the pricing plan that is automatically generated. You can't make edits to this name.

## Open Service Broker
{: #open-service}

Service brokers manage the lifecycle of services. The {{site.data.keyword.cloud_notm}} platform interacts with service brokers to create and manage service instances and service bindings. Service bindings are the representation of an association between an application and a service instance, which often include the credentials that the application uses to communicate with the service instance. Providing valid metadata values creates a successful REST API response when a request is performed.

{{site.data.keyword.cloud_notm}} uses the Open Service Broker API (OSB) `version 2.12` specification. Read through and familiarize yourself with the [Open Broker API spec](https://github.com/cloudfoundry/servicebroker/blob/v2.12/spec.md){: external}, and use the readme file as a guide to learn more.

When the resource controller receives a request to create a resource, it calls your OSB to validate the service type, product, plans, and regions availability. The resource controller also validates the visibility of the plan that is associated with the customer account. {{site.data.keyword.cloud_notm}} provides broker samples and API docs that extend the OSB spec. You can find more details about developing and hosting your broker as you walk through the detailed integrated billing onboarding development steps.

## {{site.data.keyword.cloud_notm}} metering service
{: #metering-service}

If a service offers a metered plan, {{site.data.keyword.cloud_notm}} users are charged based on the amount of resources that they use. For example, {{site.data.keyword.cloud_notm}} users that use database services might be charged based on the amount of storage that their applications use. Usage submission must occur in order for the usage to be converted into a chargeable record.

All integrated billing services that offer a metered plan must use the {{site.data.keyword.cloud_notm}} metering service to report usage data.

You’re required to automate hourly usage submission by using metering service API if you offer a metered plan.

For more information on metering, see [Metering integration](/docs/sell?topic=sell-service-metering-integration). For more information about submitting metered usage, see [Submitting usage for metered plans](/docs/sell?topic=sell-service-add-metrics#submit-usage).

## Creation scenario: Pulling it all together
{: #provision2}

Now let's pull all of the concepts together and look at an example of how service instance creation works by using the {{site.data.keyword.cloud_notm}} platform.

![Provisioning scenario](images/flow-am.svg "How the platform handles service instance creation"){: caption="Figure 1. How the platform handles service instance creation" caption-side="bottom"}

### Creating a service instance by using the console
{: #service-instance-ui}
{: ui}

When a user wants to create a service instance, they can select the service, plan, and use the **Create** operation.

The {{site.data.keyword.cloud_notm}} platform validates that the user has permission to create the service instance by using {{site.data.keyword.cloud_notm}} IAM. After this validation occurs, your service broker's creation endpoint (`PUT /v2/resource_instances/:resource_instance_id`) is started. For the instance to be created, the following rules must be met:
* The {{site.data.keyword.cloud_notm}} context is included in the context variable
* The `X-Broker-API-Originating-Identity` has the IBM IAM ID of the user that started the request
* The parameters section includes the requested location (and more parameters that are required by your service).

Example request for creating an instance:

```text
    PUT /v2/service_instances/crn%3Av1%3Abluemix%3Apublic%3Acompose-redis%3Aus-south%3Aa%2F46aa677e-e83f-4d17-a2b6-5b752564477c%3A416d769b-682d-4833-8bd7-5ef8778e5b52?accepts_incomplete=true HTTP/1.1
    Host:  https://broker.compose.cloud.ibm.com
    Authorization: basic dXNlcjpwYXNzd29yZA==
    X-Broker-Api-Version: 2.12
    X-Broker-API-Originating-Identity: ibmcloud aWJtaWQtNDU2MzQ1WA==
    {
      "service_id": "0bc9d744-6f8c-4821-9648-2278bf6925bb", // your service's GUID from onboarding
      "plan_id": "ecc19311-aba2-49f7-8198-1e450c8460d4", //your plan's GUID from onboarding
      "context": {
        "platform": "ibmcloud",
        "account_id": "003e9bc3993aec710d30a5a719e57a80",
        "crn": "crn:v1:bluemix:public:compose-redis:us-south:a/003e9bc3993aec710d30a5a719e57a80:416d769b-682d-4833-8bd7-5ef8778e5b52",
        "resource_group_crn": "crn:v1:bluemix:public:resource-controller::a/003e9bc3993aec710d30a5a719e57a80::resource-group:b4570a825f7f4d57aa54e8e1d9507926",
        "target_crn": "crn:v1:bluemix:public:resource-catalog::a/e97a8c01ac694e308ef3ad7795c7cdb3::deployment:e62e2c19-0c3b-41e3-b8b3-c71762ecd489:us-south38399"
      },
      "parameters": {
        "location": "us-south",
        "optional-param":"parameter required by your service"
      }
    }
```

### Creating a service instance by using the CLI
{: #service-instance-cli}
{: cli}

When a user wants to create a service instance, they can use `ibmcloud cli [ ibmcloud resource service-instance-create NAME SERVICE_NAME SERVICE_PLAN_NAME LOCATION ]`.

The {{site.data.keyword.cloud_notm}} platform validates that the user has permission to create the service instance by using {{site.data.keyword.cloud_notm}} IAM. After this validation occurs, your service broker's creation endpoint (PUT /v2/resource_instances/:resource_instance_id) is started. For the instance to be created, the following rules must be met:
* The {{site.data.keyword.cloud_notm}} context is included in the context variable
* The `X-Broker-API-Originating-Identity` has the IBM IAM ID of the user that started the request
* The parameters section includes the requested location (and more parameters that are required by your service).

Example request for creating an instance:

```text
    PUT /v2/service_instances/crn%3Av1%3Abluemix%3Apublic%3Acompose-redis%3Aus-south%3Aa%2F46aa677e-e83f-4d17-a2b6-5b752564477c%3A416d769b-682d-4833-8bd7-5ef8778e5b52?accepts_incomplete=true HTTP/1.1
    Host:  https://broker.compose.cloud.ibm.com
    Authorization: basic dXNlcjpwYXNzd29yZA==
    X-Broker-Api-Version: 2.12
    X-Broker-API-Originating-Identity: ibmcloud aWJtaWQtNDU2MzQ1WA==
    {
      "service_id": "0bc9d744-6f8c-4821-9648-2278bf6925bb", // your service's GUID from onboarding
      "plan_id": "ecc19311-aba2-49f7-8198-1e450c8460d4", //your plan's GUID from onboarding
      "context": {
        "platform": "ibmcloud",
        "account_id": "003e9bc3993aec710d30a5a719e57a80",
        "crn": "crn:v1:bluemix:public:compose-redis:us-south:a/003e9bc3993aec710d30a5a719e57a80:416d769b-682d-4833-8bd7-5ef8778e5b52",
        "resource_group_crn": "crn:v1:bluemix:public:resource-controller::a/003e9bc3993aec710d30a5a719e57a80::resource-group:b4570a825f7f4d57aa54e8e1d9507926",
        "target_crn": "crn:v1:bluemix:public:resource-catalog::a/e97a8c01ac694e308ef3ad7795c7cdb3::deployment:e62e2c19-0c3b-41e3-b8b3-c71762ecd489:us-south38399"
      },
      "parameters": {
        "location": "us-south",
        "optional-param":"parameter required by your service"
      }
    }
```

### Creating a service instance by using the API
{: #service-instance-api}
{: api}

This action can be done only through the UI or CLI. To see the steps, switch to the UI or CLI instructions.

The {{site.data.keyword.cloud_notm}} platform validates that the user has permission to create the service instance by using {{site.data.keyword.cloud_notm}} IAM. After this validation occurs, your service broker's creation endpoint (PUT /v2/resource_instances/:resource_instance_id) is started. For the instance to be created, the following rules must be met:
* The {{site.data.keyword.cloud_notm}} context is included in the context variable
* The `X-Broker-API-Originating-Identity` has the IBM IAM ID of the user that started the request
* The parameters section includes the requested location (and more parameters that are required by your service).

Example request for creating an instance:

```text
    PUT /v2/service_instances/crn%3Av1%3Abluemix%3Apublic%3Acompose-redis%3Aus-south%3Aa%2F46aa677e-e83f-4d17-a2b6-5b752564477c%3A416d769b-682d-4833-8bd7-5ef8778e5b52?accepts_incomplete=true HTTP/1.1
    Host:  https://broker.compose.cloud.ibm.com
    Authorization: basic dXNlcjpwYXNzd29yZA==
    X-Broker-Api-Version: 2.12
    X-Broker-API-Originating-Identity: ibmcloud aWJtaWQtNDU2MzQ1WA==
    {
      "service_id": "0bc9d744-6f8c-4821-9648-2278bf6925bb", // your service's GUID from onboarding
      "plan_id": "ecc19311-aba2-49f7-8198-1e450c8460d4", //your plan's GUID from onboarding
      "context": {
        "platform": "ibmcloud",
        "account_id": "003e9bc3993aec710d30a5a719e57a80",
        "crn": "crn:v1:bluemix:public:compose-redis:us-south:a/003e9bc3993aec710d30a5a719e57a80:416d769b-682d-4833-8bd7-5ef8778e5b52",
        "resource_group_crn": "crn:v1:bluemix:public:resource-controller::a/003e9bc3993aec710d30a5a719e57a80::resource-group:b4570a825f7f4d57aa54e8e1d9507926",
        "target_crn": "crn:v1:bluemix:public:resource-catalog::a/e97a8c01ac694e308ef3ad7795c7cdb3::deployment:e62e2c19-0c3b-41e3-b8b3-c71762ecd489:us-south38399"
      },
      "parameters": {
        "location": "us-south",
        "optional-param":"parameter required by your service"
      }
    }
```

### Understanding the {{site.data.keyword.cloud_notm}} `context` parameter
{: #parameter}

In the previous example, you can see the metadata returned in the `context` parameter. The context for {{site.data.keyword.cloud_notm}} returns the following:

* **platform**: Identifies the platform as `ibmcloud`

* **"account_id"**: Returns the ID of the account in {{site.data.keyword.cloud_notm}} that is creating the service instance.

* **crn**: When a customer creates your service in {{site.data.keyword.cloud_notm}}, a service instance is created, and this instance is identified by its {{site.data.keyword.cloud_notm}} Resource Name (CRN). The CRN is used in all aspects of the interaction with {{site.data.keyword.cloud_notm}} including creating instances, binding (creating credentials and endpoints), metering, dashboard display, and access control. From a product provider perspective, the CRN can largely be treated as an opaque string to be used with the {{site.data.keyword.cloud_notm}} APIs. It can also be decomposed by using the following structure:

   ```text
   crn:version:cname:ctype:service-name:location:scope:service-instance:resource-type:resource
   ```

   In the provisioning sample we see that the `compose-redis` service CRN is:

   ```text
   crn:v1:bluemix:public:compose-redis:us-south:a/46aa677e-e83f-4d17-a2b6-5b752564477c:416d769b-682d-4833-8bd7-5ef8778e5b52::
   ```

   In this sample, this `compose-redis` instance is part of {{site.data.keyword.cloud_notm}} account with ID. The unique ID for the instance is `416d769b-682d-4833-8bd7-5ef8778e5b52`, and the instance is hosted in the `us-south` region of the public {{site.data.keyword.cloud_notm}}.

* **resource_group_crn**: Returns the resource group that includes the service instance. For more details, see [Managing resource groups](/docs/account?topic=account-rgs).

   You typically aren't concerned with the `resource_group_crn` except in unique circumstances. Consult your IBM representative on your use case before you use that field.
   {: note}
