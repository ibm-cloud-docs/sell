---

copyright:

  years: 2018, 2022

lastupdated: "2022-04-26"

keywords: test criteria, IBM Cloud catalog, Add broker Click Manage

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}


# Publishing and testing your service
{: #step5-pubtest}

All new services must be [onboarded through Partner Center](/docs/sell?topic=sell-get-started). All existing products will be migrated to the new management tool called Partner Center Sell by 31 May 2022. Refrain from making changes to your records during this time. As part of the migration, all of your data will be retained, and when the migration is complete we will notify you by email about how you can review and validate your record.
{: important}

Now that you have your hosted broker or brokers that meet the OSB specification, you can return to the resource management console to publish your service to the {{site.data.keyword.Bluemix_notm}} catalog. 
{: shortdesc}

## Before you begin
{: #service-pre-reqs}

This step assumes that you're approved to deliver your third-party service. If you didn't complete the initial registration and approval in Onboarding Workbench, see the [Getting started tutorial](/docs/sell/index.md?topic=sell-get-started#get-started).
{: tip}

Ensure that you start step 1 and completed steps 2, 3, and 4:
1. [Author service docs and marketing announcement](/docs/sell?topic=sell-content-tasks#content-tasks).
2. [Define your service in the resource management console](/docs/sell?topic=sell-step2-define#step2-define).
3. [Develop and host your service brokers](/docs/sell?topic=sell-step3-osb#step3-osb).
4. [Develop an authentication flow](/docs/sell?topic=sell-step4-iam#step4-iam).

## Publish your service to {{site.data.keyword.Bluemix_notm}}
{: #publish}

1. From the resource management console, go to the Deployments page.
2. Click the **Brokers** tab, and click **Add broker**.
3. Click **Manage** to open the Service Broker Configuration page.
4. Add your hosted broker, and click **Register broker**.
5. After successfully registering switch to the **Catalog Deployments** tab.
6. Click **Add Deployment** and select the plan and the broker you want to deploy.
7. Select the region and data center where you want to deploy your service to and click **Add**.
8. From the Deployments page, review your unpublished deployment and click **Publish**.
9. From the Publish to the Catalog page, review the details of your deployment, and click **Publish**.

Stuck on a deployment failure? Contact your {{site.data.keyword.Bluemix_notm}} representative for help.
{: tip}

## Test your deployed service 
{: #publish-test}

Because you deployed in limited visibility mode, only you can see your service in the {{site.data.keyword.Bluemix_notm}} catalog. By using the checklist in the following section, log in to {{site.data.keyword.Bluemix_notm}} and work through the test criteria.

1. Log in to [{{site.data.keyword.Bluemix_notm}}](https://cloud.ibm.com){: external} with your IBMid.
2. Ensure that you are in the correct account (the same account you used to create the service).
3. Click **Catalog** in the menu bar, and search for your service.
4. Next, use the checklist in the following section to validate your service.

### Checklist - Test your service
{: #test-your-service}

1. Validate authentication from the service instance dashboard.
2. Catalog displays correctly (Import from broker shows correctly in the resource management console).
3. Provision works - you can create a service instance in plan of choice.
4. Deprovision works - you can delete a service instance.
5. Bind works - you can click **Connections** and connect your service to another application.
6. Unbind works - you can disconnect your service and delete the connection.
7. Create service Key / Delete service Key - you can click **Credentials** and generate a service key, and then delete that service key.
8. Test `plan_changeable` if you support multiple plans. If you enable this by setting Yes, you need to extend your Open Service Broker to support plan changes for provisioned instances. If your offering supports multiple plans, and you want users to change plans for a provisioned instance, you need to enable the ability for users to update their service instance. For more details, see the /v2/service_instances/{instance_id} PATCH endpoint in the Open Service Broker API v2.12  - Patch - display that user can change plan on provisioned instance. To test, switch the plan on an existing provisioned service instance.
9. The OSB specification doesn't support a disabled instance state, but not yet deleted instance state. In order for IBM Cloud to support customers that might experience a billing lapse or other situations that result in an account suspension (but not yet cancellation), IBM Cloud defines extended API endpoints that allow service instances to be disabled and re-enabled. The following endpoint extensions are **REQUIRED**. Work with your IBM representative and have them test your enable and disable endpoints:
   - enable and disable instances (GET): status - returns the state of your service instance.
   - enable and disable instances (PUT): Allows you to enable or disable a service instance.
10. Test usage submission if you support metered plans. For any plans with metered usage you must validate the following:
   - You can curl the usage API and correctly return accurate pricing based on usage.
   - You can demonstrate that you have enabled automated hourly submission to usage, supporting all users who provision an instance of your service.

If your tests are unsuccessful, repeat the previous steps to publish your service and test again, iterating until you're successful.


## Next steps
{: #release}

Now that you have a functional service in the catalog, you can build a demo and ask for approval to publicly release your service. See [Step 6: Publicly release your service](/docs/sell?topic=sell-public-releasing#public-releasing).
