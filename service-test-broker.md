---

copyright:

  years: 2023, 2024

lastupdated: "2024-06-10"

keywords: service brokers, test service broker, IBM Cloud platform, new service brokers, OSB, open service broker, partner center, modify service broker, common errors, scalability

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Modifying and testing your service brokers
{: #broker-modify-test}

After you build a skeleton application for your service broker, you must modify the code to make it specific for the service that you want to connect your broker to. Also, you must test your service broker by running curl commands against the different endpoints that you enable, or by creating a service instance in the {{site.data.keyword.cloud_notm}} catalog.
{: shortdesc}

## Before you begin  
{: #before-modifying-testing}

Before you can modify and test a service broker, you must complete the following task:

* [Build and host your service broker](/docs/sell?topic=sell-broker-dev-host)

## Modifying your service broker
{: #pc-modify-broker}

After you build a skeleton application for your service broker, you must modify the code to make it specific for the service that you want to connect your broker to. You can create your service-specific code by updating the file and function name for each of the tasks that you want to configure for your service. For more information about the tasks that you can configure for your service, see the following readme file: [https://github.com/OSB-Onboarding/osb-spring-server#readme](https://github.com/OSB-Onboarding/osb-spring-server#readme){: external} 

## Testing your service broker
{: #pc-broker-test}

To ensure that your broker is configured properly, you must test it. You can either test it by running curl commands against the different endpoints that you enable, or by using the {{site.data.keyword.cloud_notm}} console to create a service instance.

### Testing your service broker by running curl commands
{: #pc-test-curl}

You can validate your broker by running curl commands against the different endpoints that you enable. You need the hosted location of your service broker and the URL and credentials that are associated with your application. To test your broker, use the following methods:  

* The sample readme file for curling your OSB endpoints: [https://github.com/IBM/sample-resource-service-brokers/blob/master/README.md](https://github.com/IBM/sample-resource-service-brokers/blob/master/README.md){: external}
* The sample broker code that uses Java code language: [https://github.com/OSB-Onboarding/osb-spring-server](https://github.com/OSB-Onboarding/osb-spring-server){: external}
* The sample broker code that uses Node.js code language: [https://github.com/OSB-Onboarding/osb-nodejs-server-server](https://github.com/OSB-Onboarding/osb-nodejs-server-server){: external}
* The Open Service Broker Automation Reference App guidance for testing your broker: [https://github.com/IBM/open-service-broker-automation](https://github.com/IBM/open-service-broker-automation){: external}

### Example curl request
{: #pc-curl-broker}

Use the following example to test your broker's curl response:

```bash
curl -X PUT --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'X-Broker-API-Version: 2.17' -d '{ \ 
   "context": {
     "platform": "ibmcloud",
      "account_id": "003e9bc3993aec710d30a5a719e57a80",
      "crn": "crn:v1:bluemix:public:compose-redis:us-south:a/003e9bc3993aec710d30a5a719e57a80:416d769b-682d-4833-8bd7-5ef8778e5b52",
      "resource_group_crn": "crn:v1:bluemix:public:resource-controller::a/003e9bc3993aec710d30a5a719e57a80::resource-group:b4570a825f7f4d57aa54e8e1d9507926"
     },
   }, \ 
   "maintenance_info": { \ 
     "description": "string", \ 
     "version": "string" \ 
   }, \ 
   "parameters": {
    "location": "us-south",
    "optional-param":"parameter required by your service"
   }, \ 
   "plan_id": "ecc19311-aba2-49f7-8198-1e450c8460d4", \ 
   "service_id": "0bc9d744-6f8c-4821-9648-2278bf6925bb" \ 
 }' 'https://osb-spring-app.yoa0uliv52z.us-south.codeengine.appdomain.cloud/v2/service_instances/instance_id_1234'
```
{: codeblock}

The previous curl request returns the following response body:

```bash
{
	"dashboard_url": "http://www.ibm.com/objectstorage/crn:v1:bluemix:public:cloud-object-storage:global:a%2F4329073d16d2f3663f74bfa955259139:8d7af921-b136-4078-9666-081bd8470d94::",
	"metadata": {
    "displayName": "Test Node Resource Service Broker",
    "documentationUrl": "http://10.0.1.2/documentation.html",
    "imageUrl": "http://10.0.1.2/servicesample.png",
    "instructionsUrl": "http://10.0.1.2/servicesample.md",
    "longDescription": "Description for Test Node Resource Service Broker.",
    "providerDisplayName": "Example Corp.",
    "supportUrl": "http://10.0.1.2/support.html",
    "termsUrl": "http://10.0.1.2/terms.html"
  },
}
```
{: codeblock}

### Getting the catalog metadata stored within the broker
{: #get-catalog-data}

You can programmatically get the catalog metadata that is stored within the service broker by calling the {{site.data.keyword.cloud_notm}} Open Service Broker API as shown in the following sample request. For more information about the API command, see [{{site.data.keyword.cloud_notm}} Open Service Broker API](/apidocs/resource-controller/ibm-cloud-osb-api#list-catalog).

Use the following example to return the catalog metadata that is stored within your broker:

```bash
curl --request GET \
  --url https://osb-spring-app.yoa0uliv52z.us-south.codeengine.appdomain.cloud/v2/catalog \
  --header 'Accept: application/json' \
  --header 'Content-Type: application/json' \
  --header 'X-Broker-API-Version: 2.17'
```
{: codeblock}

The previous curl request returns the following response body:

```bash
{
	"services": [
    {
      "bindable": true,
      "description": "Short description for Test Node Resource Service Broker.",
      "id": "dff97f5c-bc5e-4455-b470-411c3edbe49c",
      "metadata": {
        "displayName": "Test Node Resource Service Broker",
        "documentationUrl": "http://10.0.1.2/documentation.html",
        "imageUrl": "http://10.0.1.2/servicesample.png",
        "instructionsUrl": "http://10.0.1.2/servicesample.md",
        "longDescription": "Extended description for Test Node Resource Service Broker.",
        "providerDisplayName": "Example corp.",
        "supportUrl": "http://10.0.1.2/support.html",
        "termsUrl": "http://10.0.1.2/terms.html"
      },
      "name": "testnoderesourceservicebroker",
      "plan_updateable": true,
      "tags": [
        "lite",
        "tag1a",
        "tag1b"
      ],
      "plans": [
        {
          "description": "The plan description for Test Node Resource Service Broker.",
          "free": true,
          "id": "ecc19311-aba2-49f7-8198-1e450c8460d4",
          "metadata": {
            "bullets": [
              "Test bullet 1",
              "Test bullet 2"
            ],
            "displayName": "Lite"
          },
          "name": "lite"
        }
      ]
    }
  ]
}
}
```
{: codeblock}

### Testing your service broker by using the {{site.data.keyword.cloud_notm}} console
{: #pc-test-console}

After you test your service broker by running curl commands, you can also test it by using the {{site.data.keyword.cloud_notm}} console. You can preview the catalog tile of your product and check whether your service broker works properly before you publish your product through Partner Center - Sell.

To test your broker by using the {{site.data.keyword.cloud_notm}} console, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center > My products**.
1. Select the product that you're onboarding, and go to **Catalog entry**.
1. Click **View catalog entry**.
1. On your catalog listing page, click **Create**. With this step, you create a service instance of your product and you are directed to the service instance page.
1. Complete any action that can trigger metering events.
1. Then, return to the {{site.data.keyword.cloud_notm}} console, click **Manage > Billing and usage > Usage** and check the Services section to see whether your service instance generated usage events for your product.

## Receiving common error codes
{: #error-manage}

If any issue occurs while you're managing your service broker, you might see that the response body contains an `error_code` property. See the following error code that you can receive:

RC-ServiceBrokerErrorResponse
:   This error code is returned by your service broker.

See the following example of this error code:

```bash
{
   "error_code": "RC-ServiceBrokerErrorResponse",
   "message": "Service Broker returned error status code 403",
   "status_code": 400,
   "transaction_id": "7e0090047662faf2670ae36ffbe02011"
}
 ```
{: codeblock}

If you receive this type of error code, go to the [Support center](/unifiedsupport/supportcenter){: external} and create a support case. For more information, see [Getting support](/docs/get-support?topic=get-support-using-avatar#getting-support).

