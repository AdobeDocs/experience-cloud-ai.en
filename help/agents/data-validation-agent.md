---
title: Data Validation Agent
description: Learn how to use the Data Validation Agent to validate your data.
---
# Data Validation Agent

The Data Validation Agent is an AI-powered service that you can use on Adobe Experience Platform AI Assistant to perform statistical and semantical validations on Experience Platform datasets. You can use the Data Validation Agent to analyze dataset fields, identify data quality issues, and retrieve natural language summaries with actionable insights. This agent is designed for data engineers, analysts, and data stewards who are looking to execute rapid data quality assessments without writing SQL queries or navigating complex schema hierarchies.

With the Data Validation Agent, you can:

- Fill the essential gaps in both the onboarding process and the day-to-day diagnostics.
- Reduce manual QA on your datasets.
- Accelerate time-to-value for your customers.

Read this documentation for comprehensive information on the Data Validation Agent.

<!-- The functionalities introduced by the agent will be available to customers as part of the "Data Engineering Agent" offering, so I believe all information should be included under that particular agent, as DVA will not be directly marketed towards users. -->

## Understanding the Data Validation Agent

The Data Validation Agent has two main validation functionalities:

- Field validation
- Dataset validation

>[!BEGINTABS]

>[!TAB Field validation]

>[!TAB Dataset validation]

>[!ENDTABS]

The agent provides two main validation functionalities:

- Field validation: validates one specific field in a dataset.
  - The validation skill provides:
    - Null count and unique value count
    - Top unique values and their frequency
    - AI-assisted invalid value detection (we call this "semantic" validation - based on the available metadata, e.g. field name, field description, field type, and the actual values of the data, we can detect which of the data values don't "fit" in) - see the Design page for more examples.
  
Example prompts:

- Validate the email field in the Customers_2024 dataset
- validate field status for dataset customer_events_2024
- validate field person.address.city for Customer Data dataset

Dataset validation: validates up to 5 fields in a dataset. The user may provide these fields explicitly, or, if not provided, we will automatically determine the most relevant fields using an AI analysis.
The validation skill provides exactly the same type of information, but for all of the targeted fields
Example prompts:
validate Customer Data 2024 dataset
validate fields email, phone for Customers_2024
summarize firstName, lastName, birthDate for Customer Data
summarize dataset 693012a4b8c98b09cea350bc

In both cases, the customers may specify the dataset via its name, its ID or its table name.