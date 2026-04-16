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

## Use cases

| Use case | Description |
| --- | --- |
| New implementation | In these scenarios, you can use the Data Engineering Agent to validate key identity and event fields to confirm formats and null rates look healthy. |
| Suspected mapping issue | In these scenarios, you can use the Data Engineering Agent to validate a field and inspect top values and invalids to confirm it matches the intended semantics. |
| Ongoing data stewardship | In these scenarios, you can use the Data Engineering Agent to run dataset validation on critical datasets weekly to catch regressions early. |

## How validation works

When you initiate a validation, the Data Engineering Agent analyzes a representative sample of your dataset, typically the most recent ~1,000 rows, rather than processing the entire dataset history. The process is strictly read-only, ensuring that your data, schemas, and mappings remain unchanged. Validation results are consistent regardless of how your data enters Experience Platform, whether through sources, streaming, file uploads, Data Prep, or other ingestion methods. Results serve as indicative checks to help you quickly identify data quality patterns or potential issues, enabling you to take further action (such as exploring with Query Service) if needed. This approach allows for rapid assessments without disrupting data ingestion or impacting production workloads.

## Validation results

For every validated field, the Data Engineering Agent returns:

**Basic statistics**

- Total row count used for the sample
- nullCount (and optionally % null)
- uniqueCount (where available)
- Top unique values (for example, top 10) and their frequencies

**Semantic validation**

- List of **suspected invalid values**
- For each invalid value, an **explanation** (for example, "not a valid email format", "timestamp outside expected range")

**Natural language summary**

- A short narrative summary of field quality
- Suggested next actions, such as "review mapping for field X", "consider dropping field Y due to high null rate", or "tighten validation for email format".

| Aspect | Example output |
| --- | --- |
| Completeness | `nullCount = 9,532 (95.3%)` |
| Uniqueness | `uniqueCount = 3` |
| Top values | `"True" (255), "False" (243)` |
| Initial values | `"abc@, reason: "not a valid email address"` |

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

## Checks performed by the Data Engineering Agent

For each field or dataset, the agent can perform:

- **Completeness checks**: null/missing counts and percentages.
- **Distribution checks**: top unique values and their distributions, high‑cardinality detection.
- **Semantic checks vs schema**: uses the XDM field name, type, and description to infer what "valid" looks like, then flags anomalies.
- **Datatype‑aware checks** (where applicable):
  - Email: format and domain plausibility
  - Phone: format readiness (for example, E.164)
  - Dates/timestamps: basic format sanity (for example, ISO‑8601)
- **Identity‑related checks** (future / extended): uniqueness of candidate identity fields or composite keys.

These checks combine deterministic statistics with LLM‑assisted semantic validation to detect values that "look wrong" even when they technically match the schema.

## Limitations

Before using the Data Engineering Agent for data validation, it's important to be aware of a few key limitations. These constraints are intended to balance performance with functionality, and will help set expectations for the types of analysis and insights you can expect.

- **Sampling only**: Validation operates on a sample of the dataset (typically the last ~1,000 rows) rather than processing the entire dataset. Full-dataset scans are not available.
- **Field count limit**: When validating a dataset, the agent analyzes up to five fields per request. You can specify these fields, or allow the agent to select them automatically.
- **Probabilistic semantics**: Detection of invalid values relies in part on LLM-based inference, which may occasionally miss subtle errors or flag borderline values.
- **Read-only operation**: The agent does not make any changes to your data or its schema. It provides insights and highlights potential issues, but does not perform automated fixes.

If your validation needs are more exhaustive or require applying complex business logic, consider supplementing the agent's results with additional tools such as Query Service or Data Prep validations.