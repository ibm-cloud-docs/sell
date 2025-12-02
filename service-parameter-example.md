---

copyright:

  years: 2019, 2024

lastupdated: "2025-12-02"

keywords: service parameter definition, parameters, parameter example,

subcollection: sell
---

{{site.data.keyword.attribute-definition-list}}

# Service parameter definitions and examples
{: #service_parameters_def_examples}

Service parameters are used to collect and add additional data points to a call when an IBM Cloud customer creates a service instance. The following sections provide examples and definitions of how service parameters can be used. To start adding custom service parameters for your product, see [Adding custom service parameters for your service](/docs/sell?topic=sell-service-add-custom-parameters).

## Service parameter examples
{: #service_parameters_examples}

The following example illustrates how to specify a custom service parameter for a required text field.

Inside the surrounding `metadata` and `service` JSON structures, the `parameters` key identifies a JSON array of custom service parameters. In this example, the array contains only one custom parameter, which has the identifier `subscription_id`. It is a required text field with the label "Subscription ID" and the description "Subscription ID that will be used when provisioning the service instance". This custom parameter will be displayed in the UI whenever the user selects either of the two associated price plans, '068f8a20-8b27-4049-91fe-a3ff5f505352' or '45333bd7-79f5-475f-9b14-9fe99734592a':

```json
{
  "metadata": {
    //...
    "service": {
      //...
      "parameters": [{
          "associations": {
              "plan": {
                  "showFor": [
                      "068f8a20-8b27-4049-91fe-a3ff5f505352",
                      "45333bd7-79f5-475f-9b14-9fe99734592a"
                  ]
              }
          },
          "description": "Subscription ID that will be used when provisioning the service instance",
          "displayname": "Subscription ID",
          "name": "subscription_id",
          "required": true,
          "type": "text"
      }]
  }
}
```

This custom parameter must be added not only to the **Service** object but also to all the **Deployment** objects for the two service plans that the parameter is associated with. Also the deployments for the deployment objects must be updated to process the custom parameter.

Always test your parameter in the {{site.data.keyword.cloud_notm}} console to verify that the changes that you specified work correctly.
{: important}

## Service parameter definitions
{: #service_parameters_definitions}

The `parameters` structure defines a JSON array of custom service parameters. When a service instance is created, it uses the information in the array to manage the custom service parameters. For an example, see the preceding subtopic in this topic.

Each custom service parameter in the `parameters` structure has the following layout. Many of the attributes are optional:

`parameters.name`
:   The key of the parameter.

`parameters.displayname`
:   The name of the parameter that is displayed.

`parameters.type`
:   The type of put field that is displayed by the {{site.data.keyword.cloud_notm}} user interface. The value can be `text`, `password`, `dropdown`, `check box`, or `radio`.

This value is required.
{: note}

The following codeblock shows examples for the `name`, `displayname`, and `type` parameters:

```json
{
  "name": "pwd",
  "displayname": "Password",
  "type": "password"
}
```

`parameters.options`
:   A JSON structure to specify available values for the `dropdown`, `check box`, and `radio` input types.

`parameters.options.displayname`
:   The name of the dropdown, check box, or radio button that you want to display in the UI.

`parameters.options.value`
:   The value of the parameter to be sent to the service broker when creating the service.

```json
{
  "options": [
    {
      "displayname": "HDFS",
      "value": "hdfs"
    },
    {
      "displayname": "YARN",
      "value": "yarn"
    },
  ]
}
```

`parameters.value`
:   The default value of the parameter. For check box input type, it can be an array of values.

```json
{
  ["hfs","yarn"]
}
```

`parameters.layout`
:   Specifies the layout of check box or radio input types. When unspecified, the default layout is horizontal.

`parameters.associations`
:   A JSON structure to describe the interactions with price plans and/or other custom parameters.

This value is optional, and all subsequent values that are appended to `parameters.associations.<value>` are optional.
{: note}

```json
{
  "type": "text",
  "associations": {
    "plan": {
    "showFor": ["apsMyserviceParametersDemo-entry","apsMyserviceParametersDemo-enterprise"]
    }
  }
}
```

`parameters.associations.plan`
:   A JSON structure to describe the interaction with price plans.

`parameters.associations.plan.showFor`
:   An array of price plan IDs. If specified, the parameter is shown in the UI when the corresponding price plan is selected.

`parameters.associations.plan.optionsRefresh`
:   When specified, the `optionsUrl` is called when the associated price plan is selected.

`parameters.associations.parameters`
:   An array of JSON describing the interaction with other custom parameters.

`parameters.associations.parameters.name`
:   The name of the other custom parameter that you want to interact with.

Required when `parameters.associations.parameters` is in use.
{: note}

`parameters.associations.parameters.showFor`
:   An array of selected values that are associated with the custom parameter that you want to interact with. This parameter shows in the UI when one of those values is selected.

`parameters.associations.parameters.optionsRefresh`
:   When this parameter is set to true, the `optionsUrl` is called when the associated parameter value is changed and this parameter is visible in the UI.

`parameters.optionsUrl`
:   The API that is called by the console to get a list of options for dropdown, check box, or radio input type. The response is a JSON structure that contains two fields:

`parameters.optionsUrl.options`
:   An array of JSON that will return `parameters.options`; for more details see the entry for `parameters.options`.

`parameters.optionsUrl.value`
:   The new default value of the parameter. For more details, see the entry for `parameters.value`.

The console passes the `ace_config` query parameter, which contains the current org GUID, space GUID, the current value of all custom parameters, and the current price plan ID. The bearer token is propagated in the header.

`parameters.invalidmessage`
:   The message that appears when the content of the text box is invalid.

`parameters.description`
:   The description of the parameter that is displayed to help users with the value of the parameter.

`parameters.required`
:   A Boolean value that indicates whether the parameter must be entered in the {{site.data.keyword.cloud_notm}} user interface.

`parameters.pattern`
:   A regular expression that the value is checked against.

`parameters.placeholder`
:   A short hint that describes the expected value.

`parameters.readonly`
:   A Boolean value that indicates whether the value of the parameter is displayed only and cannot be changed by users. The default value is false.

`parameters.hidden`
:   A Boolean value that indicates whether the key-value pair is hidden from users. The default value is false.
