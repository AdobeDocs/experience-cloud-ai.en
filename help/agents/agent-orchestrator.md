---
title: Adobe Experience Platform Agent Orchestrator
description: overview doc for agent orchestrator (WIP)
hide: true
hidefromtoc: true
---
# Adobe Experience Platform Agent Orchestrator

Adobe Experience Platform Agent Orchestrator is the intelligent layer powering AI Assistant. When you ask questions or request help, Agent Orchestrator automatically calls upon specialized agents to get you the right answers. Agent Orchestrator remembers your conversation history, enabling you to build on previous questions naturally without repeating context, and combines insights from multiple agents to present you with clear, unified responses.

You can complete complex workflows through simple conversation without needing to know which agents are working behind the scenes. The system understands your goals, creates step-by-step plans, and can adjust its approach as needed. You can explore the reasoning panel to see the step-by-step thinking process and better understand how your requests are being handled.

Read this document to learn about Agent Orchestrator.

## Components of Agent Orchestrator

Read this section for information on the several components of Agent Orchestrator.

![The marketing architecture of Agent Orchestrator.](./images/agent-orchestrator/agentic-architecture.png)

### AI Assistant conversational interface

AI Assistant in Adobe Experience Platform is a conversational experience that you can use to accelerate your workflows in Adobe applications. You can use AI Assistant to better understand product knowledge, troubleshoot problems, or search through information and find operational insights. AI Assistant supports Experience Platform, Real-Time Customer Data Platform, Adobe Journey Optimizer and Customer Journey Analytics. You can use AI Assistant to access Experience Platform Agents and other AI capabilities.

For more information, read the [AI Assistant UI guide](ui-guide.md).

### Reasoning engine

The reasoning engine is the main decision-maker in Agent Orchestrator. It understands your goals, checks any limits or requirements, and creates step-by-step plans to help you reach your objectives. Unlike simple question-and-answer systems, it can adjust its plans as things change, and can go back and try different approaches if needed. The plans it creates are shown to you in the AI Assistant, so you can see and follow the process. 

### Adobe Experience Platform agents

| Agent | Details |
| --- | --- |
| Audience Agent | Audience Agent lets you view insights about audiences, including detecting significant audience size changes, detecting duplicate audiences, explore your audience inventory, and retrieve your audiences' size. |
| Data Insights Agent | Data Insights Agent, accessible from the AI Assistant in Customer Journey Analytics, is a generative AI conversation agent that quickly and efficiently answers questions about your data. It builds relevant visualizations in Analysis Workspace using components from your data view and using your actual data. |
| Experimentation Agent | |
| Field Discovery Agent | Field Discovery Agent helps users automatically discover and understand data fields within their schemas and datasets. This intelligent agent analyzes your data structure and provides insights about field usage, relationships, and recommendations for optimization. |
| Product Support Agent | Product Support Agent is a self-serve debugging and troubleshooting capability that helps you troubleshoot Adobe Experience Platform features and applications without leaving your workflows. Support administrators can create customer support tickets with context from your AI Assistant interactions and you can check ticket updates through AI Assistant. |

### Knowledge base

The knowledge base provides agents with secure access to customer business intelligence through structured and unstructured data sources, including Adobe product documentation, customer metadata about business objects, and analytics data.

## Access

All AI Assistant requests are authenticated using Adobe Identity Management Services (IMS) and authorizations are enforced by the Adobe Experience Platform Access Control Service (or the CJA Access Control Service).

To enable a user to access the AI Assistant conversational interface and use one or more Experience Platform Agents, the customer's Adobe Admin must grant relevant permissions in the Permissions UI or the Adobe Admin Console:

* For Real-Time Customer Data Platform (Real-Time CDP) and Adobe Journey Optimizer users – The Adobe Admin must grant "Enable AI Assistant" permission to enable a user to access AI Assistant. To allow the user to ask operational insight questions, the Adobe Admin must additionally grant them "View operational insights" permission. Both permissions are set by the Admin in the Permissions UI.

* For Customer Journey Analytics users – The Adobe Admin must grant the user permission to access AI Assistant in the HYPERLINK "https://experienceleague.adobe.com/en/docs/analytics-platform/using/technotes/access-control"Adobe , which enables the user to ask product knowledge and data insights questions. Note: Operational insights questions are not available for Customer Journey Analytics; therefore, no additional permissions apply. which enables the user to ask product knowledge and data insights questions. Note: Operational insights questions are not available for Customer Journey Analytics; therefore, no additional permissions apply. For more information about Adobe IMS, please see the Adobe Identity Management Services Security Overview.

## General best practices/notes


