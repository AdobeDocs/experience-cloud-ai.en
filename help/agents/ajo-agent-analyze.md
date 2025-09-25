---
title: Journey Analyze Agent Skill Overview and User Guide
description: Comprehensive guide to the Journey Agent Analyze skill, enabling users to analyze marketing journeys, detect issues, uncover insights, and optimize customer engagement.
solution: Journey Optimizer
product: journey optimizer
role: Admin,User,Developer,Leader
---

# Journey Analyze Agent: Skill Overview and User Guide

## Overview

Journey Agent will enable Journey Optimizer users to analyze, and optimize journeys using a natural language interface. With Journey Agent, practitioners can quickly identify and resolve schedule and/or audience conflicts, detect points of user abandonment in a journey and provide insights or recommendations. It empowers practitionners to make data-driven decisions, improve customer engagement, and streamline journey orchestration.

>[!AVAILABILITY]
>
>The Journey Agent is available for all customers who have access to AI Assistant. However, you will need the following permissions in order to fully use the Journey Agent features.
>
>**View Journeys**: This permission lets you use the Journey Agent to view insights into the journey directly in AI Assistant.
>
>**Manage Journeys**: To permission lets you use the Journey Agent to create new journeys directly in AI Assistant.
>
>**View Segments**: This permission lets you use the Journey Agent to view insights into the audiences directly in AI Assistant.
>
>**Manage Segments**: To permission lets you use the Journey Agent to create new audiences directly in AI Assistant.

![Sample for AJO Agent](./images/ajo-agent/ajo-agent-sample.png)

## Use Cases

### Key Use Cases for Journey Agent Analyze

The Journey Agent Analyze skill offers a range of functionalities that can be leveraged to optimize marketing efforts:

1. **Journey Fallout Analysis**

   - Identify where and why customers drop off during a journey.
   - Detect patterns in customer behavior leading to disengagement.
   - Use insights to refine journey design and improve retention.

1. **Journey Audience Overlap Analysis**

   - Analyze audience overlap across multiple journeys.
   - Prevent audience fatigue caused by over-targeting.
   - Optimize segmentation to ensure balanced engagement.

1. **Journey Schedule Overlap Analysis**

   - Detect timing conflicts between scheduled journeys targeting the same audience.
   - Avoid over-communication and improve scheduling efficiency.
   - Maximize audience impact by ensuring journeys run at optimal times.

1. **Operational insights** 

   - Prompt-based Journey Insights – Surface operational insights about journeys , i.e. "show me all live journeys."

For each of these analyses, the agent not only detects issues but also provides **actionable recommendations to resolve them**.


## In Scope and Out of Scope Skills

### **In Scope**

The following capabilities are supported by Journey Agent Analyze:

- **Reactive Queries**: Allows users to ask specific questions about journey performance, audience usage, and scheduling conflicts.
- **Integration with Other Agents**: Collaborates with Audience Agent and Data Insights Agent for deeper analysis.
- **Agent response structuration**: reasoning (explain the logic), analysis summary (highlight key points), issue details (describe the problem), and recommendation (propose next steps).

### **Out of Scope**

The following functionalities are currently not supported:

- **Automated Journey Creation**
- **Real-Time Anomaly Detection**
- **Channels overlap**
- **Journey entry analysis**
- **Technical issue analysis**
- **Fatigue analysis**

## Sample Prompts / Example Prompts

### Common Prompts for Journey Analysis  

Here are examples of valuable prompts users can leverage to explore, monitor, and troubleshoot their journeys.

### Journey Lifecycle Questions

- "When was [Journey Name] published?"
- "When was [Journey Name] stopped?"
- "List all journeys currently in test mode"

### Journey Resource Questions

- "How many live journeys do I have?"
- "Give me a list of all scheduled recurring journeys and their expected run times."

### Audience and Journey Insights

- "Which audiences are used in more than X journeys?"
- "List all journeys using the [audience name] audience."

### Fallout analysis

- "I want to analyze the fallout by node for journey Fourth of July Campaign."
- "Perform a fallout analysis for journey Fourth of July Campaign."
- "What is profile loss over the course of journey Fourth of July Campaign?"
- "Show where users are dropping off in journey Fourth of July Campaign."

### Conflict Analysis Prompts 

Use these prompts to analyze potential conflicts between journeys, including scheduling and audience overlaps:

- "Can you do a comprehensive analysis of conflicts for our journey [Journey Name] with conflict type (scheduling/audience) information with live/running journeys?"
- "Please do a scheduling conflict analysis for journey [Journey Name] with conflict type information."
- "Please do an audience overlap analysis for journey [Journey Name] with conflict type information."
- "Are there any scheduling conflicts for journey [Journey Name]?"
- "Show me audience overlap conflicts for journey [Journey Name]."
- "Analyze all conflicts for journey [Journey Name] with other live journeys."
- "What are the current conflicts for journey [Journey Name]?"
- "Check if journey [Journey Name] has audience conflicts with other journeys."
- "Check for scheduling conflicts involving journey [Journey Name]."
- "I want to know about all journey conflicts for [Journey Name]."
- "Do any live journeys conflict with [Journey Name] by schedule or audience?"
- "Identify conflict types for journey [Journey Name] compared to running journeys."
- "Show overlapping audiences for journey [Journey Name] and other journeys."
- "Highlight scheduling overlaps between journey [Journey Name] and live journeys."
- "Is journey [Journey Name] running in conflict with any other journey?"
- "Please detect and list conflicts for [Journey Name]."
- "Report all types of conflicts for journey [Journey Name]."
- "Give me a conflict breakdown (scheduling and audience) for [Journey Name]."
- "Does [Journey Name] have any conflicts that may impact performance?"
- "Are there any active conflicts affecting [Journey Name]?"
- "List journeys in conflict with [Journey Name] by schedule or audience."
- "Has journey [Journey Name] triggered any conflict alerts?"
- "Find potential audience conflicts for journey [Journey Name]."
- "Analyze conflict risk for journey [Journey Name]."
- "Provide conflict diagnostics for [Journey Name]."

## Best Practices

### Prompting Best Practices

To maximize the effectiveness of Journey Agent Analyze, follow these best practices:

1. **Be Specific**: Use clear and concise prompts to get targeted insights. For example, instead of asking "What are my journeys?", specify "List all journeys created in the last month."
1. **Combine Insights**: Integrate insights from Audience Agent and Data Insights Agent for a holistic view of journey performance.
1. **Iterative Refinement**: Use fallout and overlap analysis to iteratively refine journey design and scheduling.

### Setup Best Practices

- **Define Clear Objectives**: Before analyzing journeys, establish clear goals (e.g., improving retention, increasing conversions).
- **Monitor Regularly**: Schedule regular reviews of journey performance to identify trends and anomalies.
- **Optimize Segmentation**: Ensure audience segmentation is balanced to avoid fatigue and maximize engagement.
