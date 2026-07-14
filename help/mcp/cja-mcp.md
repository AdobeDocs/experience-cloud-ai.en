---
title: Customer Journey Analytics tools in Adobe CX Coworker Gateway
description: Learn which Adobe Customer Journey Analytics tools are available through Adobe CX Coworker Gateway.
---

# Customer Journey Analytics tools in Adobe CX Coworker Gateway {#cja-mcp}

Use the Customer Journey Analytics product tools explore data views, discover dimensions and metrics, run reports, and manage selected analytics components from an MCP-compatible client. These tools are available through the [CX Coworker Gateway](overview.md) when your account has the required Customer Journey Analytics license and permissions.

>[!AVAILABILITY]
>
>Customer Journey Analytics tools are available to customers with a Customer Journey Analytics license. Access is controlled by the **MCP Access** permission in Adobe Admin Console. See [Access CX Coworker Gateway tools](access.md).

## Key capabilities {#mcp-capabilities}

Customer Journey Analytics tools support governed analytics workflows from your MCP client. You can:

* Discover data views and inspect how they are configured.
* Find dimensions, metrics, calculated metrics, segments, date ranges, audiences, and projects.
* Run ranked and trended reports with dimensions, metrics, date ranges, and segment filters.
* Inspect component definitions and component usage.
* Create or update selected analytics components and workspace projects.

>[!IMPORTANT]
>
>Unlike the read-only [Real-Time CDP](rtcdp-mcp.md), [Experience Platform](aep-mcp.md), and [Journey Optimizer](ajo-mcp.md) product tools, Customer Journey Analytics tools include write operations. They can create and update segments, calculated metrics, date ranges, projects, and audiences. Review and validate all MCP-initiated changes before relying on them.

## Available tools {#mcp-tools}

| Area | Tool | Description |
| --- | --- | --- |
| Setup and guides | `describeCja` | Returns reference guides for tools, dimensions, metrics, segments, calculated metrics, and project structures. |
| Setup and guides | `setDefaultSessionDataViewId` | Configures the session-level default data view for subsequent tool calls. |
| Discovery | `findDimensions` | Locates available dimensions, with semantic search support. |
| Discovery | `findMetrics` | Discovers standard and custom metrics, excluding calculated metrics. |
| Discovery | `findCalculatedMetrics` | Browses user-created and shared calculated metrics. |
| Discovery | `findSegments` | Lists segments accessible to the current user. |
| Discovery | `findDateRanges` | Retrieves saved date range components. |
| Discovery | `findDataViews` | Discovers available data views. |
| Discovery | `findProjects` | Locates workspace projects. |
| Discovery | `findAudiences` | Lists available audience components. |
| Reporting and analysis | `runReport` | Executes ranked reports with dimensions, metrics, date ranges, and optional segment filters. |
| Reporting and analysis | `searchDimensionItems` | Retrieves dimension values needed for breakdown reports. |
| Component details | `describeDimension` | Shows detailed metadata for a specific dimension. |
| Component details | `describeMetric` | Returns metric metadata and measurement details. |
| Component details | `describeSegment` | Displays a segment's definition and compatibility information. |
| Component details | `describeCalculatedMetric` | Shows the formula and base metrics used. |
| Component details | `describeProject` | Details a workspace project's configuration. |
| Component details | `describeAudience` | Returns audience metadata and publishing status. |
| Component usage | `listComponentUsage` | Ranks components by usage frequency. |
| Component usage | `listFrequentlyUsedWith` | Identifies components commonly paired together. |
| Component usage | `listSimilarTo` | Finds alternative components serving similar purposes. |
| Create and update | `upsertSegment` | Creates a new segment or modifies an existing one. |
| Create and update | `upsertCalculatedMetric` | Creates a new calculated metric or modifies an existing one. |
| Create and update | `createDateRange` | Creates a reusable date range component. |
| Create and update | `upsertProject` | Creates a new workspace project or modifies an existing one. |
| Create and update | `upsertAudience` | Creates a new audience definition or modifies an existing one. |

## Example prompts {#mcp-use-cases}

| Goal | Example prompt |
| --- | --- |
| List data views | "List the data views available to me in Customer Journey Analytics." |
| Discover components | "Find metrics related to revenue in data view `[data view name]`." |
| Run a report | "Run a trended report of orders by month for the last quarter." |
| Break down a metric | "Show me the top 10 marketing channels by visits, broken down by device type." |
| Inspect a component | "Describe the segment `[segment name]` and show me its definition." |
| Audit usage | "Which dimensions are used most frequently across my projects?" |
| Create a segment | "Create a segment for users who viewed the pricing page in the last 30 days." |

## Product context and permissions {#mcp-context}

Your account must belong to a Customer Journey Analytics product profile that includes the **MCP Access** permission item, granted by a system or product administrator in Adobe Admin Console.

Product permissions still apply. Your account must be able to view the data views, components, projects, and audiences you query, and must have the appropriate product permissions for write operations such as creating or updating segments, calculated metrics, date ranges, projects, or audiences.

## Watch it in action {#mcp-videos}

**Overview**

>[!VIDEO](https://video.tv.adobe.com/v/3486313/?learn=on&enablevpops)

**In action**

>[!VIDEO](https://video.tv.adobe.com/v/3486314/?learn=on&enablevpops)

## More information {#mcp-more}

For the complete tool reference and getting-started guide, see the [Customer Journey Analytics MCP documentation](https://developer.adobe.com/analytics-mcp/docs/cja/){target="_blank"}.