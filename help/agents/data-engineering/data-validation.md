---
title: Validate Your Data With Data Engineering Agent
description: Learn how you can use the Data Engineering Agent to perform statistical and semantical validations on your datasets.
---
# Validate your data with Data Engineering Agent

You can use the Data Engineering Agent to validate the data quality of your Adobe Experience Platform datasets. With the Data Engineering Agent, you can perform statistical and semantical validations on datasets, analyze dataset fields, identify data quality issues, and retrieve natural language summaries with actionable insights. Data engineers, analysts, and data stewards can utilize the validation skills of the Data Engineering Agent to execute rapid data quality assessments without writing SQL queries or navigating complex schema hierarchies.

By using the data validation capabilities of the Data Engineering Agent, you can:

- Fill the essential gaps in both the onboarding process and the day-to-day diagnostics.
- Reduce manual QA on your datasets.
- Accelerate time-to-value for your customers.

Read this documentation for comprehensive information on how you can use the Data Engineering Agent to validate your data on Experience Platform.

## Validation types

There are two main validation types that you can perform with the Data Engineering Agent:

- **Field validation**: Validate a specific field in a dataset.
- **Dataset validation**: Validate up to five (5) fields in a dataset. 

>[!BEGINTABS]

>[!TAB Field validation]

Use field validation to validate a specific field in a given dataset. This skill provides you with the following:

- Null count and unique value count.
- Top unique values and their corresponding frequencies.
- AI-assisted semantic validation (the ability to detect invalid values based on the available metadata and the actual values of the data).

Example prompts for field validation include:

- Validate the email field in the Customers_2024 dataset.
- Validate field status for the dataset customer_events_2024.
- Validate field person.address.city for Customer Data dataset.

>[!TAB Dataset validation]

Use dataset validation to validate entire datasets, summarizing overall quality and key issues. While you can provide these fields explicitly, the Data Engineering Agent can also analyze the dataset and automatically determine the most relevant fields. This skill provides the same type of information as field validation, albeit to a number of several targeted fields. You can validate up to five fields in a given dataset. 

Example prompts for dataset validation include:

- Validate Customer Data 2024 dataset.
- Validate fields email, phone for Customers_2024.
- Summarize firstName, lastName, birthDate for Customer Data.
- Summarize dataset 693012a4b8c98b09cea350bc.

>[!ENDTABS]
