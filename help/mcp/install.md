---
title: Install AdobeCX Enterprise MCP
description: Learn how to connect MCP-compatible clients to the Adobe CX Enterprise MCP.
---
# Install Adobe CX Enterprise MCP {#mcp-install}

Read this guide to learn how to connect an MCP-compatible client to Adobe CX Enterprise. CX Enterprise uses one endpoint for all documented tool families:

```
https://cx-enterprise.adobe.io/mcp
```

Before installing, confirm that your organization and user account can access the tool families you need. See [Access CX Enterprise MCP tools](access.md).

## How installation works {#mcp-install-how}

CX Enterprise MCP uses a remote HTTP transport with a browser-based Adobe sign-in flow. In every supported client, the setup pattern is the same:

1. Add the endpoint URL: `https://cx-enterprise.adobe.io/mcp`.
2. Save or enable the connection.
3. Complete the browser-based Adobe sign-in the first time the client invokes a tool.
4. Set your Adobe organization and sandbox for the session if your tools require them. See [Product context for tool calls](#mcp-connect-params).

>[!NOTE]
>
>No API keys, bearer tokens, client secrets, or additional headers are required in the MCP client configuration. Authentication is handled through the Adobe sign-in flow on first use.

## Enterprise installation (admin-managed) {#mcp-install-enterprise}

Most team and enterprise MCP client plans require an administrator to add custom connectors for the organization. In these environments, installation has two steps:

1. An administrator adds the CX Enterprise endpoint once for the organization.
2. Each user enables the connector and signs in with their own Adobe credentials.

### Step 1: An administrator adds the endpoint {#mcp-install-enterprise-admin}

The administrator adds `https://cx-enterprise.adobe.io/mcp` as a custom connector or remote MCP server in the client's organization settings. The exact location depends on the client.

#### Claude Team and Enterprise {#mcp-install-enterprise-claude}

In [!DNL Claude] Team and Enterprise plans, organization-level connectors are managed by a workspace **Owner** or **Primary Owner**.

1. Sign in to [!DNL Claude] as an **Owner** or **Primary Owner**.
2. Go to **Settings** > **Administration** > **Connectors**. On some plans, this appears as **Organization settings** > **Connectors**.
3. Select **Add custom connector**.
4. Enter `https://cx-enterprise.adobe.io/mcp` as the server URL and use a recognizable name, such as "Adobe for CX Enterprise".
5. Save the connector.

#### ChatGPT Team and Enterprise {#mcp-install-enterprise-chatgpt}

In [!DNL ChatGPT] Team and Enterprise workspaces, connectors are added by a workspace administrator.

1. Sign in to [!DNL ChatGPT] as a workspace administrator.
2. Go to **Settings** > **Connectors**. On some plans, this appears as **Settings** > **Apps & Connectors**.
3. Select **Add connector**.
4. Enter `https://cx-enterprise.adobe.io/mcp` as the server URL.
5. Save the connector. Depending on your workspace configuration, this step may require enabling developer mode or granting workspace-level approval.

#### Other organization-managed clients {#mcp-install-enterprise-other}

For other clients that support organization-managed remote connectors, add CX Enterprise as a remote HTTP MCP server using `https://cx-enterprise.adobe.io/mcp`. Leave optional headers, bearer token fields, client ID fields, and client secret fields empty unless your client requires a placeholder value.

### Step 2: Users enable the connector {#mcp-install-enterprise-user}

After an administrator adds CX Enterprise, each user enables it for their own account:

1. Open personal connector, app, or MCP settings in the client.
2. Find the CX Enterprise connector and enable it.
3. Start a conversation, invoke one of the Adobe tools, and complete the browser-based Adobe sign-in when prompted.
4. Set your Adobe organization and sandbox for the session if your tools require them. See [Product context for tool calls](#mcp-connect-params).

Users do not need to enter the URL themselves when an administrator has already added the connector for the organization.

## Individual installation (self-service) {#mcp-install-individual}

If you use an individual plan, a locally configured developer client, or an organization that allows members to add their own connectors, add the endpoint directly in your own client settings.

### Claude individual {#mcp-install-individual-claude}

For `claude.ai` and [!DNL Claude] Desktop on an individual plan:

1. Open **Settings** > **Connectors**.
2. Select **Add custom connector**.
3. Enter `https://cx-enterprise.adobe.io/mcp` as the server URL.
4. Save and enable the connector, then complete the Adobe sign-in flow on first use.

### ChatGPT individual {#mcp-install-individual-chatgpt}

1. Open **Settings** > **Connectors**. On some plans, this appears as **Settings** > **Apps & Connectors**.
2. Select **Add connector**.
3. Enter `https://cx-enterprise.adobe.io/mcp` as the server URL.
4. Save and enable the connector, then complete the Adobe sign-in flow on first use.

### Cursor {#mcp-install-individual-cursor}

1. Open **Settings** > **MCP**.
2. Select **Add new server**.
3. Enter `https://cx-enterprise.adobe.io/mcp` as the server URL.
4. Select **Connect** and complete the Adobe sign-in flow.

After connection, entitled Adobe for CX Enterprise tools are available in Cursor's Composer and Agent modes.

### Claude Code {#mcp-install-individual-claude-code}

Add the endpoint from the terminal:

```bash
claude mcp add --transport http cx-enterprise https://cx-enterprise.adobe.io/mcp
```

Then start [!DNL Claude Code] and run:

```text
/mcp
```

Select the `cx-enterprise` server and complete the Adobe sign-in flow in your browser.

### Codex {#mcp-install-individual-codex}

Add the endpoint from the terminal:

```bash
codex mcp add cx-enterprise --url https://cx-enterprise.adobe.io/mcp
```

Authenticate:

```bash
codex mcp login cx-enterprise
```

Verify the configuration:

```bash
codex mcp list
```

You can also add the endpoint directly to `~/.codex/config.toml`:

```toml
[mcp_servers.cx-enterprise]
url = "https://cx-enterprise.adobe.io/mcp"
```

### General JSON configuration {#mcp-install-individual-json}

For clients that accept a JSON-based MCP server configuration, use one of the following formats depending on whether your client supports native remote HTTP or requires a local bridge.

**Via `mcp-remote` bridge**

```json
{
  "mcpServers": {
    "cx-enterprise": {
      "command": "npx",
      "args": [
        "mcp-remote",
        "https://cx-enterprise.adobe.io/mcp"
      ]
    }
  }
}
```

**Native remote HTTP**

```json
{
  "mcpServers": {
    "cx-enterprise": {
      "url": "https://cx-enterprise.adobe.io/mcp",
      "transport": "http"
    }
  }
}
```

### Other clients {#mcp-install-individual-other}

For other desktop or web clients with remote MCP support, add Adobe for CX Enterprise as a remote HTTP server using `https://cx-enterprise.adobe.io/mcp`. Leave optional headers, bearer token fields, client ID fields, and client secret fields empty unless your client requires a placeholder value.

## Product context for tool calls {#mcp-connect-params}

The MCP scopes every tool call to one Adobe organization and sandbox, set at the connection level and shared across all tool families. You do not switch organizations or sandboxes from individual tools — set the context once for the session, and every product tool operates within it. Experience Platform-based tools, including Real-Time CDP and Experience Platform, require this context; analytics tools resolve against the entitlements on your Adobe credentials.

Set the context at the start of a session. Example:

> "Use organization `1234ABCD@AdobeOrg` and sandbox `prod` for this session."

If you do not know the required values, ask your MCP client to list the organizations or sandboxes available to your Adobe credentials.