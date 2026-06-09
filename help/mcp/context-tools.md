---
title: Session context tools in CX Enterprise MCP
description: Learn about the core tools that set organization, sandbox, and data view context for all CX Enterprise MCP tool calls.
---
# Session context tools in Adobe CX Enterprise MCP {#mcp-core}

Adobe CX Enterprise MCP includes a set of session context tools that establish the Adobe organization, Adobe Experience Platform sandbox, and Customer Journey Analytics data view that all other product tools operate within. No additional license or enablement is required — these tools are available to every authenticated user after connecting to the [CX Enterprise MCP server](overview.md).

## How context works {#mcp-core-how}

CX Enterprise MCP scopes every tool call to one active Adobe organization. Beyond that, context requirements depend on the product:

- **Experience Platform–based products** — [Real-Time CDP](rtcdp-mcp.md), [Experience Platform](aep-mcp.md), and [Journey Optimizer](ajo-mcp.md) tools operate within an Experience Platform sandbox. Set the sandbox once per session with `core-set_sandbox`; all three share it.
- **Other products** — Products not built on Experience Platform do not use sandbox context. For example, [Customer Journey Analytics](cja-mcp.md) tools resolve against a data view and [Adobe Analytics](aa-mcp.md) tools resolve against report suites.

Set context once at the start of a session — individual product tools do not switch organizations, sandboxes, or data views mid-session.

## Available tools {#mcp-core-tools}

| Tool | Description |
| --- | --- |
| `core-list_orgs` | Lists the Adobe organizations accessible to the authenticated user. Returns each organization's display name and `@AdobeOrg` identifier. Use this to look up the org ID before calling `core-switch_org`. |
| `core-switch_org` | Sets the active Adobe organization for the session. All subsequent tool calls are scoped to this organization until the session ends or the organization is switched again. |
| `core-list_sandboxes` | Lists the Experience Platform sandboxes available in the active organization. Returns each sandbox's name, title, type (production or development), and state. Use this to look up a sandbox name before calling `core-set_sandbox`. |
| `core-set_sandbox` | Sets the active Experience Platform sandbox for the session. Real-Time CDP, Experience Platform, and Journey Optimizer tools scope their data to this sandbox. |
| `core-list_dataviews` | Lists the Customer Journey Analytics data views available to the authenticated user in the current context. Returns data view IDs and display names. Use this to look up a data view before calling `core-set_dataview`. |
| `core-set_dataview` | Sets the default Customer Journey Analytics data view for the session. When set, CJA tools that require a data view — such as `findDimensions`, `findMetrics`, and `runReport` — use this value automatically unless a different data view is specified in the individual tool call. |

## Typical session setup {#mcp-core-setup}

Set context at the start of a session before invoking product tools:

1. **Organization** — Call `core-list_orgs` to list your accessible organizations, then `core-switch_org` with the target organization ID.
2. **Sandbox** — If you plan to use Real-Time CDP, Experience Platform, or Journey Optimizer tools, call `core-list_sandboxes` to list available sandboxes, then `core-set_sandbox` with the target sandbox name.
3. **Data view** (CJA only) — If you plan to use Customer Journey Analytics tools, call `core-list_dataviews` to list available data views, then `core-set_dataview` with your chosen data view.

You can ask your MCP client to complete this setup in a single natural language request:

> "Use organization `1234ABCD@AdobeOrg`, sandbox `prod`, and data view `My Company — Global` for this session."

The client will call the appropriate tools and confirm once the context is set.

>[!TIP]
>
>If your Adobe credentials belong to only one organization, `core-list_orgs` and `core-switch_org` still work, but the effective org will be the same regardless. You still need to call `core-set_sandbox` if you plan to use Real-Time CDP, Experience Platform, or Journey Optimizer tools, and `core-set_dataview` if you plan to use Customer Journey Analytics tools.

## Example prompts {#mcp-core-examples}

| Goal | Example prompt |
| --- | --- |
| Discover available organizations | "What Adobe organizations do I have access to?" |
| Set organization context | "Switch to organization `My Org (1234ABCD@AdobeOrg)`." |
| Discover available sandboxes | "List the sandboxes available in my current organization." |
| Set sandbox context | "Use the `prod` sandbox for this session." |
| Discover available data views | "What Customer Journey Analytics data views can I access?" |
| Set data view context | "Set `My Company — Global` as the default data view." |
| Full session setup | "Set up a session using organization `1234ABCD@AdobeOrg`, sandbox `prod`, and data view `My Company — Global`." |

## Related pages {#mcp-core-related}

- [Install Adobe CX Enterprise MCP](install.md) — how to connect your MCP client, including the product context setup section.
- [Access CX Enterprise MCP tools](access.md) — access requirements by product.