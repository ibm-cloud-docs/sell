---

copyright:

  years: 2022, 2023

lastupdated: "2023-02-24"

keywords: IBM Cloud, selling services, metrics, submit evidence, testing metrics, metering

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Adding metrics to your service
{: #service-add-metrics}

With {{site.data.keyword.cloud}} Partner Center, you can measure various metrics for services with usage-based pricing plans. You can measure metrics on created instances and submit those measures to the metering service. The rating service aggregates the submitted usage into different buckets (instance, resource group, and account) based on the model that you choose. The aggregation and rating models for all the metrics in a plan are contained in the metering and rating definition documents for the plan. For more information, see [Metering integration](/docs/sell?topic=sell-service-metering-integration).

To onboard your service to {{site.data.keyword.cloud_notm}}, you are required to add metrics to your usage-based pricing plan to determine how customers are charged. When you add metrics to your pricing plan in Partner Center, you must request an initial approval. After your metrics are approved, you can test the pricing and usage from a customer's perspective and provide evidence from your testing to get the final approval for your pricing plan.
{: shortdesc}

## Before you begin
{: #metrics-prereq}

Before you can add metrics to your pricing plan, you must complete the following tasks:

1. [Submit tax and Electronic Funds Transfer documentation](/docs/sell?topic=sell-service-pricing-info#submit-tax-eft)
2. [Export the Control Classification Number (ECCN)](/docs/sell?topic=sell-service-pricing-info#service-eccn)
3. [Enter the United Nations Standard Products and Services Code (UNSPSC)](/docs/sell?topic=sell-service-pricing-info#service-unspsc)
4. [Add a paid pricing plan](/docs/sell?topic=sell-service-pricing-info#add-plan-paid)
5. [Confirm the digital platform reseller agreement](/docs/sell?topic=sell-service-pricing-info#dra)

## Adding metrics to your pricing plan
{: #add-metrics-plan}

If you offer a paid integrated product and add a paid pricing plan that requires customers to pay for their usage, you must add metrics to your pricing plan to aggregate your product's usage. After you add metrics to your plan, you must request an initial metering approval, so you can submit your resource usage and start reviewing your metrics.

To add metrics to your pricing plan, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Sell** > **My products**.
1. Select the product that you're onboarding, and click **Pricing**.
1. Select a usage-based plan from the table and click **Add metrics**.
1. In the Usage metrics section, click **Add metrics**.
1. Complete the required fields.
1. Click **Done**.
1. To submit your pricing plan and metering for review, click **Request approval** in the Metering approval section.

## Submitting resource usage to the {{site.data.keyword.cloud_notm}} Usage Metering API
{: #submit-usage}

To review how customers understand and experience your pricing plan, and validate that your metered plans are correctly configured, you must submit your resource usage. Submitting your resource usage includes creating your metering JSON, calling the Usage Metering API, and providing the evidence of your testing.

### Creating your metering JSON
{: #create-metering-json}

To submit your resource usage, you must develop a JSON file with your metering information. After you develop your metering JSON, you can submit your resource usage by calling the Usage Metering API. There are specific fields that you must include in the request body of your JSON file to make sure it contains all your metering information. For more information on the required fields and submitting usage records, see the [Usage Metering API](/apidocs/usage-metering#report-resource-usage){: external}.

To create the JSON that contains all your metering information, you must include the following fields in the request body:

```text
resource_instance_id
plan_id
start
end
measured_usage
```
{: codeblock}

See the following JSON example that includes the required fields:

```json
[
  {
    "start": 1485907200001,
    "end": 1485910800000,
    "region": "us-south",
    "resource_instance_id": "crn:v1:bluemix:staging:database-service:us-south:a/1c8ae972c35e470d994b6faff9494ce1:793ff3d3-9fe3-4329-9ea0-404703a3c371::",
    "plan_id": "da40662d-2f72-4a19-8c79-8c77cf285e17",
    "measured_usage": [
      {
        "measure": "QUERIES",
        "quantity": 100
      },
      {
        "measure": "STORAGE",
        "quantity": 123.456
      }
    ]
  },
  {
    "start": 1485910800000,
    "end": 1485910800000,
    "resource_instance_id": "ed20abbe-8870-44e6-90f7-56d764c21127",
    "plan_id": "da40662d-2f72-4a19-8c79-8c77cf285e17",
    "measured_usage": [
      {
        "measure": "instances",
        "quantity": {
          "previous": 0,
          "current": 1
        }
      }
    ]
  }
]
```
{: codeblock}

To submit usage for your active service instances, call the [Usage Metering API](/apidocs/usage-metering#report-resource-usage){: external} as shown in the following sample request. To make the API call, your metering approval request must be approved by {{site.data.keyword.cloud_notm}}.

You can find the `resource_id` value, which is the Global catalog ID listed on the Brokers page in Partner Center.
{: tip}

```bash
curl -X POST -H "Authorization: {iam_token}"   -H "Accept: application/json"   -H "Content-Type: application/json"   -d "{REQUEST_BODY}"   "{base_url}/v4/metering/resources/{resource_id}/usage"

```
{: codeblock}
{: curl}

```java
// Report usage for a mythical resource.
// Use zero for quantities since this is only an example.
MeasureAndQuantity lookupMeasure = new MeasureAndQuantity.Builder()
    .measure("LOOKUP")
    .quantity(Long.valueOf(0))
    .build();
MeasureAndQuantity writeMeasure = new MeasureAndQuantity.Builder()
    .measure("WRITE")
    .quantity(Long.valueOf(0))
    .build();
MeasureAndQuantity queryMeasure = new MeasureAndQuantity.Builder()
    .measure("QUERY")
    .quantity(Long.valueOf(0))
    .build();
MeasureAndQuantity gbMeasure = new MeasureAndQuantity.Builder()
    .measure("GIGABYTE")
    .quantity(Long.valueOf(0))
    .build();
List<MeasureAndQuantity> measures = new ArrayList<>();
measures.add(lookupMeasure);
measures.add(writeMeasure);
measures.add(queryMeasure);
measures.add(gbMeasure);

ResourceInstanceUsage resourceInstanceUsageModel = new ResourceInstanceUsage.Builder()
    .resourceInstanceId(resourceInstanceId)
    .planId(planId)
    .region(region)
    .start(startTime)
    .end(endTime)
    .measuredUsage(measures)
    .build();

ReportResourceUsageOptions reportResourceUsageOptions = new ReportResourceUsageOptions.Builder()
    .resourceId(resourceId)
    .resourceUsage(new java.util.ArrayList<ResourceInstanceUsage>(
        java.util.Arrays.asList(resourceInstanceUsageModel)))
    .build();

Response<ResponseAccepted> response = service.reportResourceUsage(reportResourceUsageOptions).execute();
ResponseAccepted responseAccepted = response.getResult();

System.out.println(responseAccepted);
```
{: codeblock}
{: java}

```javascript
// Report usage for a mythical resource.
// Use zero for quantities since this is only an example.
const measures = [{
  measure: 'LOOKUP',
  quantity: 0,
},
{
  measure: 'WRITE',
  quantity: 0,
},
{
  measure: 'QUERY',
  quantity: 0,
},
{
  measure: 'GIGABYTE',
  quantity: 0,
}];

const resourceInstanceUsageModel = {
  resource_instance_id: resourceInstanceId,
  plan_id: planId,
  region: region,
  start: startTime,
  end: endTime,
  measured_usage: measures,
};

const params = {
  resourceId: resourceId,
  resourceUsage: [resourceInstanceUsageModel],
};

usageMeteringService.reportResourceUsage(params)
  .then(res => {
    console.log(JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}


```python
//  Report usage for a mythical resource.
//  Use zero for quantities since this is only an example.
measures = [
  {
    'measure': 'LOOKUP',
    'quantity': 0,
  },
  {
    'measure': 'WRITE',
    'quantity': 0,
  },
  {
    'measure': 'QUERY',
    'quantity': 0,
  },
  {
    'measure': 'GIGABYTE',
    'quantity': 0,
  },
]

resource_instance_usage_model = {
  'resource_instance_id': resource_instance_id,
  'plan_id': plan_id,
  'region': region,
  'start': start_time,
  'end': end_time,
  'measured_usage': measures,
}

response_accepted = usage_metering_service.report_resource_usage(
  resource_id=resource_id,
  resource_usage=[resource_instance_usage_model]).get_result()

print(json.dumps(response_accepted, indent=2))
```
{: codeblock}
{: python}


```go
// Report usage for a mythical resource.
// Use zero for quantities since this is only an example.
resourceInstanceUsageModel := usagemeteringv4.ResourceInstanceUsage{
  ResourceInstanceID: &resourceInstanceID,
  PlanID:             &planID,
  Region:             &region,
  Start:              &startTime,
  End:                &endTime,
  MeasuredUsage: []usagemeteringv4.MeasureAndQuantity{
    usagemeteringv4.MeasureAndQuantity{
      Measure:  core.StringPtr("LOOKUP"),
      Quantity: core.Int64Ptr(0),
    },
    usagemeteringv4.MeasureAndQuantity{
      Measure:  core.StringPtr("WRITE"),
      Quantity: core.Int64Ptr(0),
    },
    usagemeteringv4.MeasureAndQuantity{
      Measure:  core.StringPtr("QUERY"),
      Quantity: core.Int64Ptr(0),
    },
    usagemeteringv4.MeasureAndQuantity{
      Measure:  core.StringPtr("GIGABYTE"),
      Quantity: core.Int64Ptr(0),
    },
  },
}
reportResourceUsageOptions := usageMeteringService.NewReportResourceUsageOptions(
  resourceID,
  []usagemeteringv4.ResourceInstanceUsage{resourceInstanceUsageModel},
)

responseAccepted, response, err := usageMeteringService.ReportResourceUsage(reportResourceUsageOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(responseAccepted, "", "  ")
fmt.Println(string(b))
```
{: codeblock}
{: go}

### Response
{: #metering-api-response}

The response body includes the acceptance status of every usage record. A successful submission returns a response code of `201`. If any other response code is returned, update and resend the data until you receive the `201` code. See the following example of a successful response:

```bash
{
    "resources": [
        {
            "code": "successful_submission",
            "status": 201,
            "message": "Payload was successfully submitted",
            "details": [
                {
                    "field": "data.resource_instance_id",
                    "message": "is required",
                    "value": {
                        "start": 1501282845663,
                        "end": 1501282845664,
                        "region": "us-south",
                        "plan_id": "04082014.ibm.node.default",
                        "measured_usage": [
                            {
                                "measure": "current_running_instances",
                                "quantity": 1
                            },
                            {
                                "measure": "current_instance_memory",
                                "quantity": 1
                            }
                        ]
                    },
                    "type": "object"
                }
            ]
   }
   ```
{: codeblock}

For more information on status codes, see [Response status codes](/apidocs/usage-metering#report-resource-usage-response).

## Review your metrics and provide evidence of your testing
{: #submit-evidence}

After you create the metering JSON, submit the usage records by calling the Usage Metering API, and receive approval from {{site.data.keyword.IBM_notm}}, you can start reviewing and testing how customers understand and experience your pricing plan.

To test and submit evidence for your pricing plan, complete the following steps:

1. Click **Test estimation and metering**.
1. Preview your product in the catalog and generate an estimate by clicking **Add to estimate**.
1. Enter your expected usage, then click **Calculate cost**.
1. Upload evidence of your usage.
     1. Upload a screen capture of the usage data that's generated by the estimator by clicking **Add file**.
     1. Upload a screen capture of your rated usage by clicking **Add file**. To find your rated usage, in the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Billing and usage**  > **Usage**.
     1. Upload a screen capture of the resource usage data JSON that you previously submitted to the {{site.data.keyword.cloud_notm}} Usage Metering API by clicking **Add file**.

    You can upload files in `.jpeg`, `.pdf`, or `.png` file format only.
   {: note}

1. Click **Done**.
