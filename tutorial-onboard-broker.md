---

copyright:
  years: 2021

lastupdated: "2021-10-12"


keywords: third-party, sell on IBM Cloud, partner center, service, broker, pricing plan, regions, location

subcollection: sell

content-type: tutorial
account-plan: paid
completion-time: 10m 

---

{:shortdesc: .shortdesc}
{:screen: .screen}  
{:codeblock: .codeblock}  
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:beta: .beta}
{:external: target="_blank" .external}
{:step: data-tutorial-type='step'} 


# Onboarding a broker
{: #broker-onboard}
{: toc-content-type="tutorial"}
{: toc-completion-time="10m"} 

This tutorial walks you through how to onboard a broker that you use to connect a pricing plan to your third-party service. When users create instances of your service from the {{site.data.keyword.cloud}} catalog, the broker manages the lifecycle of those instances, and connects the service to the applications that developers are building.
{: shortdesc}

The process to sell third-party products in Partner Center is still under development. With the current release, you can offer your product for free. If you're interested in trying it out, contact us at cloud.onboarding@us.ibm.com.
{: beta}

This tutorial is one of four in a series that demonstrates how to onboard and publish a third-party service to {{site.data.keyword.cloud_notm}}. As you complete the tutorial, adapt each step to fit your product's needs.

## Before you begin
{: #broker-onboard-prereqs}

For an example of how to build your broker, see [IBM Cloud reference broker](https://github.com/IBM-Cloud/onboarding-osb). 

Make sure you have the following API keys:
* An onboarding API key for access to the Global Catalog API.
* An {{site.data.keyword.cloud_notm}} API key for access to your deployment target.

For more information, see [Managing API keys](/docs/account?topic=account-userapikey).

## Configure your broker
{: #broker-onboard-cfg}
{: step}

1. Click **Menu** > **Partner Center** > **My Products**, and select your service from the table. 
2. From the Brokers tab, click **Add broker**. 
3. Enter the name, URL, username, and password for your broker, and click **Done**. 

## Next steps
{: #broker-onboard-next}

Link your broker to the pricing plan for your service. 
