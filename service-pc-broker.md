---

copyright:

  years: 2022

lastupdated: "2022-06-03"

keywords: service brokers, IBM Cloud platform, new service brokers, hosting service broker, OSB, open service broker, partner center

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Developing, hosting, and testing your service brokers
{: #broker-dev-host}

The {{site.data.keyword.Bluemix_notm}} platform interacts with service brokers to create and manage service instances and service bindings. You can build your broker by using a combination of our public {{site.data.keyword.Bluemix_notm}} service broker samples, Open Service Broker Reference App, and the Open Service Broker API documentation.
{: shortdesc}

When you onboard your service to {{site.data.keyword.cloud}}, you must build one or more service brokers to manage the lifecycle of your service and metering integration. For more information, see [Metering Integration](/docs/sell?topic=sell-service-metering-integration).


## Before you begin
{: #pc-broker-pre-reqs}

* [Register your service in {{site.data.keyword.Bluemix_notm}} Partner Center](/docs/sell?topic=sell-svc-register).
* [Define the product details of your service](/docs/sell?topic=sell-svc-define).
* Review the [Provisioning scenario](/docs/sell?topic=sell-how-it-works#provision2) to gain an understanding of how resource creation works.
* Read and familiarize yourself with the [Open Broker API spec](https://github.com/openservicebrokerapi/servicebroker/blob/v2.12/spec.md){: external}, and use the readme file as a guide to learn more. {{site.data.keyword.Bluemix_notm}} uses the Open Service Broker API (OSB) `version 2.12` specification.

## Building your broker
{: #pc-broker-guides}

Configure and deploy a broker that has your required specifications by using the following steps: 

Explore [broker samples](https://github.com/IBM/sample-resource-service-brokers){: external} to see how you can structure your broker to meet requirements. Not all languages are represented by a sample.
{: tip}

1. Go to [Open Service Broker Reference App](https://github.com/IBM-Cloud/onboarding-osb){: external} as a guide to create your broker. The reference app provides step-by-step instructions to configure, deploy on {{site.data.keyword.codeenginefull_notm}}, and test your broker. 
1. Go to [{{site.data.keyword.Bluemix_notm}} Open Service Broker API](/apidocs/resource-controller/ibm-cloud-osb-api){: external} to set required specifications, including required endpoints. 

### Including required endpoints
{: #pc-endpoints}

All service brokers must set certain required endpoints. Additional endpoint logic is required for bindable services and disabling and re-enabling service instances.

#### Required endpoint logic for all service brokers
{: #pc-endpoint-sb}

Service brokers must provide a standard set of metadata values that are consumed by REST APIs, and {{site.data.keyword.Bluemix_notm}} brokers must have logic for the following REST API endpoints or paths:

catalog (GET)
:   Returns your catalog metadata included in your broker. 

resource instances (PUT)
:   Creates your service instance.

resource instances (DELETE)
:   Deletes your service instance.

resource instances (PATCH)
:   Updates your service instance.

**Note on catalog (GET)**: This endpoint defines the contract between the broker and the {{site.data.keyword.Bluemix_notm}} platform for the services and plans that the broker supports. This endpoint returns the catalog metadata that is stored within your broker. These values define the minimal provisioning contract between your service and the {{site.data.keyword.Bluemix_notm}} platform. All additional catalog metadata that isn't required for provisioning is stored within the {{site.data.keyword.Bluemix_notm}} catalog. Any updates to catalog display values like links and icons must be updated in the {{site.data.keyword.Bluemix_notm}} console, and not housed in your broker. None of metadata that is stored in your broker is displayed in the {{site.data.keyword.Bluemix_notm}} console or the {{site.data.keyword.Bluemix_notm}} CLI. The console and CLI return what was set within Partner Center Sell and stored in the {{site.data.keyword.Bluemix_notm}} catalog. The following section shows the minimal-required values that catalog (GET) returns:

```text
{
       "services": [{
           "id": "ibmcloud-link",
           "name": "ibmcloud-link",
           "description": "An IBM provided service that enables aliasing to service instances in the IBM Cloud.",
           "bindable": true,
           "plan_updateable": false,
           "plans": [
               {
                   "id": "ibmcloud-link-alias",
                   "name": "ibmcloud-alias",
                   "free": true,
                   "description": "The IBM Cloud alias plan used for linking."
               }
               ]
       }]
}
```

#### Required endpoints logic for bindable services
{: #pc-bindable}

If your service can be bound to applications in {{site.data.keyword.Bluemix_notm}}, it must return API endpoints and credentials to your service consumers. A bindable service must use the bindable operations in the Open Service Broker specification, and implement the following endpoints or paths:

bindings and credentials (PUT)
:   Binds your service instance to an application.

bindings and credentials (DEL)
:   Unbinds your service instance from an application.

#### Required {{site.data.keyword.Bluemix_notm}} extension endpoints
{: #pc-extension}

The OSB specification doesn't support a disabled instance state. A disabled state includes a missing payment or other situations that result in an account suspension (but not yet cancellation) and is different from a deleted instance state. In order for {{site.data.keyword.Bluemix_notm}} to support customers that might experience a disabled state, {{site.data.keyword.Bluemix_notm}} defined the extended API endpoints that allow service instances to be disabled and re-enabled. The following endpoint extensions are required:

enable and disable instances (GET)
:   Status - returns the state of your service instance.

enable and disable instances (PUT)
:   Enable or disable a service instance.

It's the service provider's responsibility to disable access to the service instance when the disable endpoint starts and to re-enable that access when the enable endpoint is started.
{: note}

### Broker information provided by the {{site.data.keyword.Bluemix_notm}} platform
{: #pc-broker-info}

Your service broker or brokers receive the following information from the {{site.data.keyword.Bluemix_notm}} platform:

#### X-Broker-API-Originating-Identity
{: #pc-x-broker}

The **user identity header** is provided through an API originating identity header. This request header includes the user's {{site.data.keyword.Bluemix_notm}} IAM Identity. The IAM Identity is base64 encoded. {{site.data.keyword.Bluemix_notm}} supports a single authentication realm: `IBMid`. The `IBMid` realm uses an IBMid Unique ID (IUI) to identify the user's identity in {{site.data.keyword.Bluemix_notm}}. This IUI is an opaque string to the service provider.

Example:

```text
X-Broker-API-Originating-Identity: ibmcloud eyJpYW1faWQiOiJJQk1pZC01MEdOUjcxN1lFIn0=
Decoded:
{"iam_id":"IBMid-50GNR717YE"}
```
{: codeblock}

#### API header version
{: #pc-api-header}

The **API version header** is [2.12](https://github.com/openservicebrokerapi/servicebroker/blob/v2.12/spec.md){: external}. For example: `X-Broker-Api-Version: 2.12`.

#### resource instance (PUT) body.context and resource instance (PATCH) body.context
{: #put}

`PUT /v2/service_instances/:resource_instance_id` and `PATCH /v2/service_instances/:resource_instance_id` receive the following value within **body.context**: `{ "platform": "ibmcloud", "account_id": "tracys-account-id", "crn": "resource-instance-crn" }`.

### Additional broker recommendations
{: #pc-more-info}

#### Recommendations on using asynchronous instead of synchronous operations
{: #pc-asynch-ops}

The OSB API supports both synchronous and asynchronous modes of operation. If your operations are going to take less than 10 seconds, you must use synchronous responses. Otherwise, you must use the asynchronous mode of operation. The asynchronous mode requires the `last_operation` endpoint. For more information, see [Get the status of a provision in-progress for a service instance](/apidocs/resource-controller/ibm-cloud-osb-api).

#### Recommendations for managing brokers across locations
{: #pc-managing-broker}

It's important for users to understand the location of their cloud services for latency, availability, and data residency.

When you're creating service instances on {{site.data.keyword.Bluemix_notm}}, one of the required parameters your users provide is the location where they want that service instance to be created. Some services can support creation in multiple locations. For example, a database service can support creation in all {{site.data.keyword.Bluemix_notm}} regions or it can support a subset.

If your third-party API-based service is implemented in another cloud and exposed into {{site.data.keyword.Bluemix_notm}}, the location indicates the service's location in the other cloud.

When you onboard to {{site.data.keyword.Bluemix_notm}}, you must implement at least one OSB broker. You can have more than one broker depending on your deployment strategy and the locations you want to support for your service. Within Partner Center Sell, you establish the mapping between your pricing plan and the broker. The typical choices are to define a single broker to service all locations for your service or to define a broker per location; this choice is up to the service provider.

For a list of available locations, review the [{{site.data.keyword.IBM_notm}} global catalog locations](https://globalcatalog.cloud.ibm.com//search?q=kind:geography){: external}. If your service requires more locations to be defined, consult the {{site.data.keyword.Bluemix_notm}} onboarding team.

## Hosting your brokers
{: #pc-host}

Your broker must be hosted as part of an application that can respond to REST API calls and your hosted location must meet {{site.data.keyword.Bluemix_notm}} security guidelines. You might host your broker in {{site.data.keyword.Bluemix_notm}}, or it can be hosted externally, if it's publicly accessible from {{site.data.keyword.Bluemix_notm}} itself.

To host your broker outside of {{site.data.keyword.IBM_notm}}, you must ensure that it meets the following security guidelines:
- Must follow Transport Layer Security (TLS) protocol version 1.2. For more information, see [TLS protocol overview](https://www.ibm.com/docs/en/sdk-java-technology/8?topic=provider-tls-protocol-overview){: external}.
- Must be hosted on a valid HTTPs endpoint that is accessible on the public internet


## Testing your service's broker
{: #pc-broker-test}

You must validate your broker by running curl commands against the different endpoints that you enable. You need the hosted location of your service broker and the URL and credentials that are associated with your application. To test your broker, use the following methods:  

* The sample readme file guidance for curling your OSB endpoints: [https://github.com/IBM/sample-resource-service-brokers/blob/master/README.md](https://github.com/IBM/sample-resource-service-brokers/blob/master/README.md){: external}.
* The Open Service Broker Reference App guidance for testing your broker: [Testing the broker](https://github.com/IBM-Cloud/onboarding-osb#testing-the-broker){: external}

### Example curl request
{: #pc-curl-broker}

Use the following example to test your brokers curl response:

```bash
curl -X PUT  https://<sample-service-broker>/v2/service_instances/<encoded-resource-crn> \
     -u '<your broker user>:<your broker password>' \
     -H 'content-type: application/json' \
      -d '{ "context": {"platform": "ibmcloud", \
                        "account_id": "34ff5928-c3c7-4d46-bbf6-1a5628c325d1", \
                        "resource_group_crn": "crn:v1:bluemix:public:resource-controller::a/003e9bc3993aec710d30a5a719e57a80::resource-group:b4570a825f7f4d57aa54e8e1d9507926", \
                        "crn": "<resource-crn>", \
                        "target_crn": "<target_crn>"}, \
            "service_id": "a07f025c-90db-4652-afd1-cf4adfac93c8", \
            "plan_id": "fe442cec-2eef-41fe-9f92-58d6c094584f"}'
```
{: codeblock}