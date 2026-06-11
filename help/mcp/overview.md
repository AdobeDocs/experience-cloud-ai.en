---
title: Adobe CX Enterprise MCP servers
description: Adobe CX Enterprise MCP server is the unified MCP for Adobe CX Enterprise, giving MCP clients a single connection to supported product tools.
---
# Adobe CX Enterprise MCP servers {#mcp-overview}

Adobe CX Enterprise MCP servers is the unified Model Context Protocol (MCP) for Adobe CX Enterprise. With one connection, MCP-compatible clients can access the Adobe product tools your organization and account are entitled to use.

Use the CX Enterprise endpoint for all MCP client setup:

```
https://cx-enterprise.adobe.io/mcp
```

After you connect, the endpoint exposes the tools available to your Adobe organization and credentials. Product-specific pages in this guide describe what each product tool can do, what data it can access, and any product-specific limitations.

## What is the Model Context Protocol? {#mcp-what-is}

MCP is an open standard that lets applications expose tools to large language models (LLMs) in a uniform way. MCP-compatible clients such as [!DNL Claude], [!DNL ChatGPT], [!DNL Cursor], [!DNL Claude Code], [!DNL Codex], and [!DNL VS Code] can use those tools to retrieve product context, run supported operations, and return answers in natural language.

CX Enterprise provides a governed endpoint for CX Enterprise product tools. Instead of adding separate product servers, connect once to the endpoint and use the product tools surfaced for your entitled solutions.

## Available product tools {#available-product-tools}

The following product tools are documented in this guide:

| Product tools | What it exposes through the endpoint | Availability | Documentation |
| --- | --- | --- | --- |
| **Real-Time CDP** | Audiences, destinations, sources, identity namespaces, and activation health (read-only) | Beta | [Real-Time CDP tools](rtcdp-mcp.md) |
| **Experience Platform** | Schemas, datasets, data governance, Query Service, and audit events (read-only) | Beta | [Experience Platform tools](aep-mcp.md) |
| **Journey Optimizer** | Campaigns and channel configurations (read-only) | Beta | [Journey Optimizer tools](ajo-mcp.md) |
| **Customer Journey Analytics** | Data views, dimensions, metrics, reports, segments, date ranges, projects, and audiences (read and write) | Available | [Customer Journey Analytics tools](cja-mcp.md) |
| **Adobe Analytics** | Report suites, dimensions, metrics, reports, segments, date ranges, and workspace projects (read and write for supported components) | Available | [Adobe Analytics tools](analytics-mcp.md) |
| **Workfront** | Work management tools for projects, tasks, and approval workflows | Preview | [Workfront MCP server](https://experienceleague.adobe.com/en/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-overview) |

>[!NOTE]
>
>Tool availability depends on your product licenses, organization enablement, product permissions, and the Adobe credentials used to authenticate. The MCP only surfaces tools your organization and user account are entitled to access. See [Access CX Enterprise MCP tools](access.md).

## Get started {#mcp-get-started}

1. Review [Access CX Enterprise MCP tools](access.md) to confirm product availability, enablement, and permissions.
2. Follow [Install Adobe for CX Enterprise MCP](install.md) to connect your MCP client to the endpoint.
3. Review the product page for each product tool you plan to use.

## How it works {#mcp-how}

Adobe CX Enterprise uses a remote HTTP transport with a browser-based Adobe sign-in flow. No API keys, bearer tokens, client secrets, or additional headers are stored in your MCP client configuration. On first use, the client opens a browser-based Adobe sign-in flow and the endpoint discovers the Adobe authorization server automatically.

The MCP establishes your Adobe organization and sandbox context for the session, and all product tools operate within that context — individual tools do not switch organizations or sandboxes. Set this context once at the start of a session; see [Product context for tool calls](install.md#mcp-connect-params).

## Security, beta, and legal notices {#mcp-notices}

>[!WARNING]
>
>The Model Context Protocol (MCP) is an emerging open-source standard and may present security or reliability risks. Adobe MCP integrations and related documentation are provided "as is," without warranties of any kind.
>
>Connecting MCP clients to Adobe products is a customer-elected configuration. Customers are responsible for evaluating the security and suitability of any MCP integration. Adobe is not responsible for issues arising from misconfiguration, misuse of MCP, vulnerabilities in third-party implementations, or unintended actions performed through MCP-enabled workflows.
>
>To reduce risk, Adobe encourages testing integrations in a sandbox environment before production use, and carefully reviewing and validating MCP-initiated actions and responses before confirming or relying on them.

Beta product tools and Beta documentation are subject to change before general availability. Adobe makes no representations about the completeness or accuracy of Beta documentation. By using any Adobe MCP feature identified as Beta, you acknowledge that the Beta is provided **"as is" without warranty of any kind** and that Adobe has no obligation to maintain, correct, update, change, modify, or otherwise support the Beta. Beta materials are considered Confidential Information of Adobe. Any feedback you provide to Adobe about the Beta, including problems, defects, suggestions, improvements, or recommendations, is assigned to Adobe, including all rights, title, and interest in that feedback.