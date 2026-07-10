---
title: Validate data with Coworker when upgrading from Adobe Analytics to Customer Journey Analytics
description: Learn how Analytics admins use the CX Enterprise Coworker data validation skill to compare Adobe Analytics and Customer Journey Analytics data during migration.
hold: true
---
# Validate data with Coworker when upgrading from Adobe Analytics to Customer Journey Analytics

CX Enterprise Coworker includes a validation skill that allows you to validate data when upgrading from Adobe Analytics to Customer Journey Analytics. Data validation is completed within a single conversation.

This skill automatically compares:

* Each dimension, metric, and trend individually across implementations. 

* All Adobe Analytics report suites against all Customer Journey Analytics data views. 

After making these comparisons, the skill generates AI-driven insights and recommendations that you can implement to facilitate your upgrade to Customer Journey Analytics.

## Before you begin

To validate data as part of your upgrade, you need:

* The Adobe Analytics report suite you want to validate.

* The Customer Journey Analytics data view that contains the same data.

You don't need to know how your implementation is architected ahead of time. The skill automatically detects whether your data is mapped through an Analytics source connector or through two side-by-side implementations, so you don't have to provide that context yourself.

## Start a validation session

1. Log in to CX Enterprise Coworker.

1. Select [!UICONTROL **New Chat**].

1. In the text field, prompt the agent to validate your migration from Adobe Analytics to Customer Journey Analytics:

   **Prompt**

   > Help me validate my company's upgrade from Adobe Analytics to Customer Journey Analytics.

   Your request is routed to the data validation skill, which starts an interactive setup process. 

1. The setup process includes the questions in the table below. For each question, select an answer, then select [!UICONTROL **Submit**].

   >[!NOTE]
   >
   >You can change any of these selections later in the same conversation. For example, ask the agent to change your report suite or data view, and the agent repeats only the steps needed to update that selection, without restarting the entire setup process.

   | Question | Additional context |
   |---------|----------|
   | [!UICONTROL **Select your Analytics company**] | This is your Adobe Analytics login company. |
   | [!UICONTROL **Select your report suite**] <!--In the UI, recommend change to "Select your Adobe Analytics report suite"--> | This is the report suite in Adobe Analytics that contains the data that you want to validate against the Customer Journey Analytics data. |
   | [!UICONTROL **Select your Customer Journey Analytics data view**] | This is the data view in Customer Journey Analytics that contains the same data as the Adobe Analytics report suite that you selected. |

1. Review the setup summary to confirm you're validating the right data before you continue. The summary includes the company, report suite, and data view you selected, along with a preview of the top metrics and dimensions in each system.

1. Continue with the following section, [Choose the data to validate](#choose-the-data-to-validate).

## Choose the data to validate

You can validate individual metrics or dimensions, or you can validate all metrics and dimensions that are included in the report suite and data view. 

1. Select from the following options:

   | Validation option | Description |
   |---------|----------|
   | [!UICONTROL **Single metric comparison**] | Compare one metric's trend between Adobe Analytics and Customer Journey Analytics. Use this when you want a quick check on a specific metric, such as page views or visits. |
   | [!UICONTROL **Single dimension comparison**] | Compare the breakdown of a single dimension between Adobe Analytics and Customer Journey Analytics. Use this when you suspect a mapping or classification difference for a specific dimension. |
   | [!UICONTROL **Full report suite and data view audit**] | Compare up to 40 metrics and 10 dimensions in a single run. Use this when you want a comprehensive view of your migration's overall health. |



1. Continue with the following section, [Review the analysis](#review-the-analysis).

## Review the analysis

1. Select the [!UICONTROL **Overall matching rate**] tab to view a percentage that indicates how closely the data from the Adobe Analytics report suite matches that of the Customer Journey Analytics data view. This score always appears first, before any other results. It weighs every compared metric and dimension equally to ensure that high-volume metrics, such as page views, don't skew the score.

   Use the following scale to interpret the score:

   | Score | Rating | What it means |
   |---------|----------|----------|
   | 97%–100% | ![Green square](./images/data-validation-aa-cja/excellent-square.svg) [!UICONTROL Excellent] | All properties are highly aligned. No action required. |
   | 90%–96% | ![Yellow circle](./images/data-validation-aa-cja/good-circle.svg) [!UICONTROL Good] | Minor gaps are present. Monitor trends and investigate if they decline. |
   | 75%–89% | ![Orange circle](./images/data-validation-aa-cja/review-circle.svg) [!UICONTROL Review] | Meaningful gaps exist. Investigate root causes before relying on Customer Journey Analytics data. |
   | Less than 75% | ![Red circle](./images/data-validation-aa-cja/critical-circle.svg) [!UICONTROL Poor] | Significant misalignment. Take immediate action before using Customer Journey Analytics data. |

1. Select the [!UICONTROL **Key insights**] tab to view two to four short callout boxes, each summarizing one finding from the analysis in a single sentence. Callouts are color-coded by severity so you can spot the most important findings first.

1. Select the [!UICONTROL **Summary**] tab to view Adobe Analytics totals, Customer Journey Analytics totals, total variance, days passing, and days critical, where days passing and days critical reflect how many days in the date range fall into the [!UICONTROL **Pass**] and [!UICONTROL **Critical**] variance statuses described below.

1. (Conditional) When doing a single-dimension comparison or a single-metric comparison, you can view a side-by-side comparison of the Adobe Analytics data and the Customer Journey Analytics data in the [!UICONTROL **Daily trend**] tab.

   For metrics, this is a line chart that compares the daily trend.

   ![Daily trend tab showing a line chart](./images/data-validation-aa-cja/trend-line.png)

   For dimensions, this is a bar chart that compares the top values.

   ![Daily trend tab showing a horizontal bar chart](./images/data-validation-aa-cja/trend-bar.png)

1. (Conditional) When doing a single-dimension comparison or a single-metric comparison, you can view row-level detail in the [!UICONTROL **Date detail**] tab. This table lists the date, the Adobe Analytics value, the Customer Journey Analytics value, the variance percentage, and a status badge for each compared metric or dimension value.

   ![Date detail tab showing a table of variance percentages and status badges](./images/data-validation-aa-cja/date-detail.png)

   The variance and status columns use the following scale:

   | Variance | Status | What it means |
   |---------|----------|----------|
   | Less than 3% | ![Green checkmark](./images/data-validation-aa-cja/pass-check.svg) [!UICONTROL Pass] | Data is well aligned. No action required. |
   | 3%–10% | ![Yellow warning triangle](./images/data-validation-aa-cja/flagged-warning.svg) [!UICONTROL Flag] | Monitor the difference and investigate if it continues or worsens. |
   | Greater than 10% | ![Red circle](./images/data-validation-aa-cja/critical-circle.svg) [!UICONTROL Critical] | Investigate immediately. This usually points to a schema, ingestion, or mapping issue. |

1. (Conditional) When running a full report suite and data view audit, the [!UICONTROL **Daily trend**] and [!UICONTROL **Daily detail**] tabs are replaced by a scorecard showing pass, flagged, and critical counts, along with separate tables listing the top five best-matching and top five lowest-matching metrics and dimensions.

1. Scroll down in the analysis to view additional patterns and issues that were discovered during the analysis, likely causes for those patterns, and suggested actions that you can take to resolve any data discrepancies. 

   >[!NOTE]
   >
   >Some variance is expected and doesn't indicate a problem with your migration. 

   Common issues include:

   * Adobe Analytics counts device-based visitors, while Customer Journey Analytics counts people, using cross-device identity stitching.
   * Adobe Analytics processes data at collection time, while Customer Journey Analytics processes data at report time.
   * Session definitions differ: Adobe Analytics visits use a fixed timeout, while Customer Journey Analytics sessions are configurable.
   * Adobe Analytics filters bots by default, while Customer Journey Analytics bot filtering is opt-in.
   * Adobe Analytics reports missing values as "Unspecified" or "None," while Customer Journey Analytics reports them as "No value."
   * Marketing channel differences can result from Adobe Analytics processing rules compared to Customer Journey Analytics derived fields applied retroactively.
   * If Customer Journey Analytics values are consistently about twice the Adobe Analytics values across all metrics, this usually indicates duplicate data in the data view rather than an identity stitching effect.

1. Verify that the suggested actions are valid, then resolve them in Adobe Experience Platform or Adobe Analytics.

1. (Optional) Continue your analysis by analyzing another metric, analyzing another dimension, or by running another report of up to 40 metrics and 10 dimensions, as described in [Choose the data to validate](#choose-the-data-to-validate). You don't need to repeat the setup process to do this; your company, report suite, and data view selections carry forward throughout the conversation.

