---
title: Real-Time CDP MCP (Beta)
description: Learn how to connect Adobe Real-Time CDP to MCP clients using the MCP server.
---
# Real-Time CDP tools in CX Coworker Gateway {#rtcdp-mcp}

You can use the Real-Time CDP MCP product tools to inspect audiences, destinations, sources, identity namespaces, and activation health from an MCP-compatible client. These tools are available through the unified [CX Coworker Gateway gateway](overview.md) when your organization is enabled and your user account has the required Real-Time CDP permissions.

>[!AVAILABILITY]
>
>The Real-Time CDP product tool is in Beta. Access is by invitation only and requires Adobe organization enablement. See [Access CX Coworker Gateway tools](access.md).

## Key capabilities {#mcp-capabilities}

Real-Time CDP tools provide a read-only monitoring and triage surface. You can:

* List and inspect audiences, including lifecycle state, origin, and identity namespace.
* Review audience evaluation and export jobs to identify recent failures.
* Inspect configured destination accounts, destination flows, and activation run history.
* Inspect source connectors, accounts, flows, and ingestion run history.
* List identity namespaces and merge policies.

>[!IMPORTANT]
>
>All Real-Time CDP tools in the current Beta are read-only. Creating, updating, activating, or deleting audiences, destinations, sources, or dataflows is not supported.

## Available tools {#mcp-tools}

| Area | Tool | Description |
| --- | --- | --- |
| Audiences | `search_audiences` | List and look up audiences by name, entity type, lifecycle state, identity namespace, or origin. |
| Audiences | `preview_audience_membership` | Estimate the size of a PQL or SDD segment expression before saving it as an audience. |
| Audiences | `inspect_audience_evaluation_jobs` | Retrieve segment evaluation job records to diagnose audience refresh issues or confirm recent evaluation history. |
| Audiences | `inspect_audience_export_jobs` | Retrieve audience export job records to confirm exports completed or surface failure details. |
| Destinations | `search_destination_connectors` | List destination connector types available in the platform. |
| Destinations | `search_destination_accounts` | List authenticated destination accounts. |
| Destinations | `search_destination_input_connections` | Retrieve the Experience Platform-side input of a destination flow. |
| Destinations | `search_destination_output_connections` | Retrieve the external endpoint of a destination flow, including target path, file format, and delivery configuration. |
| Destinations | `search_destination_flows` | List and inspect configured destination activation flows, including state, mappings, and schedule. |
| Destinations and sources | `inspect_flow_runs` | Retrieve source and destination flow execution history, including status, timing, record counts, and failure details. |
| Sources | `search_source_connectors` | List source connector types available in the platform. |
| Sources | `search_source_accounts` | List authenticated source accounts. |
| Sources | `search_source_input_connections` | Retrieve what a source flow pulls from an account. |
| Sources | `search_source_output_connections` | Retrieve the Experience Platform dataset destination for a source flow. |
| Sources | `search_source_flows` | List and inspect configured source ingestion pipelines, including state, mappings, and schedule. |
| Identity | `search_identity_namespaces` | List identity namespace definitions in your sandbox. |
| Identity | `search_merge_policies` | List merge policy records that control how Real-Time Customer Profiles are assembled. |

## Example prompts {#mcp-use-cases}

| Goal | Example prompt |
| --- | --- |
| List audiences | "List my audiences in the `prod` sandbox." |
| Inspect an audience | "Show me the details and lifecycle state for audience ID `abc123`." |
| Diagnose evaluation issues | "Show me the most recent audience evaluation jobs and flag failures." |
| Check export jobs | "List recent audience export jobs and show me the status of each." |
| Estimate audience size | "Estimate the size of this PQL expression before I save it: `homeAddress.country = 'US'`." |
| Review destination setup | "List my destination activation flows and show which are enabled or disabled." |
| Investigate a failed activation run | "Show me the run history for flow ID `xyz789` and summarize any errors." |
| Review source ingestion | "Show me recent run history for source flow ID `src456` and flag failures." |
| Inspect identity configuration | "What identity namespaces are configured in my sandbox?" |

## Permissions {#mcp-context}

Your Adobe organization and sandbox context are established once at the gateway connection level and apply to every tool family, so you do not switch organizations or sandboxes from the Real-Time CDP tools. To set that context for a session, see [Product context for tool calls](install.md#mcp-connect-params).

Your user account must have permission to view the Real-Time CDP resources you query. The gateway does not bypass product permissions.

## Known limitations {#mcp-limitations}

| Limitation | Description | Workaround |
| --- | --- | --- |
| Read-only surface | Real-Time CDP tools only expose retrieve APIs. You cannot create, update, activate, or delete audiences, destinations, sources, or dataflows. | Use the Real-Time CDP UI or Experience Platform APIs for write operations. |
| No engagement or delivery metrics | Tools do not return downstream delivery stats, engagement, or conversion metrics from destination platforms. | Use the destination platform's reporting, Customer Journey Analytics tools, or Adobe Analytics tools for engagement and conversion data. |
| Segment query must be authored externally | `preview_audience_membership` requires a valid PQL or SDD expression. The tool does not compose the query for you. | Author the expression in Segment Builder or the Segmentation Service API, then paste it into your prompt. |
| Pagination via continuation tokens | List tools return paginated results. Full enumeration across very large sandboxes requires chaining continuation tokens. | Narrow queries using filters such as name, state, connection spec, or time range. |
| Activation run filtering is time-based only | Activation run inspection supports filtering by status and completion timestamp, but not by error type or destination platform directly. | Filter by `flowId` first to scope runs to a specific destination flow. |

