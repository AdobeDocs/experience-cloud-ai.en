---
title: Adobe Experience Platform Agent Orchestrator
description: overview doc for agent orchestrator (WIP)
hide: true
hidefromtoc: true
---
# Adobe Experience Platform Agent Orchestrator

Adobe Experience Platform Agent Orchestrator is the intelligent layer that powers AI Assistant. When you ask questions or request help, Agent Orchestrator automatically calls upon specialized agents to get you the right answers. Agent Orchestrator remembers your conversation history, enabling you to build on previous questions naturally without repeating context, and combines insights from multiple agents to present you with clear, unified responses.

You can complete complex workflows through simple conversation without needing to know which agents are working behind the scenes. The system understands your goals, creates step-by-step plans, and can adjust its approach as needed. You can explore the reasoning panel to see the step-by-step thinking process and better understand how your requests are being handled. With Agent Orchestrator, you can use AI Assistant to tackle complex workflows and optimize strategies across Adobe Experience Cloud applications.

Read this document to learn about Agent Orchestrator.

## Components of Agent Orchestrator {#components}

Agent Orchestrator is made up of several key parts, including the AI Assistant conversational interface, a reasoning engine for decision-making and planning, specialized Adobe Experience Platform agents, and a knowledge base that provides access to relevant information.

![The marketing architecture of Agent Orchestrator.](./images/agent-orchestrator/agentic-architecture.png)

### AI Assistant conversational interface {#ai-assistant}

AI Assistant is a conversational experience that you can use to accelerate your workflows in Adobe applications. You can use AI Assistant to better understand product knowledge, troubleshoot problems, or search through information and find operational insights. AI Assistant supports Experience Platform, Real-Time Customer Data Platform, Adobe Journey Optimizer and Customer Journey Analytics. You can use AI Assistant to access Experience Platform Agents and other AI capabilities.

For more information, read the [AI Assistant UI guide](ui-guide.md).

### Reasoning engine {#reasoning-angine}

The reasoning engine is the main decision-maker in Agent Orchestrator. It understands your goals, checks any limits or requirements, and creates step-by-step plans to help you reach your objectives. Unlike simple question-and-answer systems, it can adjust its plans as things change, and can go back and try different approaches if needed. The plans it creates are shown to you in the AI Assistant, so you can see and follow the process. 

### Adobe Experience Platform agents {#agents}

| Agent | Details |
| --- | --- |
| Audience Agent | Audience Agent lets you view insights about audiences, including detecting significant audience size changes, detecting duplicate audiences, explore your audience inventory, and retrieve your audiences' size. |
| Data Insights Agent | Data Insights Agent, accessible from the AI Assistant in Customer Journey Analytics, is a generative AI conversation agent that quickly and efficiently answers questions about your data. It builds relevant visualizations in Analysis Workspace using components from your data view and using your actual data. |
| Journey Agent | Journey Agent allows Journey Optimizer users to create, analyze, and optimize journeys using a natural language interface. With Journey Agent, you can quickly build journeys, detect and resolve schedule or audience conflicts, analyze performance and drop-off points, and identify top-performing journeys to replicate for future campaigns. It helps you make data-driven decisions, improve customer engagement, and streamline journey orchestration. |
| Product Support Agent | Product Support Agent is a self-serve debugging and troubleshooting capability that helps you troubleshoot Adobe Experience Platform features and applications without leaving your workflows. Support administrators can create customer support tickets with context from your AI Assistant interactions and you can check ticket updates through AI Assistant. |

### Knowledge base {#knowledge-base}

The knowledge base provides agents with secure access to customer business intelligence through structured and unstructured data sources, including Adobe product documentation, customer metadata about business objects, and analytics data.

## Access {#access}

AI Assistant requests are authenticated using the Adobe Identity Management Services. Authorizations are enforced by Adobe Experience Platform Access Control and Customer Journey Analytics Access Control.

To get access to the AI Assistant conversational interface and use one or more Experience Platform Agents, your Adobe administrator must grant you the relevant permissions in the Permissions UI or the Adobe Admin Console:

* **Real-Time CDP** and **Adobe Journey Optimizer**: Your administrator must grant you the **Enable AI Assistant** permission to enable you to access AI Assistant. Your administrator must also grant you the **View Operational Insights** permissions to allow you to ask operational insights questions in AI Assistant. Both permissions are set by the administrator in the Permissions UI.

* **Customer Journey Analytics**: Your administrator must grant you the permission to access AI Assistant through [Customer Journey Analytics Access Control](https://experienceleague.adobe.com/en/docs/analytics-platform/using/technotes/access-control). This allows you to ask product knowledge and data insights questions. 

>[!NOTE]
>
>Operational insights questions are not available for Customer Journey Analytics; therefore, no additional permissions apply.

* **Adobe Experience Manager**: Your administrator must grant you the permission to access AI Assistant through the [Adobe Admin Console](https://helpx.adobe.com/enterprise/using/admin-console.html).


