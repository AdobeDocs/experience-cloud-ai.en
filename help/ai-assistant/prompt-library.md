---
title: AI Assistant Prompt Library
description: Learn about the different kinds of prompts and prompt patterns that you can use when querying AI Assistant.
TQID: https://experienceleague.adobe.com/QICjh9cNBT3XeKObkXqSDEGQT26zpv86V36L0tqvSgo
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: Experience Cloud
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
---
# AI Assistant Prompt Library

Read this guide for different types of prompts that you can use on AI Assistant.

## Audience Agent

The following sections provide example prompts you can use with the Audience Agent to explore and analyze your audiences. These include ways to investigate audience characteristics, detect duplicate audiences, retrieve audience sizes, and monitor significant changes in audience size over time. Use these prompts to gain deeper insights and maintain the quality of your audience data.

### Conversation audience exploration

- "Show me fields for affluent buyers."
- "Which audiences have not been activated or used in any campaign in the last 30 days?"
- "List all the audiences that have been mapped to new destinations in the last 3 months."

### Detect duplicate audiences

- "Do I have any audiences with identical or similar descriptions?"
- "Identify audiences that have the same rules but have different names."
- "Show me all the audiences that have the same rules but different activation destinations."

### Retrieve audience size

- "What is the current size of my audience "Gold-star Members in California_f153e1"?"
- "What is my biggest audience?"

### Detect significant changes in audience size

- "Which audiences have increased in size by more than 20% in the last week?"
- "Which audiences have decreased in size by more than 15% in the last month?"
- "What is my fastest growing audience?"

## Data Insights Agent

The following example prompts can be used with the Data Insights Agent to analyze your data, identify trends, and uncover actionable insights.

### Data visualization

- "Show me profits in September."
- "Trend orders in September."
- "Show revenue by region in September."
- "Share of revenue by product category."
- "Orders by day of week, from January to May."
- "Show orders by gender, from March to June."
- "What is the profit across SKUs from February to May."
- "Revenue by store name in September."
- "What were my top 10 SKUs by profit in September?"
- "Proportion of purchases by month of year."
- "Total profit in September."

## Journey Agent

The following example prompts can be used with the Journey Agent to help you analyze journey lifecycles, manage journey resources, gain insights into audience and journey relationships, and detect conflicts between journeys. Use these prompts to optimize your journey orchestration and resolve issues efficiently.

### Journey Lifecycle Questions

- "When was {JOURNEY_NAME} published?"
- "When was {JOURNEY_NAME} stopped?"
- "List all journeys currently in test mode"

### Journey Resource Questions

- "How many live journeys do I have?"
- "Give me a list of all scheduled recurring journeys and their expected run times."

### Audience and Journey Insights

- "Which audiences are used in more than X journeys?"
- "List all journeys using the {AUDIENCE_NAME} audience."

### Conflict Analysis Prompts 

Use these prompts to analyze potential conflicts between journeys, including scheduling and audience overlaps:

+++Select to view list

- "Can you do a comprehensive analysis of conflicts for our journey {JOURNEY_NAME} with conflict type (scheduling/audience) information with live/running journeys?"
- "Please do a scheduling conflict analysis for journey {JOURNEY_NAME} with conflict type information."
- "Please do an audience overlap analysis for journey {JOURNEY_NAME} with conflict type information."
- "Are there any scheduling conflicts for journey {JOURNEY_NAME}?"
- "Show me audience overlap conflicts for journey {JOURNEY_NAME}."
- "Analyze all conflicts for journey {JOURNEY_NAME} with other live journeys."
- "What are the current conflicts for journey {JOURNEY_NAME}?"
- "Check if journey {JOURNEY_NAME} has audience conflicts with other journeys."
- "Check for scheduling conflicts involving journey {JOURNEY_NAME}."
- "I want to know about all journey conflicts for {JOURNEY_NAME}."
- "Do any live journeys conflict with {JOURNEY_NAME} by schedule or audience?"
- "Identify conflict types for journey {JOURNEY_NAME} compared to running journeys."
- "Show overlapping audiences for journey {JOURNEY_NAME} and other journeys."
- "Highlight scheduling overlaps between journey {JOURNEY_NAME} and live journeys."
- "Is journey {JOURNEY_NAME} running in conflict with any other journey?"
- "Please detect and list conflicts for {JOURNEY_NAME}."
- "Report all types of conflicts for journey {JOURNEY_NAME}."
- "Give me a conflict breakdown (scheduling and audience) for {JOURNEY_NAME}."
- "Does {JOURNEY_NAME} have any conflicts that may impact performance?"
- "Are there any active conflicts affecting {JOURNEY_NAME}?"
- "List journeys in conflict with {JOURNEY_NAME} by schedule or audience."
- "Has journey {JOURNEY_NAME} triggered any conflict alerts?"
- "Find potential audience conflicts for journey {JOURNEY_NAME}."
- "Analyze conflict risk for journey {JOURNEY_NAME}."
- "Provide conflict diagnostics for {JOURNEY_NAME}."

+++

## Product Support Agent

The Product Support Agent helps you troubleshoot issues, create support cases, and track the status of your support tickets. Use the following example prompts to get assistance.

### Troubleshooting help

- "Why does my profile count differ on the License Usage Dashboard and the Experience Platform home page?"
- "What are the reasons for a journey not triggering?"
- "How does Adobe Experience Platform create real-time experiences?"
- "How do you configure and use alerts in Adobe Experience Platform?"
- "What is the limit for batch segmentation jobs in Adobe Experience Platform Activation?"
- "What is the average profile richness limit in Adobe Experience Platform Activation?"

### Support case creation

- "Create a support ticket."
- "Can you help me create a support ticket?"

### Track case progress

- "What is the latest on my case E-12345?"
- "What's the update on ticket E-67890?"

