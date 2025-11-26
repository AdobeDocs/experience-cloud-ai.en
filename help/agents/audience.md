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
>
>**Manage Segments**: To permission lets you use the Audience Agent to create new audiences directly in AI Assistant.

The Audience Agent lets you view insights about audiences, including detecting significant audience size changes, detecting duplicate audiences, exploring your audience inventory, and retrieving your audiences' size.

>[!SLIDE](audience-agent-overview)

## Supported use cases

The Audience Agent within AI Assistant supports the following use cases:

- Conversationally explore your audience
  - Find audience sizes of existing audiences
  - Look for audiences based on full or partial attributes named
  - Detect duplicate audiences
  - Discover XDM fields you can use to define an audience
- Detect significant changes in audience size
  - This lets you find audiences that have suddenly grown or shrunk, letting you better analyze potential market changes
- Audience creation 
    - This skill lets you create an audience based on the given attributes and events
    - Additionally, this skill lets you estimate the potential size of an audience prior to creating the audience, letting you quickly iterate on the most effective audience before it's ready to activate

<!-- - Find your audience size and detect significant changes in audience size
  - This lets you find audiences that have suddenly grown or shrunk, letting you better analyze potential market changes
- Detect duplicate audiences
  - This lets you reduce redundancies with your created audiences
- Find audiences based on full or partial attributes named
  - This lets you more easily navigate through your audience inventory
- Discover XDM fields you can use to define an audience
  - This skill lets you more easily identify the right fields to use in your audience based on context and relevance -->

The Audience Agent does not **currently** support the following feature:

- Goal-based audience exploration
  - Goal-based audience exploration lets you discover relevant datasets and profiles aligned to a business goal by applying machine learning models such as propensity to buy or convert.

Additionally, when using Audience Agent, you should keep the following constraints in mind:

- Audience Agent needs at least 24 hours to process your data
  - For example, you **cannot** have a query that looks for data within the last 24 hours. You'll need to look within the last 48 hours, at a minimum.
- Audience Agent only supports the following audience types:
    - **People-based** audiences that are evaluated using batch segmentation
    - **Account-based** audiences for the following use cases:
      - Conversational audience exploration
      - Duplicate audience detection

## Sample prompts

The following examples demonstrate sample prompts and responses for the Audience Agent.

### Conversational audience exploration

Show me fields for affluent buyers.

+++ Response

![The AI Assistant shows a table displaying fields that are relevant to affluent buyers.](./images/audience/affluent-buyers.png)

+++

Which audiences have not been activated or used in any campaign in the last 30 days?

+++ Response

![The AI Assistant shows a table that displays audiences that haven't been activated or used in campaigns in the last 30 days.](./images/audience/not-activated.png)

+++

List all the audiences that have been mapped to new destinations in the last 3 months.

+++ Response

![The AI Assistant lists the one audience that has been mapped to a new destination in the last 3 months.](./images/audience/new-destination.png)

+++

Which account audience has the largest audience size and what is that size?

+++ Response

![The AI Assistant shows a table that displays the largest account audiences.](./images/audience/largest-account-audience.png)

+++

### Detect duplicate audiences

Do I have any audiences with identical or similar descriptions?

+++ Response

![The AI Assistant displays a table that contains the segment definition and the names of the audiences with the same segment definitions.](./images/audience/similar-descriptions.png)

+++

Identify audiences that have the same rules but have different names.

+++ Response

![The AI Assistant displays a table that contains the names of audiences that share the same audience rules.](./images/audience/same-rules-different-names.png)

+++

Show me all the audiences that have the same rules but different activation destinations.

+++ Response

![The AI Assistant shows that there are no duplicate segment definitions to different destinations.](./images/audience/same-rules-different-destinations.png)

+++

Identify account audiences that have the same rules but have different names.

+++ Response

![The AI Assistant displays a table that contains the names and IDs of account audiences that share the same audience rules.](./images/audience/duplicate-account-audience.png)

+++

### Retrieve audience size

What is the current size of my audience "Gold-star Members in California_f153e1"?

+++ Response

![The AI Assistant states the current size of the audience that was asked about.](./images/audience/current-size.png)

+++

What is my biggest audience?

+++ Response

![The AI Assistant gives information about the audience with the most profiles, including name and audience ID.](./images/audience/largest-audience.png)

+++

### Detect significant changes in audience size

Which audiences have increased in size by more than 20% in the last week?

+++ Response

![The AI Assistant displays a table that lists the names of all the audiences that match the query. It also shows the percentage increase, the current audience size, as well as the former audience size.](./images/audience/increase-past-week.png)

+++

Which audiences have decreased in size by more than 10% in the last month?

+++ Response

![The AI Assistant displays a table that lists the names of all the audiences that match the query. It also shows the current audience size, the former audience size, as well as the date of the old audience size.](./images/audience/decrease-month.png)

+++

What is my fastest growing audience?

+++ Response

![The AI Assistant states the name of the fastest growing audience, as well as the current size and the percentage of growth.](./images/audience/fastest-growing.png)

+++

### Create an audience

When you create an audience with Audience Agent, AI Assistant will guide you through a plan. For example, you can ask to "Create an audience made up of men who live in California". AI Assistant then lists the plan that it will undertake to create the audience.

+++ Response

![The AI Assistant shows the plan to create an audience.](./images/audience/audience-create-plan.png)

+++

This plan is made up of three steps:

1. [Identify audience characteristics](#identify)
2. [Estimate audience size](#estimate)
3. [Create and persist a new audience](#create)

#### Identify audience characteristics {#identify}

![Step 1 of the plan, which is to identify audience characteristics.](./images/audience/plan-step-1.png)

After accepting the plan, AI Assistant will grab the audience's characteristics based off of your initial query.

+++ Response

![The audience definition based off of the user query.](./images/audience/audience-create-definition.png)

+++

If the AI Assistant's audience definition is correct, you can approve and move on to the next step.

#### Estimate audience size {#estimate}

![Step 2 of the plan, which is to estimate the size of the potential audience.](./images/audience/plan-step-2.png)

After approving the identified audience characteristics, AI Assistant will estimate the size of the potential audience and the audience definition details. 

+++ Response

![The sample estimate for the potential audience is displayed. The estimated size and the segment definition are shown.](./images/audience/audience-create-estimate.png)

+++

If the estimated size looks correct, you can approve and move on to the next step.

#### Create and persist new audience {#create}

![Step 3 of the plan, which is to finish creating the audience.](./images/audience/plan-step-3.png)

Finally, if the characteristics and the audience size look correct, you can approve or reject the audience's creation.

+++ Response

First, you can review the proposed audience through the provided data grid.

![The review screen is displayed.](./images/audience/audience-create-review.png)

If the audience looks correct, you can accept the proposal by selecting **[!UICONTROL Create]** to finish creating the audience.

![The complete proposal for the audience is displayed.](./images/audience/audience-create-proposal.png)

+++

The audience is now created.

![The audience proposal was accepted, and the audience was created.](./images/audience/audience-finish-create.png)

## Next steps

After reading this guide, you should have a better understanding of Audience Agent and what features it supports. For more information on agents in Adobe Experience Platform, read the [Agent Orchestrator overview](./agent-orchestrator.md).

