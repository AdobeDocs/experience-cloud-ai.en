---
title: Access CX Coworker Gateway tools
description: Confirm product availability, organization enablement, and permissions before using Adobe CX Coworker Gateway tools.
---
# Access CX Coworker Gateway tools {#mcp-access}

Adobe CX Enterprise exposes product tools through a single MCP. Access is evaluated by product tools: your Adobe organization must be enabled for the relevant product tools, and your user account must have the product permissions required to view or change the product data those tools expose.

>[!IMPORTANT]
>
>Your Adobe organization must be enabled before you can use CX Coworker Gateway tools. If your organization does not yet have access, contact your Adobe Account Team to request enablement for your organization.

## Access requirements {#mcp-requirements}


| Product tools | Availability | Access requirements |
| --- | --- | --- |
| Real-Time CDP | Beta | Active Real-Time CDP license, Beta enablement for your Adobe organization, and permissions to view the audiences, destinations, sources, identity, and activation resources you query. |
| Experience Platform | Beta | Active Experience Platform license, Beta enablement for your Adobe organization, and permissions to view the schemas, datasets, governance, Query Service, audit, and sandbox resources you query. |
| Journey Optimizer | Beta | Active Journey Optimizer license, Beta enablement for your Adobe organization, and permissions to view campaigns and channel configurations. |
| Customer Journey Analytics | Available | Active Customer Journey Analytics license and a product profile that includes the **MCP Access** permission item in Adobe Admin Console. Product permissions still govern which data views, components, reports, projects, and audiences you can access or modify. |
| Adobe Analytics | Available | Active Adobe Analytics license and a product profile that includes the **MCP Access** permission item in Adobe Admin Console. Product permissions still govern which report suites, components, reports, segments, date ranges, and projects you can access or modify. |
| Workfront | Preview | Active Workfront license and Workfront MCP enablement. See the [Workfront MCP documentation](https://experienceleague.adobe.com/en/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-overview). |


>[!NOTE]
>
>The MCP surfaces only the tools your organization and credentials are entitled to use. If a product tool is missing after you sign in, confirm product licensing, organization enablement, and user permissions.

## Request access {#mcp-request}

For Beta or limited-release product tools, contact your Adobe account representative and specify which Adobe for CX Coworker Gateway product tools you want to use. Your representative can coordinate product enablement and confirm when your Adobe organization is ready.

For generally available product tools that use the **MCP Access** permission item, ask a system or product administrator to add your account to a product profile that includes MCP access.

## In-product enablement {#mcp-product-enablement}

Some products require in-product enablement or product-specific permissions in addition to MCP access. For example:

- Adobe Analytics and Customer Journey Analytics require the **MCP Access** permission item in Adobe Admin Console.
- Workfront MCP tools are enabled from Workfront settings.
- Beta product tools require Adobe organization enablement before their tools appear through the MCP.

Check the product page for the product tool you plan to use for product-specific permissions, context requirements, and limitations.

## Before you install {#mcp-prerequisites}

Before connecting your MCP client, confirm that:

- Your Adobe organization is enabled for the product tools you need.
- Your user account has the product permissions required for the data and operations you plan to use.
- You have access to a supported MCP client such as [!DNL Claude], [!DNL ChatGPT], [!DNL Cursor], [!DNL Claude Code], [!DNL Codex], or [!DNL VS Code].
- For enterprise installation, you or a colleague can manage connectors or custom apps in your MCP client's organization settings.

Next: [Install Adobe CX Coworker Gateway](install.md).