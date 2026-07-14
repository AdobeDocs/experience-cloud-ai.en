---
title: Adobe Analytics tools in Adobe CX Coworker Gateway
description: Learn which Adobe Analytics tools are available through Adobe CX Coworker Gateway.
---
# Adobe Analytics tools in Adobe CX Coworker Gateway {#aa-mcp}

You can use Adobe Analytics tools to explore report suites, discover dimensions and metrics, run reports, and manage selected analytics components from an MCP-compatible client. These tools are available through the unified [Adobe CX Coworker Gateway](overview.md) when your account has the required Adobe Analytics license and permissions.

>[!AVAILABILITY]
>
>Analytics tools are available to customers with an Adobe Analytics license. Access is controlled by the **MCP Access** permission in Adobe Admin Console. Read the [Access CX Coworker Gateway tools](access.md) for more information.

## Key capabilities {#mcp-capabilities}

Adobe Analytics tools support analytics discovery and reporting workflows from your MCP client. You can:

- Discover report suites and inspect how they are configured.
- Find dimensions, metrics, calculated metrics, segments, date ranges, and workspace projects.
- Run ranked and trended reports with dimensions, metrics, date ranges, and segment filters.
- Create and update selected reusable components, such as segments and date ranges.
- Generate insights from Adobe Analytics data using natural language.

>[!IMPORTANT]
>
>Some Adobe Analytics tools can create or update analytics components. Review and validate all MCP-initiated changes before relying on them.

## Tool coverage {#mcp-tools}

| Area | What you can do |
| --- | --- |
| Report suites | Discover report suites available to your account and inspect configuration details. |
| Components | Find and describe dimensions, metrics, calculated metrics, segments, and date ranges. |
| Reporting | Run ranked and trended reports using selected dimensions, metrics, date ranges, and segment filters. |
| Segments and date ranges | Create and update reusable segments and date ranges where your product permissions allow it. |
| Workspace projects | Discover and describe Analysis Workspace projects. |

For the complete, current list of tools, see the [Adobe Analytics MCP tool reference](https://developer.adobe.com/analytics-mcp/docs/aa/reference){target="_blank"}.

## Example prompts {#mcp-use-cases}

| Goal | Example prompt |
| --- | --- |
| Discover report suites | "List the report suites I can access." |
| Find components | "Find metrics related to revenue." |
| Run a report | "Run a ranked report for page views by page for the last 7 days." |
| Inspect a segment | "Describe the segment `[segment name]` and show me its definition." |
| Explore projects | "List my Analysis Workspace projects related to acquisition." |

## Product context and permissions {#mcp-context}

Your account must belong to an Adobe Analytics product profile that includes the **MCP Access** permission item, granted by a system or product administrator in Adobe Admin Console.

Product permissions still apply. Your account must be able to view the report suites, components, reports, and projects you query, and must have the appropriate product permissions for write operations such as creating or updating reusable components.

## More information {#mcp-more}

For the complete tool reference and getting-started guide, see the [Adobe Analytics MCP documentation](https://developer.adobe.com/analytics-mcp/docs/aa/){target="_blank"}.