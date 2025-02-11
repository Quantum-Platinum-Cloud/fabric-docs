---
title: Differences between Real-Time Analytics and Azure Data Explorer
description: Learn about the differences between Real-Time Analytics and Azure Data Explorer.
ms.reviewer: tzgitlin
ms.author: yaschust
author: YaelSchuster
ms.topic: overview
ms.custom: build-2023, build-2023-dataai, build-2023-fabric
ms.date: 05/23/2023
ms.search.form: product-kusto
---
# What is the difference between Real-Time Analytics and Azure Data Explorer?

[!INCLUDE [preview-note](../includes/preview-note.md)]

Real-Time Analytics is a fully managed big data analytics platform optimized for streaming, and time-series data. It utilizes a query language and engine with exceptional performance for searching structured, semi-structured, and unstructured data. Real-Time Analytics is fully integrated with the entire suite of Fabric products, for both data loading, data transformation, and advanced visualization scenarios.

For more information on Real-Time Analytics, see [What is Real-Time Analytics in Fabric?](overview.md).

Real-Time Analytics is a SaaS offering in the Microsoft Fabric offering. Azure Data Explorer is a PaaS offering in Azure. Real-Time Analytics and Azure Data Explorer share the same core engine with the identical core capabilities, but different management behavior. This article details the difference between the two services. Real-Time Analytics also offers additional capabilities, such as [Eventstreams](event-streams/overview.md).

## Capability support

| Category | Capability| Synapse Real-Time Analytics | Azure Data Explorer |
|----|----|----|----|
| **Security** | VNET | &cross; | Supports VNet Injection and Azure Private Link  |
|  | CMK | &cross; | &check; |
|  | RBAC | &check; | &check; |
| **Business Continuity** | Availability Zones | Yes- dependent on regional zonal availability | Optional |
| **SKU** | Compute options | SaaS platform | 22+ Azure VM SKUs to choose from  |
| **Integrations** | Built-in ingestion pipelines | Event Hubs, Event Grid, [!INCLUDE [product-name](../includes/product-name.md)] Pipeline, [!INCLUDE [product-name](../includes/product-name.md)] Dataflow | Event Hubs, Event Grid, IoT Hub |
|  | OneLake integration | Supports data copying to and from OneLake | &cross; |
|  | Spark integration | Built-in Kusto Spark connector integration with support for Azure Active Directory pass-through authentication, Synapse Workspace MSI, and Service Principal | Azure Data Explorer linked service: Built-in Kusto Spark integration with support for Azure Active Directory pass-through authentication, Synapse Workspace MSI, and Service Principal|
|  | KQL artifacts management | Option to save queries as KQL Querysets that can be shared within the tenant | &cross; |
|  | Database management | &check; |  &check; |
| **Features** | KQL queries | &check; | &check; |
|  | API and SDKs | &check; | &check; |
|  | Connectors | &check; | &check; |
|  | Query tools | &check; | &check; |
|  | Autoscale | &check; (Built-in) | &check; (Optional: manual, optimized, custom) |
|  | Dashboards| &cross; | &check; |
|  | Power BI quick create | &check; | &cross; |
| **Pricing** | Business Model | Included in the Power BI Premium workspace consumption model. Billing per use and dedicated capacity available | Cost plus billing model with multiple meters: Azure Data Explorer IP markup, Compute, Storage, and Networking |

## Next steps

* Get started with [Real-Time Analytics](tutorial-introduction.md)
