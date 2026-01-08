---
title: Journey Create Agent Skill Overview
description: Learn how to use the Journey Agent Create skill to build marketing journeys through natural language prompts in Journey Optimizer.
solution: Journey Optimizer
product: journey optimizer
role: Admin,User,Developer
feature: AI Assistant
topic: Administration
level: Beginner
---

# Journey Create Agent: Skill overview and user guide

## Overview

Journey Create Agent enables Journey Optimizer users to build and configure marketing journeys using a natural language interface. With Journey Create Agent, practitioners can quickly create journeys by describing their requirements in conversational prompts. The agent streamlines journey creation, allowing marketers to focus on strategy rather than technical configuration.

>[!AVAILABILITY]
>
>The Journey Create Agent is available for all customers who have access to AI Assistant. However, you will need the following permissions in order to fully use the Journey Create Agent features:
>
>**Manage Journeys**: This permission lets you create new journeys directly in AI Assistant.
>
>**View Journey Events, Data Sources and Actions**: This permission ensures that the AI Assistant can search through Journey Events and Custom Actions. 
>
>**View Segments**: This permission ensures that AI Assistant can search for audience segments when creating a Journey.
>
>**Manage Segments**: This permission lets you create new audiences directly in AI Assistant.

## Use cases

### Key use cases for Journey Create Agent

The Journey Create Agent skill offers capabilities that can be leveraged to accelerate marketing execution:

1. **Event-triggered journey creation**

   - Create journeys that activate based on specific customer events.
   - Design automated responses to customer actions in real-time.
   - Build personalized communication flows based on customer behavior.

1. **Audience-targeted journey creation**

   - Build journeys targeting specific audience segments.
   - Design multi-step communication sequences with strategic timing.

1. **Business-event triggered journey creation** 

   - Create journeys that activate based on a particular business event and target a specified audience (e.g. product back in stock or game score change)
   - Build personalized communication flows based on customer behavior.

1. **Audience qualification journey creation** 

   - Create journeys that activate as profiles enter or exit an audience segment definition.
   - Build personalized communication flows based on customer behavior.  

1. **Conditional journey flows**

   - Create decision branches based on customer attributes.
   - Design split paths that adapt to customer preferences.

For each of these use cases, the agent translates natural language requirements into structured journey configurations.

## In scope and out of scope skills

### **In scope**

The following capabilities are supported by Journey Create Agent:

- **Natural language journey creation**: Allows users to describe journey flow in conversational language.
- **Event-based and audience-based journeys**: Supports both trigger-based and scheduled journey types, also business event and audience qualification.
- **Conditional logic**: Handles decision splits and branching based on customer attributes.
- **Multi-channel messaging**: Supports push notifications, email, and SMS channels.
- **Journey scheduling**: Configures start dates and timing for scheduled journeys.

### **Out of scope**

The following functionalities are currently not supported:

- **Advanced journey analytics**
- **Real-time journey modifications**
- **Cross-journey orchestration**
- **A/B testing configuration**
- **Complex data transformations**
- **Content message creation**

## Sample prompts

### Common prompts for journey creation

Here are examples of valuable prompts users can leverage to create journeys.

### Event-triggered journey prompts

**Store visit journey:**

“Create a journey that starts when a user enters my store location. Send a push notification to welcome users to the store. Wait 2 days and check to see if the user has a valid email address. If the user has a valid email address, send an email survey to ask about their store experience. If the user does not have a valid email address, send a push notification to prompt for registration.”

**Post-purchase journey:**

"Create a journey that starts when a customer makes a purchase online. Send a push notification to thank them for their purchase. Next, check to see if they are loyalty members. If the user is a loyalty rewards member, send a second push notification with a 10% discount code. If the user is not a loyalty rewards member, send a push inviting them to sign up for the loyalty program. Wait 2 days and send a follow-up push with a survey about their purchase experience."

**Event-based promotion:**

"Create a journey triggered when the game score reaches 50. Send an SMS message to loyalty reward members saying that they are eligible for a free slice of pizza from the partner sponsor."

### Audience-targeted journey prompts

**Seasonal campaign:**

"I want to create a journey targeting an audience of day hikers. I want to send an email alerting this audience to my upcoming holiday sale that includes a variety of hiking essentials. Wait 3 days after sending the first email and send a second email that has a 15% coupon with free shipping. Wait 1 week and then send a 3rd email message to show our new sleeping bag and tent collection. Schedule the journey to start on 12/20."

**Loyalty appreciation:**

"Build a loyalty appreciation journey for SUV owners, including a thank you push notification with a free carwash offer and a follow-up push notification reminder if the first notification is not interacted with within 1 day."

### Open-ended prompts

For users starting without a specific journey in mind:

- "I'd like to create a journey"
- "Help me create a journey"
- "Create me a journey"

The agent will provide guidance and examples to help you define your journey requirements.

## Best practices

### Prompting best practices

To maximize the effectiveness of Journey Create Agent, follow these best practices:

1. **Be Specific**: Provide clear details about your journey goals, target audience, and desired actions. Include information about channels, timing, and conditions.
1. **Specify Timing**: Clearly indicate wait periods between actions and when the journey should start.
1. **Define Conditions**: When using conditional logic, explain the criteria for each branch path.
1. **Include Channels**: Specify which communication channels you want to use (push, email, SMS).
1. **Mention Scheduling**: For scheduled journeys, provide the desired start date and time.
1. **Custom Actions**: If you are using custom actions in your workflow you need to specify that you are using a custom action along with the exact name of the custom action. Example: 
   When a user enters my store location send a welcome message using custom action ExternalPush. Wait 2 days and then send a follow up message using custom action ExternalEmail with a survey on their visit.
1. **Validate Expressions**: Make sure to check and validate any expressions that Journey Agent creates to ensure that the correct fields and values are used. 

### Setup best practices

- **Define Clear Objectives**: Before creating journeys, establish clear goals (improving retention, driving conversions, increasing engagement).
- **Prepare Audiences**: Ensure your target audiences are already created and properly segmented.
- **Plan Message Content**: Have your messaging strategy defined before journey creation.
- **Consider Customer Experience**: Design journey flows that respect customer preferences and avoid over-communication.

