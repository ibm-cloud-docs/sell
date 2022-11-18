---

copyright:

  years: 2018, 2022

lastupdated: "2022-11-18"

keywords: billing service, resource management console, Open Service Broker, end-to-end 

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Checklist for selling services on {{site.data.keyword.cloud_notm}}
{: #checklist}

Use the following checklists to track all the tasks required to define, develop, and publish your third-party service.
{: shortdesc}

## Register your product
{: #register}

| Task | Description | Environment |
|------|-------------|-------------|
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Provide your company name | Specify the legal name of your company.  | {{site.data.keyword.cloud_notm}} console | 
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Create a test environment | The test environment is not needed for services, but is necessary for software. If you onboard software in the future, you use the test environment to validate that it's ready for use. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Assign team access | With the correct {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) access, members of your team can help onboard your service. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Invite team members to your account | Members of your account are assigned the IAM access that you set up in the previous task. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Confirm your legal agreement with {{site.data.keyword.IBM_notm}} | Review and submit the {{site.data.keyword.IBM_notm}} Digital Provider Agreement if you plan to offer free plans, or upload your custom digital provider agreement to be reviewed and approved by {{site.data.keyword.IBM_notm}}. | {{site.data.keyword.cloud_notm}} console |
{: caption="Table 1. Getting started tasks for selling services" caption-side="top"} 

For more information, see [Getting set up to sell services](/docs/sell?topic=sell-get-started).

## Defining your service
{: #define}

| Task | Description | Environment |
|------|-------------|-------------|
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Confirm your display and programmatic names | Review the programmatic name that was generated for you and make any needed updates. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Verify your partner details | Review the Company and Team information and make sure that everything is correct. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Create your service ID | Create your service ID that is used to identify your service when communicating with other {{site.data.keyword.cloud_notm}} services.  | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Create your API key | Create an API key that is used to authenticate your service ID. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Define your product details | Add details, such as your product logo, keywords, description, features, and documentation URL for your product's entry and details page in the {{site.data.keyword.cloud_notm}} catalog. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Define your support details | Provide your support site URL, contacts, escalation process, and the locations where your support teams are based. | {{site.data.keyword.cloud_notm}} console |
{: caption="Table 2. Tasks for defining service details" caption-side="top"} 

For more information, see the following links:

* [Define the product details of your service](/docs/sell?topic=sell-svc-define)
* [Defining your support experience](/docs/sell?topic=sell-saas-support-details&interface=ui)

## Defining your pricing plan 
{: #pricing}

| Task | Description | Environment |
|------|-------------|-------------|
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Submit the Electronic Transfer Funds and tax form | To receive payment disbursements for usage-based pricing plans, email the required documents. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Add your ECCN | Add the Export Control Classification Number (ECCN) that applies to your product. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Add your UNSPSC | Add the United Nations Standard Products and Services Code (UNSPSC) that applies to your product. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Add your pricing plans | {{site.data.keyword.cloud_notm}} supports two pricing models: free or usage-based. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Add metrics to your pricing plan | Add metrics to your usage-based pricing plan to determine how customers are charged. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Test and submit resource usage | Review how customers understand and experience your pricing plan, and validate that your metered plans are correctly configured by enabling and submitting a usage test. This usage test includes creating your metering JSON, calling the Usage Metering API and submitting metering evidence. For more information, see [Usage Metering API](/apidocs/usage-metering#report-resource-usage){: external}. | Development environment and documentation, {{site.data.keyword.cloud_notm}} console  |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Review and submit the {{site.data.keyword.cloud_notm}}'s Digital Platform Reseller Agreement | Review and submit the Digital Platform Reseller Agreement if you plan to offer paid plans, or upload your custom digital provider agreement to be reviewed and approved by {{site.data.keyword.IBM_notm}}. | {{site.data.keyword.cloud_notm}} console |
{: caption="Table 3. Tasks for add pricing plans for services" caption-side="top"} 

For more information, see the following links:

* [Defining your pricing plan](/docs/sell?topic=sell-service-pricing-info&interface=ui)
* [Add a pricing plan for your service](/docs/sell?topic=sell-svc-pricing&interface=ui)
* [Adding metrics to your service](/docs/sell?topic=sell-service-add-metrics&interface=ui)

## Developing your broker
{: #develop}

| Task | Description | Environment |
|------| ----------| ------------ |
|![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Learn about the Open Service Broker specification version 2.12 | Service brokers manage the lifecycle of services. The {{site.data.keyword.Bluemix_notm}} platform interacts with Open Service Brokers to create and manage service instances and service bindings. For more information, see [Open Broker API spec](https://github.com/openservicebrokerapi/servicebroker/blob/v2.12/spec.md){: external}.| Documentation |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") View the {{site.data.keyword.Bluemix_notm}} broker samples |  Clone the repo, browse the broker samples, and use these samples to start development. For more information, see [Sample Resource Service Brokers](https://github.com/IBM/sample-resource-service-brokers){: external}. | Code examples |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") View the {{site.data.keyword.Bluemix_notm}} Open Service Broker API documentation | Review the criteria that the broker must meet. The {{site.data.keyword.Bluemix_notm}} Open Service Broker extends the Open Service Broker 2.12 specification. For more information, see [Open Service Broker API](https://cloud.ibm.com/apidocs/resource-controller/ibm-cloud-osb-api).| Documentation  |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Develop your service broker |  Use your development environment and {{site.data.keyword.cloud_notm}} resources to develop your broker. | Development environment and documentation |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Host your Open Service Broker | The hosted location of the service broker must follow Transport Layer Security (TLS) protocol version 1.2. The service broker must be hosted as part of an app that can respond to REST API calls, and it must meet {{site.data.keyword.Bluemix_notm}} security guidelines. |  Development environment and documentation |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Test your hosted Open Service Broker |  Validate each of the API endpoints your service broker supports by running curl commands against your hosted service broker. Validate your service broker by running curl commands against the different endpoints you’re enabling. | Development environment and documentation |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Set up {{site.data.keyword.Bluemix_notm}} SSO and redirect URLs | You can enable single sign-on and add redirect URLs that can handle authentication and authorization. | {{site.data.keyword.Bluemix_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Add your broker | Add your broker to your product and link it to your pricing plans. | {{site.data.keyword.Bluemix_notm}} console |
{: caption="Table 4. Developing your broker" caption-side="top"}

For more information, see the following links:

* [Developing, hosting, and testing your service brokers](/docs/sell?topic=sell-broker-dev-host&interface=ui)
* [Onboard a broker](/docs/sell?topic=sell-broker-onboard&interface=ui)


## Publishing and testing your service
{: #pubtest}

| Task | Description | Environment |
|------|-------------|-------------|
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Verify that all tasks are completed | Confirm that you completed the getting started tasks, defined your service details, and added your broker. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Request to publish your service | Submit a request for {{site.data.keyword.cloud_notm}} to review your product details and approve it's ready for publishing. | {{site.data.keyword.cloud_notm}} console |
| ![Checkbox icon](../icons/checkbox-icon.svg "Checkbox") Publish your service | After your publishing request is approved, publish your service to the {{site.data.keyword.cloud_notm}} catalog. | {{site.data.keyword.cloud_notm}} console |
{: caption="Table 5. Tasks for publishing services" caption-side="top"} 

For more information, see the following links:

* [Publishing your service](/docs/sell?topic=sell-service-publish)
* [Publish your service to the IBM Cloud catalog](/docs/sell?topic=sell-svc-publish)

As a third-party provider, you're responsible for maintaining all assets of published services in the {{site.data.keyword.cloud_notm}} catalog and deprecating outdated versions.  
{: note}
