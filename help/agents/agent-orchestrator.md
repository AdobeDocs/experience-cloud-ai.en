---
title: Adobe Experience Platform Agent Orchestrator
description: Learn about Adobe Experience Platform Agent Orchestrator.
---
# Adobe Experience Platform Agent Orchestrator

Adobe Experience Platform Agent Orchestrator is the new agentic layer in Adobe Experience Platform. Designed to leverage Experience Platform's rich data and customer knowledge, Experience Platform Agent Orchestrator powers the intelligence and reasoning behind purpose-built expert Adobe Experience Platform Agents, enabling them to execute complex decision-making and problem-solving tasks at speed and scale — all with human oversight. When you ask questions or request help via natural language in a conversational interface like AI Assistant, Agent Orchestrator automatically calls upon specialized agents to get you the right answers. Agent Orchestrator remembers your conversation history, enabling you to build on previous questions naturally without repeating context, and combines insights from multiple agents to present you with clear, unified responses.

You can complete complex end-to-end workflows through an intuitive conversational interface without needing to know which agents are working behind the scenes. The system understands your goals, creates step-by-step plans, and adjusts its approach as needed based on your feedback. Within your conversation in AI Assistant, you can explore the Agent Orchestrator reasoning panel to see the step-by-step thinking process and better understand how your requests are being handled.

>[!SLIDE](agent-orchestrator-overview)

Read this document to learn about Agent Orchestrator.

## Components of Agent Orchestrator {#components}

Agent Orchestrator is made up of several key components, including the AI Assistant conversational interface, a reasoning engine for decision-making and planning, specialized Adobe Experience Platform agents, and a knowledge base that provides access to relevant information.

![The marketing architecture of Agent Orchestrator.](./images/agent-orchestrator/agentic-architecture.png)

### AI Assistant conversational interface {#ai-assistant}

AI Assistant is an intelligent, natural language conversational experience that lets practitioners using enabled Experience Cloud applications to leverage GenAI and Agentic AI capabilities, the breadth of which depends on the Experience Cloud applications licensed by customers. To unlock access, read [the guide on accessing AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/access).

For more information, read the [AI Assistant UI guide](../ai-assistant/ai-assistant-ui.md).

### Reasoning engine {#reasoning-engine}

Reasoning engine interprets your goals based on your natural language prompts, checks any limits or requirements, and creates step-by-step plans to help you reach your objectives. Unlike simple question-and-answer systems, it can adjust its plans as things change, and can go back and try different approaches if needed. The plans it creates are shown to you in the AI Assistant conversational interface, so you can see and follow the process, as well as intervene if needed.

### Adobe Experience Platform Agents {#agents}

Adobe Experience Platform Agents are purpose-built grouping of AI agents skilled in delivering common jobs across customer experience domains. Below is the list of Adobe Experience Platform Agents that are currently available in Experience Cloud applications:

| Agent | Details | Supported applications |
| --- | --- | --- |
| [Audience Agent](audience.md) | Audience Agent lets you view insights about audiences, including detecting significant audience size changes, detecting duplicate audiences, explore your audience inventory, and retrieve your audiences' size. | <ul><li>Real-Time CDP</li><li>Adobe Journey Optimizer</li></ul> |
| [Data Insights Agent](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai) | Data Insights Agent, accessible from the AI Assistant in Customer Journey Analytics, is a generative AI conversation agent that quickly and efficiently answers questions about your data. It builds relevant visualizations in Analysis Workspace using components from your data view and using your actual data. | Customer Journey Analytics |
| [Experimentation Agent](./agent-experiment.md) | Experimentation Agent helps teams learn faster by analyzing experiment results, predicting impact, and proposing new experiments. It centralizes past and active experiments so you can build on what you've already learned, spot gaps, and prioritize what to test next. | Adobe Journey Optimizer Experimentation Accelerator |
| [Journey Agent](./ajo-agent-analyze.md) | Journey Agent allows Adobe Journey Optimizer users to create, analyze, and optimize journeys using a natural language interface. With Journey Agent, you can quickly build journeys, detect and resolve schedule or audience conflicts, analyze performance and drop-off points, and identify top-performing journeys to replicate for future campaigns. It helps you make data-driven decisions, improve customer engagement, and streamline journey orchestration. | Adobe Journey Optimizer |
| [Product Support Agent](product-support.md) | Product Support Agent is a self-serve debugging and troubleshooting capability that helps you troubleshoot Adobe Experience Platform features and applications without leaving your workflows. Support administrators can create customer support tickets with context from your AI Assistant interactions and you can check ticket updates through AI Assistant. | <ul><li>Adobe Experience Platform</li><li>Real-Time CDP</li><li>Adobe Journey Optimizer</li><li>Adobe Journey Optimizer B2B Edition</li><li>Customer Journey Analytics</li><li>Adobe Experience Manager</li></ul> |

For further information around availability of Agents in Experience Cloud applications, please review the [Agentic AI in Experience Cloud documentation](https://experienceleague.adobe.com/en/docs/core-services/interface/features/agentic-ai).

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

