---
title: Audience Agent
description: Learn how to use AI Assistant to create audiences, view audience changes, detect duplicate audiences, and view audience insights.
---

# Audience Agent

>[!AVAILABILITY]
>
>The Audience Agent is available for all customers who have access to AI Assistant. However, you will need the following permissions in order to fully use the Audience Agent features.
>
>**View Segments**: This permission lets you use the Audience Agent to view insights into the audiences directly in AI Assistant.
>**Manage Segments**: To permission lets you use the Audience Agent to create new audiences directly in AI Assistant.

The Audience Agent lets you view insights about audiences, including detecting significant audience size changes, detecting duplicate audiences, exploring your audience inventory, and retrieving your audiences' size.

## Supported use cases

The Audience Agent within AI Assistant supports the following use cases:

- Estimate the size of an audience during creation
- Detect significant changes in audience size
- Detect duplicate audiences
- Find audiences based on full or partial attributes named
- Find the size of your audiences

The Audience Agent currently does **not** support the following features:

- Knowledge-based audience creation
  - Knowledge-based audience creation is creating an audience based on the given attributes and events
  - Support for this feature is coming soon
- Goal-based audience creation
  - Goal-based audience creation is creating an audience based off of another already existing audience

Additionally, when using Audience Agent, you should keep the following constraints in mind:

- Audience Agent needs at least 24 hours to process your data
  - For example, you **cannot** have a query that looks for data within the last 24 hours. You'll need to look within the last 48 hours, at a minimum.

## Sample prompts

The following examples demonstrate sample prompts and responses for the Audience Agent.

### Conversation audience exploration

What are the top 5 cities where my profiles live?

+++ Response

not working atm

+++

Which audiences have not been activated or used in any campaign in the last 30 days?

+++ Response

working

+++

List all the audiences that have been mapped to new destinations in the last 3 days.

+++ Response

working

+++

### Detect duplicate audiences

Do I have any audiences with identical or similar descriptions?

+++ Response

working

+++

Identify audiences that have the same rules but have different names.

+++ Response

working

+++

Show me all the audiences that have the same rules but different activation destinations.

+++ Response

working

+++

### Retrieve audience size

What is the current size of my audience {NAME}?

+++ Response

working

+++

What would the size of an audience targeting users who visited our pricing page at least twice in the past week but haven't converted be?

+++ Response

not working

+++

What is my biggest audience?

+++ Response

working

+++

### Detect significant changes in audience size

Which audiences have increased in size by more than 20% in the last week?

+++ Response

working but need better data

+++

Which audiences have decreased in size by more than 15% in the last month?

+++ Response

working but need better data

+++

Which audiences have dropped to zero at least once in the last week?

+++ Response

working but need better data

+++

What are my fastest growing audiences?

+++ Response

+++

## Next steps

After reading this guide, you should have a better understanding of Audience Agent and what features it supports. For more information on agents in Adobe Experience Platform, read the [Agent Orchestrator overview](./agent-orchestrator.md).