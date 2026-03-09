---
title: Data Engineering Agent
description: Learn how you can use the Data Engineering Agent. 
hide: true
hidefromtoc: true
---
# Data Engineering Agent

<!--- THIS IS A DRAFT --->

Data Engineering Agent is an Agent Orchestrator-powered, AI-based copilot for data teams in Adobe Experience Platform. The agent is designed to handle the heavy lifting across the end-to-end data lifecycle: data modeling, onboarding, SQL data prep, governance, and lifecycle management. With the Data Engineering Agent, engineers and architects can move faster with higher data quality and less manual work.

Data Engineering Agent is organized into skills that you can take advantage of to optimize your workflows.

| Data Engineering Agent skill | Description |
| --- | --- |
| Data Onboarding | <strong>Data onboarding</strong> supports batch sources such as S3, Marketo, and Data Landing Zone (DLZ). Its capabilities include: <ul><li>Connecting to various data sources including S3, Data Landing Zone, Marketo, and more.</li><li>Profiling source data (e.g., distinct values, nulls, duplicates, and basic quality metrics).</li><li>Aligning source fields to both standard XDM field groups and custom fields.</li><li>Proposing and building data ingestion dataflows (for example, moving data from S3 or Marketo into RTCDP/CJA datasets).</li></ul> |
| Automated data quality and semantic enrichment | <ul><li>Performs comprehensive data quality assessments, including identifying anomalies and reporting valid/invalid record counts.</li><li>Recommends data quality improvements such as type normalization, currency formatting, and ID deduplication.</li><li>Applies semantic enrichment to schemas based on data sampling and intelligent naming pattern recognition.</li><li>Engages users for confirmation on suggested enrichments, ensuring finalized and approved data changes.</li></ul> |
| Data Distiller | |
| Data Collection | |
| Data Validation | |

With Data Engineering Agent, you can ensure:

- **Faster onboarding**: Reduce time from weeks of manual schema mapping & pipeline setup to hours of guided, conversational configuration.
- **Higher data quality**: Fewer invalid records and production incidents due to built‑in data quality analysis and semantic checks.
- **Improved governance & compliance**: Governance policies are attached at design time (labels, TTL, identity handling) rather than as an afterthought.
- **More productive data teams**: Repetitive SQL/dataflow work is automated so engineers focus on higher‑value design and optimization.
- **Broader self‑service**: Non‑expert stakeholders can safely self‑serve common data prep tasks with guardrails.