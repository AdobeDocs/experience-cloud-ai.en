---
title: AI in Experience Cloud Applications
description: Learn how Experience Cloud applications use generative AI (GenAI), AI Assistant, and agentic AI.
---
# AI in Experience Cloud

Welcome to the comprehensive guide for AI capabilities across Adobe Experience Cloud applications. This documentation covers how generative AI, AI Assistant, and Adobe agents are integrated into your Experience Cloud workflows to accelerate productivity and enhance decision-making.

## What's included in this guide

### AI Assistant

[AI Assistant](./ai-assistant/ai-assistant-ui.md) is an intelligent conversational, generative AI tool that will boost productivity and redefine work in Adobe Experience Platform-based Applications. Users can gain product knowledge, troubleshoot problems, and find operational insights through natural language prompts. You can also use AI Assistant to access Adobe Experience Platform Agents and other AI capabilities.

**Key features:**

- **Conversational Interface**: You can choose between a full-screen and a rail view interface to suit your workflow preferences.
- **Discovery Prompts**: AI Assistant provides pre-configured prompts that are organized by categories such as Learn, Analyze, and Optimize.
- **Context Setting**: You are able to configure the application, sandbox, and dataview settings to receive responses that are tailored to your needs.
- **Data Visualization**: The tool delivers interactive charts and graphs, enabling you to gain insights from your data.
- **Response Verification**: All responses include source citations, explanations of AI reasoning, and mechanisms for providing feedback.


### Agent Orchestrator

[Adobe Experience Platform Agent Orchestrator](./agents/agent-orchestrator.md) is the new agentic layer in Adobe Experience Platform. Designed to leverage the platform's rich data and customer knowledge, Experience Platform Agent Orchestrator powers the intelligence and reasoning behind purpose-built expert Adobe Experience Platform Agents, enabling them to execute complex decision-making and problem-solving tasks at speed and scale — all with human oversight. When you ask questions or request help via natural language in a conversational interface like AI Assistant, Agent Orchestrator automatically calls upon specialized agents to get you the right answers. Agent Orchestrator remembers your conversation history, enabling you to build on previous questions naturally without repeating context, and combines insights from multiple agents to present you with clear, unified responses.

**Core components:**

- **Reasoning Engine**: Creates step-by-step plans and adjusts approaches as needed
- **Specialized Agents**: Purpose-built agents for specific tasks and domains
- **Knowledge Base**: Secure access to business intelligence and documentation

### Specialized Agents

#### Audience Agent

The Audience Agent provides insights about audiences including:

- Detecting significant audience size changes.
- Identifying duplicate audiences.
- Exploring audience inventory.
- Retrieving audience sizes.

Read the [Audience Agent documentation](./agents/audience.md) for more information.

#### Data Insights Agent

Available in Customer Journey Analytics, the Data Insights Agent:

- Answers questions about your data using natural language.
- Builds relevant visualizations in Analysis Workspace.
- Uses components from your dataview and actual data.

#### Journey Analyze Agent

The Journey Analyze Agent enables the Adobe Journey Optimizer users to:

- Analyze, and optimize journeys using natural language.
- Detect and resolve schedule or audience conflicts.
- Analyze performance and drop-off points.

Read the [Journey Agent documentation](./agents/ajo-agent.md) for more information.

#### Product Support Agent

Use the Product Support Agent for self-serve debugging and troubleshooting:

- Troubleshoot Adobe Experience Platform features without leaving workflows.
- Create support tickets with context from AI Assistant interactions.
- Check ticket updates through AI Assistant.

Read the [Product Support Agent documentation](./agents/product-support.md) for more information.

## Getting started

### Access requirements

To use AI Assistant and Experience Platform Agents, your Adobe Admin needs to set up the appropriate permissions:

- To use AI Assistant within Real-Time CDP and Adobe Journey Optimizer, you need the "Enable AI Assistant" permission, as well as the "View Operational Insights" permission to access operational questions.
- Access to AI Assistant in Customer Journey Analytics is managed through Customer Journey Analytics Access Control, which allows you to ask both product knowledge and data insights questions.
- For Adobe Experience Manager, you can access AI Assistant through permissions set in the Adobe Admin Console.

### Privacy and security

AI Assistant is built with privacy, security, and governance at the forefront:

- No personal data is used for training.
- All existing access control policies are honored.
- HIPAA-ready when used with Adobe Experience Platform Healthcare Shield.
- 30-day retention policy for interaction logs.
- Sandbox-specific data isolation.

## Best practices

To get the most value from your AI Assistant experience, follow these best practices:

- **Be specific** in your prompts to obtain targeted and relevant insights from the AI Assistant.
- **Verify responses** by reviewing the source citations and the reasoning explanations provided by the AI Assistant.
- **Use context setting** to make sure that the most relevant data sources are used for your questions.
- **Provide feedback** to help improve the performance and accuracy of the AI Assistant over time.
- **Combine insights** from multiple agents to achieve a more comprehensive and well-rounded analysis.

## Legal considerations

When using AI Assistant, it is important to be aware of key legal and practical considerations. Currently, AI Assistant supports responses in English only. Always take care to verify the information provided, as language models may occasionally make mistakes. Make use of the reasoning steps and explanations included in the responses to better understand the answers you receive. If you encounter any issues or inaccuracies, please submit feedback to help improve the AI Assistant over time.
