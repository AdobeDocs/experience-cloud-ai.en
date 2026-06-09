---
title: Adobe Experience Platform tools in CX Enterprise MCP
description: Learn which Adobe Experience Platform tools are available through CX Enterprise MCP.
---

# Adobe Experience Platform tools in Adobe CX Enterprise MCP {#aep-mcp}

You can use the Adobe Experience Platform product tools to inspect schemas, datasets, data governance configuration, Query Service resources, and audit events from an MCP-compatible client. These tools are available through the [Adobe CX Enterprise MCP](overview.md) when your organization is enabled and your user account has the required Experience Platform permissions.

>[!AVAILABILITY]
>
>The Experience Platform product tool is in Beta. Access is by invitation only and requires Adobe organization enablement. See [Access CX Enterprise MCP tools](access.md).

## Key capabilities {#mcp-capabilities}

Experience Platform tools provide a read-only monitoring and triage surface. You can:

- Inspect XDM schemas, classes, field groups, data types, descriptors, and union schemas.
- Explore relationships between datasets, schemas, identities, profiles, and audiences.
- Review dataset metadata, ingestion batches, data lake metrics, and failed ingestion files.
- Inspect data usage labels, governance policies, and marketing actions.
- Review Query Service queries, saved templates, scheduled queries, alert subscriptions, and connection parameters.
- Search audit events across Experience Platform.

>[!IMPORTANT]
>
>All Experience Platform tools in the current Beta are read-only. Creating, updating, or deleting schemas, datasets, policies, queries, or sandboxes is not supported. Tools that would expose record-level data, such as dataset previews and dataset file downloads, are intentionally disabled.

## Available tools {#mcp-tools}

| Area | Tool | Description |
| --- | --- | --- |
| Schemas | `search_schema_registry` | List and retrieve XDM schemas, field groups, classes, data types, descriptors, behaviors, union schemas, registry statistics, and audit logs. |
| Schemas | `search_class_relations` | Explore how Experience Platform business entities, such as datasets, schemas, identities, profiles, and audiences, relate to one another. |
| Datasets and data lake | `search_datasets` | List and inspect datasets and data ingestion batches, including batch status, metrics, and file listings. |
| Datasets and data lake | `search_data_lake` | Retrieve data lake dataset metadata, storage and ingestion size metrics, and failed batches within a time window. |
| Datasets and data lake | `search_data_access` | List the files belonging to a failed ingestion batch to diagnose ingestion failures. |
| Data governance | `search_dule` | List and retrieve data usage labels, governance policies, and marketing actions, and evaluate whether a marketing action on labeled data would violate a policy. |
| Query Service | `search_query_service` | List and inspect Query Service queries, saved templates, scheduled queries and their runs, alert subscriptions, and interactive Postgres connection parameters. |
| Query Service | `search_allowed_ip_ranges` | Retrieve the allowed IP ranges configured for Query Service in the current sandbox. This tool requires the Data Distiller add-on. |
| Audit | `search_audit` | List audit events across Experience Platform, filterable by action, asset type, status, and time range. |

## Example prompts {#mcp-use-cases}

| Goal | Example prompt |
| --- | --- |
| Browse schemas | "List the schemas enabled for Real-Time Customer Profile in the `prod` sandbox." |
| Inspect a schema | "Show me the full definition for the schema titled `Loyalty Members`." |
| Understand entity relationships | "How do datasets, identities, and profiles relate to each other?" |
| List datasets | "List my datasets and show which are enabled for Profile." |
| Inspect ingestion batches | "Show me the 5 most recent ingestion batches and flag failures." |
| Diagnose a failed batch | "List the files from failed batch `batch789` so I can see what broke." |
| Review labels and policies | "List our custom data usage labels, marketing actions, and policies." |
| Evaluate a marketing action | "Would exporting data labeled `C1` to a third party violate any policy?" |
| Find expensive queries | "Show me the top 5 longest-running queries in the past 24 hours." |
| Review scheduled queries | "List my scheduled queries and flag any that are quarantined." |
| Trace asset changes | "What actions were performed on dataset ID `abc123` in the past 7 days?" |

## Permissions {#mcp-context}

Your Adobe organization and sandbox context are established once at the MCP connection level and apply to every product tool, so you do not switch organizations or sandboxes from the Experience Platform tools. To set that context for a session, see [Product context for tool calls](install.md#mcp-connect-params).

Your user account must have permission to view the Experience Platform resources you query. The MCP does not bypass product permissions.

## Known limitations {#mcp-limitations}

| Limitation | Description | Workaround |
| --- | --- | --- |
| Read-only surface | Experience Platform tools only expose retrieve APIs. You cannot create, update, or delete schemas, datasets, policies, queries, or sandboxes. | Use the Experience Platform UI or Experience Platform APIs for write operations. |
| No record-level data | Tools that would return customer records, such as dataset file downloads and dataset previews, are disabled. | Use the Data Access API or Query Service directly when you need record-level data. |
| Audit retention window | `search_audit` returns at most the last 1000 records, and audit events are retained for the last 90 days. | Narrow the query with asset type, action, status, and an explicit time range. |
| Allowed IP ranges require Data Distiller | `search_allowed_ip_ranges` is only available to organizations that have purchased the [!DNL Data Distiller] add-on. | Confirm your organization's entitlement. Without it, the tool returns no data. |
| Pagination on list operations | List tools return paginated results. Full enumeration across very large sandboxes requires chaining paging parameters. | Narrow queries using filters such as name, state, or time range. |