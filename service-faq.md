---

copyright:

  years: 2015, 2025

lastupdated: "2025-12-02"

keywords: IBM Cloud, different metering options, new IBM Cloud Identity, selling products, paid products, payments for third-party products, disbursements, funds, testing

subcollection: sell

content-type: faq

---

{{site.data.keyword.attribute-definition-list}}

# FAQ about selling services
{: #3p-faqs}

FAQ about selling products on {{site.data.keyword.cloud}} might include questions about how and when to receive disbursements, how to view and test a service as a customer, and available metering models. Additional information about selling products on {{site.data.keyword.cloud_notm}} can be found in the Digital Platform Reseller Agreement in {{site.data.keyword.cloud_notm}} Partner Center that must be accepted to offer free and paid products.
{: shortdesc}

To find all FAQs for {{site.data.keyword.cloud_notm}}, see our [FAQ library](/docs/faqs).

## What are the different metering options for plans?
{: #metering}
{: faq}

{{site.data.keyword.cloud}} supports multiple models for aggregating service usage. Service providers measure various metrics on the created instances and submit those measures to the metering service. The rating service aggregates the submitted usage into different buckets (instance, resource group, and account) based on the model that service providers choose. The aggregation and rating models for all the metrics in a plan are contained in the metering and rating definition documents for the plan.

You're required to automate hourly usage submission by using the metering service API if you offer a metered plan.
{: note}

For more information on metering, see [Metering integration](/docs/sell?topic=sell-service-metering-integration). For more information about submitting metered usage, see [Submitting usage for metered plans](/docs/sell?topic=sell-service-add-metrics#submit-usage).

## How do I receive payments for my services?
{: #get-disbursements}
{: faq}

Third-party services that offer paid usage-based pricing plans receive disbursements through an Electronic Funds Transfer (EFT). To set up this method to receive disbursements in {{site.data.keyword.cloud_notm}} Partner Center Sell, you must submit the EFT form when you set up your first usage-based pricing plan. You can download the form from the Payments to me page.

## When are disbursements sent to me?
{: #disbursements-sent}
{: faq}

If any disbursements are due to a third-party provider, they are sent on the last business day of the second calendar month. For example, March activity would be paid on the last calendar day of May, unless the last day of the month falls on a weekend or holiday. In this case, disbursements are sent on the next business day. Disbursements are calculated from beginning of the month to the end of the month.

## What is the fee structure?
{: #fee-structure}
{: faq}

Disbursements are paid against revenue recognized by {{site.data.keyword.IBM}} in a royalty month. {{site.data.keyword.IBM_notm}} pays a third-party provider for each sale of a product as follows:

* As-a-service products: 87% of net revenue
* Software products: 80% of net revenue
* Professional services: 80% of net revenue

## Can a third-party provider run activity reports and payout reconciliations?
{: #third-party-activity-reports}
{: faq}

We are adding features to support reports soon. Disbursements are based on the quantities that you submit to the usage metering service and the price that is defined when you set up your pricing plan in Partner Center. Third-party disbursements are calculated as a percentage of the net revenue for each product that is sold by {{site.data.keyword.IBM_notm}} for a given calendar month. Net revenue is defined as the revenue recognized by {{site.data.keyword.IBM_notm}} or an {{site.data.keyword.IBM_notm}} affiliate calculated using applicable discounts, refunds, returns, offsets, and other adjustments determined in accordance with the current revenue recognition policies of {{site.data.keyword.IBM_notm}} and its affiliates and the controlling accounting principles. For full detail regarding payouts, refer to the Digital Platform Reseller Agreement that must be signed in Partner Center to offer usage-based pricing.

## How can I generate a new {{site.data.keyword.cloud_notm}} Identity and Access Management API Key?
{: #iam-creds}
{: faq}

You're given your API Key when you enable IAM. It is critical that you save the API Key. The value is not shown again. If you lose your API Key, you can delete the key and create a new one. For more information, see [Managing service ID API keys](/docs/account?topic=account-serviceidapikeys).

## How can I view and test my service as a customer?
{: #test-service-user}
{: faq}

Before you publish your service to the catalog, you can test how your customers will see and use it from the {{site.data.keyword.cloud_notm}} catalog. In Partner Center, go to your **Product details**, and click **View catalog entry**. This view enables you to preview your service in the catalog and check that the broker and pricing is working as expected by creating an instance in your account.




## What is {{site.data.keyword.IBM_notm}} Partner Plus?
{: #partnerplus-ibm}
{: faq}

The {{site.data.keyword.IBM_notm}} Partner Plus program offers you a partnership that is built on mutual success and provides you access to competitive incentives, insider programs, and enhanced support.
For more information, see the [{{site.data.keyword.IBM_notm}} Partner Plus](https://www.ibm.com/partnerplus){: external} website.
