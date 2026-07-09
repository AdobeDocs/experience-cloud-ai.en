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
   | [!UICONTROL **Full report suite and data view audit**] | Compare up to 20 metrics and dimensions in a single run. Use this when you want a comprehensive view of your migration's overall health. |

1. Continue with the following section, [Review the analysis](#review-the-analysis).

## Review the analysis

1. Select each of the following tabs to review the analysis:

   | Analysis review tab | Description |
   |---------|----------|
   | [!UICONTROL **Overal matching rate**] | A percentage that indicates how closely the data from the Adobe Analytics report suite matches that of the Customer Journey Analytics data view. |
   | [!UICONTROL **Key insights**] | Key insights discovered during the analysis. |
   | [!UICONTROL **Summary**] | Adobe Analytics totals, Customer Journey Analytics totals, total variance, days passing, and days critical. <!--what are these?--> |
   | [!UICONTROL **Daily trend**] | Graph showing a side-by-side comparison of the Adobe Analytics data and the Customer Journey Analytics data. |
   | [!UICONTROL **Daily detail**] | <!--what goes here?--> |

1. Scroll down in the analysis to view additional patterns that were discovered during the analysis, likely causes for those patterns, and suggested actions that you can take to resolve any data discrepancies. 

1. Verify that the suggested actions are valid, then resolve them in Adobe Experience Platform or Adobe Analytics.

1. (Optional) Continue your analysis by analyzing another metric, analyzing another dimension, or by running another report of up to 20 metrics and dimensions, as described in [Choose the data to validate](#choose-the-data-to-validate).

