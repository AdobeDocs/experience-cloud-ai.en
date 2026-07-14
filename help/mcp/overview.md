---
title: Adobe CX Coworker Gateway
description: Adobe CX Coworker Gateway is the unified MCP for Adobe CX Enterprise, giving MCP clients a single connection to supported product tools.
---
# Adobe CX Coworker Gateway {#mcp-overview}

Adobe CX Coworker Gateway is the unified Model Context Protocol (MCP) for Adobe CX Enterprise. With one connection, MCP-compatible clients can access the Adobe product tools your organization and account are entitled to use.

>[!IMPORTANT]
>
>Your Adobe organization must be enabled before you can use **CX Coworker Gateway** tools.
>
>If your organization does not yet have access, email [cx-coworker-gateway-support@adobe.com](mailto:cx-coworker-gateway-support@adobe.com) to request enablement for your organization.

Use the CX Coworker Gateway endpoint for all MCP client setup:

```
https://cx-coworker-gateway.adobe.io/mcp
```

After you connect, the endpoint exposes the tools available to your Adobe organization and credentials. Product-specific pages in this guide describe what each product tool can do, what data it can access, and any product-specific limitations.

## What is the Model Context Protocol? {#mcp-what-is}

MCP (Model Context Protocol) is an open-source standard for connecting AI applications to external systems. MCP-compatible clients such as [!DNL Claude], [!DNL ChatGPT], [!DNL Cursor], [!DNL Claude Code], [!DNL Codex], and [!DNL VS Code] can use those tools to retrieve product context, run supported operations, and return answers in natural language.

CX Coworker Gateway provides a governed endpoint for CX Coworker Gateway product tools. Instead of adding separate product servers, connect once to the endpoint and use the product tools surfaced for your entitled solutions.

## Available product tools {#available-product-tools}

The following product tools are documented in this guide:


| Product tools                  | What it exposes through the endpoint                                                                                                 | Availability | Documentation                                                                                                                                |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------ | -------------------------------------------------------------------------------------------------------------------------------------------- |
| **Real-Time CDP**              | Audiences, destinations, sources, identity namespaces, and activation health (read-only)                                             | Beta         | [Real-Time CDP tools](rtcdp-mcp.md)                                                                                                          |
| **Experience Platform**        | Schemas, datasets, data governance, Query Service, and audit events (read-only)                                                      | Beta         | [Experience Platform tools](aep-mcp.md)                                                                                                      |
| **Journey Optimizer**          | Campaigns and channel configurations (read-only)                                                                                     | Beta         | [Journey Optimizer tools](ajo-mcp.md)                                                                                                        |
| **Customer Journey Analytics** | Data views, dimensions, metrics, reports, segments, date ranges, projects, and audiences (read and write)                            | Available    | [Customer Journey Analytics tools](cja-mcp.md)                                                                                               |
| **Adobe Analytics**            | Report suites, dimensions, metrics, reports, segments, date ranges, and workspace projects (read and write for supported components) | Available    | [Adobe Analytics tools](analytics-mcp.md)                                                                                                    |
| **Workfront**                  | Work management tools for projects, tasks, and approval workflows                                                                    | Preview      | [Workfront MCP server](https://experienceleague.adobe.com/en/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-overview) |


>[!NOTE]
>
>Tool availability depends on your product licenses, organization enablement, product permissions, and the Adobe credentials used to authenticate. The MCP only surfaces tools your organization and user account are entitled to access. See [Access CX Coworker Gateway tools](access.md).



## Get started {#mcp-get-started}

1. Review [Access CX Coworker Gateway tools](access.md) to confirm product availability, enablement, and permissions.
2. Follow [Install Adobe for CX Coworker Gateway](install.md) to connect your MCP client to the endpoint.
3. Review the product page for each product tool you plan to use.

