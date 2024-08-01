---

copyright:
  years: 2021, 2024
lastupdated: "2024-08-01"

keywords: HA, DR, high availability for Partner Center, disaster recovery for Partner Center, failover for Partner Center

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Understanding high availability and disaster recovery for {{site.data.keyword.cloud_notm}} Partner Center
{: #ha-dr}

{{site.data.keyword.cloud}} provides a service for hosting Partner Center. Partner Center follows the practices that are described in [How {{site.data.keyword.cloud_notm}} ensures high availability and disaster recovery](/docs/overview?topic=overview-zero-downtime).
{: shortdesc}

This service is hosted in the Dallas (`us-south`), Frankfurt (`eu-de`), and Sydney (`au-syd`) regions, which are collectively served by a global endpoint. Partner Center data is stored in a US cross-regional DB2 on Cloud high availability instance. If the service in one region fails, Partner Center is still operational as traffic is routed automatically to the other available regions. When the service in the failed region recovers, it starts receiving traffic again without any action required from users.
