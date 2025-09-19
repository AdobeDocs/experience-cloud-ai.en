---
title: Audience Agent
description: Learn how to use the Audience Agent to create audiences, view audience changes, detect duplicate audiences, and view audience insights.
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

- Detect significant changes in audience size
- Detect duplicate audiences
- Find audiences based on full or partial attributes named
- Find the size of your audiences
- Discover XDM fields you can use to define an audience

The Audience Agent currently does **not** support the following features:

- Knowledge-based audience creation
  - Knowledge-based audience creation is creating an audience based on the given attributes and events
  - Support for this feature is coming soon
- Goal-based audience exploration
  - Goal-based audience exploration is creating a propensity model that 
- Estimate the size of an audience to support audience creation


Additionally, when using Audience Agent, you should keep the following constraints in mind:

- Audience Agent needs at least 24 hours to process your data
  - For example, you **cannot** have a query that looks for data within the last 24 hours. You'll need to look within the last 48 hours, at a minimum.
- Audience Agent only supports **people** based audiences that are created in Segment Builder

## Sample prompts

The following examples demonstrate sample prompts and responses for the Audience Agent.

### Conversation audience exploration

Show me fields for affluent buyers.

+++ Response

![](./images/audience/affluent-buyers.png)

+++

Which audiences have not been activated or used in any campaign in the last 30 days?

+++ Response

![](./images/audience/not-activated.png)

+++

List all the audiences that have been mapped to new destinations in the last 3 months.

+++ Response

![](./images/audience/new-destination.png)

+++

### Detect duplicate audiences

Do I have any audiences with identical or similar descriptions?

+++ Response

![](./images/audience/similar-descriptions.png)

+++

Identify audiences that have the same rules but have different names.

+++ Response

![](./images/audience/same-rules-different-names.png)

+++

Show me all the audiences that have the same rules but different activation destinations.

+++ Response

![](./images/audience/same-rules-different-destinations.png)

+++

### Retrieve audience size

What is the current size of my audience "Gold-star Members in California_f153e1"?

+++ Response

![](./images/audience/current-size.png)

+++

What is my biggest audience?

+++ Response

![](./images/audience/largest-audience.png)

+++

### Detect significant changes in audience size

Which audiences have increased in size by more than 20% in the last week?

+++ Response

![](./images/audience/increase-past-week.png)

+++

Which audiences have decreased in size by more than 15% in the last month?

+++ Response

![](./images/audience/decrease-month.png)

+++

What is my fastest growing audience?

+++ Response

![](./images/audience/fastest-growing.png)

+++

## Next steps

After reading this guide, you should have a better understanding of Audience Agent and what features it supports. For more information on agents in Adobe Experience Platform, read the [Agent Orchestrator overview](./agent-orchestrator.md).
