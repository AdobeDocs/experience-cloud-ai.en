---
title: Adobe Journey Optimizer tools in CX Enterprise MCP
description: Learn which Adobe Journey Optimizer tools are available through the CX Enterprise MCP.
---
# Adobe Journey Optimizer tools in CX Enterprise MCP {#ajo-mcp}

Use the Adobe Journey Optimizer product tools to inspect campaigns and channel configurations from an MCP-compatible client. These tools are available through the [CX Enterprise MCP](overview.md) when your organization is enabled and your user account has the required Journey Optimizer permissions.

>[!AVAILABILITY]
>
>The Journey Optimizer product tools are in Beta. Access is by invitation only and requires Adobe organization enablement. See [Access CX Enterprise MCP tools](access.md).

## Key capabilities {#mcp-capabilities}

Journey Optimizer tools provide a read-only surface for campaign and channel configuration review. You can:

- List Journey Optimizer campaigns and filter by status.
- Retrieve campaign details, including targeting, schedule, channel, and content configuration metadata.
- List channel configurations for email, SMS, push, and WhatsApp channels.
- Review campaign and channel setup in natural language without navigating product screens.

>[!IMPORTANT]
>
>All Journey Optimizer tools in the current Beta are read-only. Creating, updating, deleting, starting, stopping, or publishing campaigns is not supported.

## Available tools {#mcp-tools}

| Tool | Description |
| --- | --- |
| `ajo_campaign_list` | Browse Journey Optimizer marketing campaigns. Supports filtering by status, such as `DRAFT`, `LIVE`, `STOPPED`, and `COMPLETED`. |
| `ajo_campaign_get` | Fetch details and configuration for a specific campaign by ID, including audience targeting, schedule, channel, and content settings metadata. |
| `ajo_channel_configuration_list`, `ajo_channel_configuration_get` | View surface presets and branding settings for email, SMS, push, or [!DNL WhatsApp] channels. |

## Example prompts {#mcp-use-cases}

| Goal | Example prompt |
| --- | --- |
| Campaign overview | "Show me all my Journey Optimizer campaigns." |
| Status audit | "Which campaigns are currently live?" |
| Campaign details | "Get the full details of campaign `[campaign ID]`." |
| Audience and targeting | "What audience is targeted in campaign `[campaign ID]`?" |
| Schedule and timing | "When is campaign `[campaign ID]` scheduled to run?" |
| Troubleshooting | "Review the setup of campaign `[campaign ID]` and flag possible issues." |
| Channel configuration | "What email channel configurations are available?" |
| Channel audit | "Which channel configurations are missing or incomplete?" |

## Product context and permissions {#mcp-context}

Your user account must have permission to view the Journey Optimizer campaigns and channel configurations you query. The MCP does not bypass product permissions.

If your organization uses multiple sandboxes, specify the sandbox or environment context in your prompt when you need results from a specific sandbox.

## Known limitations {#mcp-limitations}

| Limitation | Description | Workaround |
| --- | --- | --- |
| Read-only surface | Journey Optimizer tools only expose retrieve operations. You cannot create, update, delete, start, stop, or publish campaigns. | Use the Journey Optimizer UI or APIs for write operations. |
| No engagement or performance metrics | Tools do not return reporting data such as impressions, click-through rates, conversions, or delivery stats. | Use Journey Optimizer reporting, Customer Journey Analytics tools, or Adobe Analytics tools for performance metrics. |
| Campaign list pagination is limited | Campaign listing returns the first page of results, up to 50 campaigns sorted alphabetically. Offset and limit values are not applied. | Use `Get Campaign` directly if the campaign ID is known. Use the Journey Optimizer UI for full browsing and filtering. |
| No server-side filtering by date, channel, or schedule | Campaign listing supports status filtering, but not publish date, schedule date, channel, or campaign type filtering. | Use the Journey Optimizer UI campaign list for native date and channel filtering. |
| Message content retrieval unavailable | Message HTML, subject lines, personalization tokens, and offer content are not available through the current tools. | View message content and personalization directly in the Journey Optimizer UI. |