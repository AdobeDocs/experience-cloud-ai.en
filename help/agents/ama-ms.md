---
title: Adobe Marketing Agent for Microsoft 365 Copilot
description: Learn how you can use the Adobe Marketing Agent for Microsoft 365 Copilot.
hide: true
hidefromtoc: true
---
# Adobe Marketing Agent for [!DNL Microsoft 365 Copilot]

The Adobe Marketing Agent for [!DNL Microsoft 365 Copilot] is an AI-powered tool that connects Adobe Experience Platform directly to [!DNL Microsoft 365 Copilot]. With this agent, you can ask natural-language questions within [!DNL Microsoft 365] applications such as [!DNL Teams], [!DNL Word], [!DNL Powerpoint], and [!DNL Excel] to instantly retrieve marketing insights from Experience Platform without interrupting your workflow. The same agent is available across these apps, and your chat history with the Adobe Marketing Agent carries over—so you can start research in [!DNL Copilot] in [!DNL Teams], for example, and continue the conversation in [!DNL Word] or [!DNL Powerpoint] while you draft a campaign brief or review a presentation.

With the Adobe Marketing Agent for [!DNL Microsoft 365 Copilot], marketing managers, analytics and insights teams, and business stakeholders can:

- Make faster, data-driven marketing decisions.
- Reduce time spent switching between tools.
- Simplify access to audience and journey insights across teams.

## How the agent works

The Adobe Marketing Agent for [!DNL Microsoft 365 Copilot] provides an integrated experience between Experience Platform and [!DNL Microsoft 365] applications:

- Adobe Marketing Agent appears as an agent in [!DNL Microsoft 365 Copilot], including in [!DNL Teams], [!DNL Word], [!DNL Powerpoint], and [!DNL Excel].
- Sign in with your Adobe account and select the data environment (sandbox, data view) that you would like to use.

### Data access and permissions

The answers you receive reflect the **data and access level** tied to your Adobe identity, what you can query and see is the same as what you are entitled to in Experience Platform and its associated solutions. The Adobe Marketing Agent **inherits** those permissions and does **not** require a separate permissions setup for the [!DNL Microsoft 365] integration. For underlying Experience Platform AI Assistant capabilities and other Adobe AI agents, **permission requirements are unchanged** from using those features in Experience Platform.

The agent connects your [!DNL Microsoft 365] instance to Experience Platform and its associated applications (Real-Time CDP, Adobe Journey Optimizer, and Customer Journey Analytics). With this integration, you can then use the Experience Platform AI Assistant and agents to retrieve relevant insights directly to your [!DNL Microsoft 365] instance. The answers returned in your [!DNL Microsoft 365] instance are presented as conversational and natural language texts, tables, and data visualizations. Additionally, support for follow-up questions and investigations are available within the same [!DNL Copilot] chat.

## Key use cases and example scenarios

| Use case | Description |
| --- | --- |
| Retrieve operational insights for audiences and customer journeys | With the Adobe Marketing Agent, you can easily retrieve operational insights across your audiences and customer journeys. You can identify which audiences are the largest or most engaged, so you can prioritize where to focus your efforts. You can see which customer journeys are currently active and learn how they are performing, helping you pinpoint opportunities for optimization. The agent also lets you track how your different segments are growing or shrinking over time, empowering you to respond to changes in your audience dynamics as they happen.  |
| Use data visualization to better analyze customer journeys and campaigns | You can review journey performance and drop‑offs, compare campaign performance over time, and understand which touchpoints drive conversions. Additionally, you can generate visual reports on campaign performance and compare these across channels, regions, or over different time periods. You can also explore trends without needing to manually build queries or dashboards. |
| Empower collaboration and decision-making | Use pre‑built "starter prompts" to explore audiences, campaigns, and web traffic. Take advantage of a natural‑language interface for easier learning of Experience Platform and Customer Journey Analytics concepts. Furthermore, you can share insights on [!DNL Teams] channels or chats during planning meetings. You can also use the Adobe Marketing Agent to answer ad-hoc questions in real-time while reviewing plans or decks, allowing you to keep stakeholders aligned on the same set of metrics and definitions. |

## Prerequisites 

Before you can use the Adobe Marketing Agent for [!DNL Microsoft 365 Copilot], you must first ensure that you have the following:

- [!DNL Microsoft 365] with [!DNL Microsoft Teams] or [!DNL Microsoft Copilot Chat].
- Experience Platform and at least one of: Real-Time CDP, Adobe Journey Optimizer, and/or Customer Journey Analytics.
- Entitlement to the Experience Platform Agent Orchestrator and agents.
- Access to your organization's Adobe Experience Cloud account (sign-in and product entitlements) for the solutions and data you use. If you do not have Adobe access, contact your Adobe administrator.

## Enable the agent for your organization {#enable-the-agent-for-your-organization}

End users can use the Adobe Marketing Agent only after it is made available in your [!DNL Microsoft 365] tenant. **Work with your [!DNL Microsoft 365] Copilot administrator** (or equivalent admin for Copilot agents in your organization) to enable access and assign the agent as your organization requires.

Typical outcomes after admin setup include:

- You can open **[!DNL Agent Store]** in [!DNL Teams], find **[!DNL Adobe Marketing Agent]** in your list of agents, and choose **[!DNL Add]** to attach it to your Copilot agents.
- Alternatively, your Copilot administrator can **publish** the agent to everyone in your organization or to specific groups so users do not need to add it individually.

For administrator steps and policy options in the [!DNL Microsoft 365] admin center, see [Manage agents for Microsoft 365 Copilot](https://learn.microsoft.com/en-us/microsoft-365-copilot/extensibility/manage) in the Microsoft documentation.

## Get started

After your organization has enabled the agent (see [Enable the agent for your organization](#enable-the-agent-for-your-organization)), navigate to [!DNL Microsoft 365 Copilot] in the application of your choice and use the left-navigation to select **[!DNL All Agents]**.

![Microsoft 365 Copilot left navigation with All Agents selected.](../agents/images/ama/all-agents.png)

Locate the card for [!DNL Adobe Marketing Agent] or use the search bar to manually look for the agent. Once you have the agent, select the card.

![Adobe Marketing Agent card or search result in the agents gallery.](../agents/images/ama/select-ama.png)

Use the pop-up window to learn more information about the agent, once you are ready, select **[!DNL Add]**.

![Adobe Marketing Agent details pop-up with Add button highlighted.](../agents/images/ama/add-ama.png)

The [!DNL Microsoft 365 Copilot] dashboard updates with the [!DNL Adobe Marketing Agent] branding now on the main page.

![Microsoft 365 Copilot home page showing Adobe Marketing Agent on the main dashboard.](../agents/images/ama/home.png)

### Sign in and set your context

Next, prompt the agent to sign in and follow the ensuing steps required to authenticate your account. During this step, you will need to copy a numerical code that the agent returns and then sign in to your Adobe organization. If you cannot complete sign-in or you lack access to Adobe solutions for your organization, contact your **Adobe administrator**.

![Adobe sign-in step showing a numerical code to copy and instructions to authenticate with your Adobe organization.](../agents/images/ama/sign-in.png)

When successful, use the context setter to establish the documentation source, sandbox, and dataview that you will use for your queries.

![Context setter UI to choose documentation source, sandbox, and data view for queries.](../agents/images/ama/context.png)

### Use the agent to retrieve operational insights 

Once you are signed in, you can use the prompts provided in the main page to get started. You can also take advantage of a starter prompt that can branch out to analyzing marketing audiences, reviewing campaign performances, and monitoring campaign journeys. For example, select **[!DNL Review campaign performance]** and then select **[!DNL Analyze engagement - Show web visitors for top 10 products last week]**

![Starter prompts on the agent home page, including Review campaign performance and Analyze engagement options.](../agents/images/ama/starter-guide.png)

Allow for a few moments for the agent to calculate and then the agent responds with a visualized representation of your data. You can use the bar chart presented or you can select **[!DNL View data]** to view the data in tables.

![Agent response with a bar chart visualizing web visitors for top products and View data option.](../agents/images/ama/response.png)

![Same insights shown as a data table after selecting View data.](../agents/images/ama/tables.png)

You can further investigate by selecting follow up questions that the agent recommends. Alternatively, you can pivot and try different starter prompts, verify the information sources that the agent referenced, or provide feedback using the feedback mechanism.

![Suggested follow-up questions below the agent's response for further investigation.](../agents/images/ama/follow-up.png)

For more information on the AI Assistant UI features, read the guide on [using the AI Assistant](../ai-assistant/ai-assistant-ui.md).

## Security, Privacy, and Responsible AI

**Data handling and governance**

The Adobe Marketing Agent relies on the same controls and governance that apply to Experience Platform and [!DNL Microsoft 365]. Your organization retains ownership and control of its data. Insights returned through the agent are scoped to each user's Adobe permissions and data entitlements; no additional permission model is introduced for the [!DNL Microsoft 365] surface beyond what already applies in Experience Platform and related Adobe AI agents.

**Responsible AI use**

The agent is intended to return read‑only insights and does not modify your customer data in Experience Platform. You should review any generated summaries and analyses before you use them to make business decisions.

**Supported languages and scope**

The initial release is available as an English‑language experience. Capabilities are limited to read‑only insights; the agent does not create or update marketing assets or configurations.

## Appendix

Read the following for additional information on the Adobe Marketing Agent for [!DNL Microsoft Copilot 365].

### Adobe Marketing Agent [!DNL Microsoft 365 Copilot] admin steps

To set up agents from an external provider (third-party developers or the Microsoft Commercial Marketplace), you must first ensure your tenant settings allow external apps and then manage them through the Integrated Apps or Agents section of the admin center.

#### Enable external agents in tenant settings

Before you can deploy external agents, your organization's policy must allow them.

- Log in to the [Microsoft 365 admin center](https://admin.microsoft.com/).
- Go to **Agents** > **Settings** > **User access**.
- Under **Allowed agent types,** ensure **Allow apps and agents built by external publishers** is selected.

>[!IMPORTANT]
>
>If this setting is disabled, external agents will not appear in the [Agent Store](https://devblogs.microsoft.com/microsoft365dev/introducing-the-agent-store-build-publish-and-discover-agents-in-microsoft-365-copilot/) for your users.

#### Acquire and approve the agent

Typically, you can find external agents in the [[!DNL Microsoft Commercial Marketplace]](https://appsource.microsoft.com/).

- **From the Marketplace**: Find the agent you want and select **Get it now**. This will often redirect you back to your admin center's **Integrated Apps** page.
- **Review Permissions**: In the [Integrated Apps](https://learn.microsoft.com/en-us/microsoft-365/admin/manage/manage-deployment-of-add-ins?view=o365-worldwide) list, select the external agent.
- Review the **Data & tools** and **Security & compliance** tabs to see what data the external provider will access.
- Select **Approve** or **Activate** to move it into your organization's inventory.

#### Deploy to certain users

Once approved, you can control exactly who sees the agent in their Copilot sidebar.

- In the [[!DNL Microsoft 365] admin center](https://admin.microsoft.com/), navigate to **Agents** > **All agents**.
- Select the external agent from the list.
- Select **Deploy** (or **Edit Assignment**).
- Choose **Specific users/groups** and search for the individuals or [!DNL Entra ID] groups who should have it.
- Select **Finish deployment**. This "pushes" the agent to those users so it appears automatically in their Copilot interface.

#### Manage updates

External providers frequently update their agents. In order to manage these updates, follow the best practices below:

- Check the [[!DNL Agent Registry]](https://learn.microsoft.com/en-us/microsoft-365/admin/manage/agent-registry?view=o365-worldwide) periodically.
- If an update requires new permissions, the agent may show a status of **Pending Update**.
- You must manually **Approve Updates** before the new version is rolled out to your assigned users.