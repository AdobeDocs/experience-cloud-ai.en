---
title: Get Started With Coworker Chat In Playground
description: Learn how to use Coworker Chat in Playground to explore how natural-language prompts can help you learn, investigate, and refine your work. 
hide: true
---
# Get started with Coworker Chat in Playground

Use Coworker Chat in Playground to explore how natural-language prompts can help you learn, investigate, and refine your work. Playground provides sample ways to start a conversation so you can quickly understand what Coworker Chat can do.

>[!IMPORTANT]
>
>Use the following to complete this exercise:
>
>- Link: [ao.adobe.io](https://ao.adobe.io/)
>- Instance: AEP GenAI - VA7
>- Sandbox: `fsi-box`

## AI Coworker Demo: [!DNL weBank] Credit Card Upgrade Campaign

This exercise covers Real-Time CDP and Adobe Journey Optimizer.

You're a CX Enterprise strategist at **[!DNL weBank]**, a digital-first financial services company. Use the AI Coworker to go from raw data to a live campaign — entirely through conversation.

## Part 1: Understand Your Business

### 1.1 — Get the lay of the land

**Prompt**

> Give me an overview of my sandbox — how many audiences, datasets, and destinations do I have?

**Expected result**

Coworker returns a full sandbox inventory in seconds:

| Resource | Count |
| --- | --- |
| Audiences | 21 |
| Datasets | 30 |
| Schemas | 28 |
| Sources | 3 |
| Destinations | 1 (Amazon S3) |
| Journeys | 0 |

### 1.2 — What audiences already exist?

**Prompt**

> List all my audiences sorted by size

**Expected result**

Coworker lists 21 audiences sorted by size, from 8,012 profiles down to 0:

| Category | Audience | Profiles |
| --- | --- | --- |
| Propensity scores | Credit Card Upgrade High | 1,195 |
| Propensity scores | Medium | 4,113 |
| Propensity scores | Low | 8,012 |
| Mortgage propensity | High | 1,233 |
| Mortgage propensity | Medium | 4,141 |
| Mortgage propensity | Low | 7,946 |
| Account value tiers | +500K | 4,377 |
| Account value tiers | 250-500K | 4,537 |
| Account value tiers | 100-250K | 2,666 |
| Account value tiers | 50-100K | 894 |
| Account value tiers | <50K | 846 |
| Demographics | Female | 6,719 |
| Demographics | Male | 6,601 |
| Geography | East Coast | 2,260 |
| Geography | West Coast | 1,740 |
| Channel opt-in | Email | 6,597 |
| Channel opt-in | SMS | 6,675 |
| Birthday | Birthday this month | 0 |
| Birthday | Within 7 days | 0 |
| Birthday | Today | 0 |
| Birthday | Next 30 days | 0 |

All birthday audiences currently show 0 because they are time-dependent.

### 1.3 — What data feeds these audiences?

**Prompt**

> What datasets do I have that contain customer data?

**Expected result**

Coworker identifies two key business datasets and related system datasets:

| Dataset | Description |
| --- | --- |
| **weBank: CRM** | Customer profile/account data (profile + identity enabled) |
| **weBank: Customer Actions** | Behavioral event data (profile + identity enabled) |

System Journey Optimizer datasets for engagement signals include email tracking, push tracking, consent, and message feedback.

## Part 2: Discover the Right Fields

### 2.1 — Find account value fields

**Prompt**

> What fields are available related to account value or balance?

**Expected result**

Coworker surfaces the primary field and related fields in the **weBank: CRM** dataset:

| Field | Notes |
| --- | --- |
| `_aepgenai_va7.fsiBankAccountDetails.totalAccountValue` | Primary field; used in all 5 Account Value tier audiences |
| `numberOfAccounts` | Related field |
| `accountType` | Related field |
| `currentStatement` | Related field |
| `actionAmount` | Related field |

### 2.2 — Find credit card fields

**Prompt**

> Find fields related to credit card or card type

**Expected result**

Coworker identifies these fields in the **weBank: CRM** schema:

| Field | Description |
| --- | --- |
| `_aepgenai_va7.fsiBankAccountDetails.creditcardType` | Stores card type (Visa, Mastercard, Amex) |
| `_aepgenai_va7.fsiBankAccountDetails.creditcardHolder` | Cardholder name |

### 2.3 — Geographic fields

**Prompt**

> Is there a field for home state or region?

**Expected result**

Coworker identifies geographic fields in the **weBank: CRM** dataset:

| Field | Notes |
| --- | --- |
| `homeAddress.state` | U.S. state abbreviation; used in Lives on East Coast and Lives on West Coast |
| `homeAddress.stateProvince` | Also found |
| `homeAddress.region` | Also found |
| `placeContext.geo.stateProvince` | Also found |

## Part 3: Find the Right Audience for a Reactivation Campaign

### 3.1 — Ask the AI to help you find the right audience

**Prompt**

> Help me find or create the right audience for a credit card reactivation campaign — I want to target customers who were scored as high or medium propensity for a credit card upgrade but haven't taken action yet

**Expected result**

Coworker finds two candidate audiences that have never been targeted in a journey or destination:

| Audience | Profiles |
| --- | --- |
| Credit Card Upgrade High | 1,195 |
| Credit Card Upgrade Medium | 4,113 |

Recommended options:

| Option | Approach |
| --- | --- |
| **A** | Use both directly with journey branching — aggressive offer for High, nurture for Medium |
| **B** | Create a derived segment-of-segments with upgrade-exclusion logic for cleaner management |

Combined size: approximately 5,308 profiles

### 3.2 — Create the precision audience

**Prompt**

> Create an audience of customers who are in the "Propensities: Credit Card Upgrade High" audience AND have an account value over $250,000 AND are opted in to email

Name it **Platinum Upgrade - High Value Email Eligible** → Select Batch → Approve Plan

**Expected result**

Coworker layers ML propensity, financial value, and channel eligibility into one precision segment — work that would normally require a data team ticket.

### 3.3 — Estimate size & waterfall

**Prompt**

> How large is that audience? Show me the waterfall breakdown.

**Expected result**

Coworker returns a real-time profile count estimate and a visual waterfall chart:

| Filter step | Result |
| --- | --- |
| Credit Card Upgrade High propensity | Approximately 1,195 profiles |
| + Account Value over $250K | Narrows further |
| + Email Opt-In | Final addressable count |

This shows exactly which condition is the biggest filter and whether to loosen the criteria.

### 3.4 — Check for similar audiences

**Prompt**

> Are there any existing audiences similar to the one I just created?

**Expected result**

Coworker confirms no single combined audience exists, but all building blocks are already present:

| Building block | Details |
| --- | --- |
| Propensities: Credit Card Upgrade High | Score ≥ 90 |
| Account Value: 250-500K | Existing audience |
| Account Value: +500K | Existing audience |
| Email Opt-In | `consents.marketing.email.val = "y"` |

Coworker confirms there is no duplication risk and recommends proceeding.

## Part 4: Build the Journey

### 4.1 — Get journey ideas grounded in your data

**Prompt**

> Based on popular use cases in financial services, suggest some quick-win journeys I can create with the audiences I have

**Expected result**

Coworker suggests five concrete journey ideas grounded in actual audiences:

| Journey idea | Audiences |
| --- | --- |
| Birthday Loyalty Touch | Birthday within 7 days + Account Value tiers |
| Credit Card Upgrade Nurture | CC Upgrade High + Email Opt-In |
| Mortgage Regional Outreach | Mortgage High + East/West Coast |
| Wealth Tier Advisory Upgrade | Account Value: +500K |
| Opt-In Cross-Channel Activation | Email Opt-In minus SMS Opt-In |

### 4.2 — Create the credit card upgrade journey

**Prompt**

> Create a journey using the audience "Platinum Upgrade - High Value Email Eligible". Send a push notification introducing the weBank Platinum Card benefits. Wait 3 days. If the customer hasn't applied, send an SMS with a limited-time offer of 0% APR for 12 months on balance transfers. Wait 5 more days. If still no application, send a final push notification with a personal banker invitation.

Review plan → Approve Plan → Grant permissions

**Expected result**

Coworker creates a full 3-touch, 2-channel journey from a single natural language description, including wait timers, condition checks, and escalating offers.

### 4.3 — Bonus: Create a journey from an image

**Prompt**

> Create this journey from the image I uploaded

**Expected result**

Coworker reads the uploaded image — including nodes, channels, wait times, and conditions — and generates the full journey in Journey Optimizer. This turns a planning artifact directly into a deployable journey.

### 4.4 — Check for conflicts

**Prompt**

> Are there any active journeys that could conflict with the journey I just created?

**Expected result**

Coworker automatically checks all active journeys for audience overlap, schedule collisions, and channel saturation.

## Part 5: Turn Journey Drop-Offs into a New Audience

### 5.1 — Identify the drop-off point

**Prompt**

> Show me the journey I just created and identify which step has the biggest drop-off

**Expected result**

Coworker analyzes journey step events and surfaces the node with the highest exit rate. For example:

> 68% of profiles who received the first email never opened it and exited before the SMS step.

### 5.2 — Create a drop-off audience

**Prompt**

> Turn those journey drop-offs into a new audience — people who entered the Platinum Upgrade journey but never reached the SMS step

Name it **Platinum Upgrade - Email Non-Responders** → Select Batch → Approve Plan

**Expected result**

Coworker creates a net-new audience based on journey behavioral data — profiles that entered the journey but did not progress to the SMS step. This audience is immediately usable for a follow-up campaign.

### 5.3 — Reactivate the drop-offs

**Prompt**

> Create a reactivation journey for the "Platinum Upgrade - Email Non-Responders" audience. Try a different approach — start with a push notification highlighting a limited-time 75,000 bonus points offer, wait 2 days, then send a direct mail invitation to visit their local branch.

Review plan → Approve Plan → Grant permissions

**Expected result**

Coworker creates a dedicated recovery journey using different channels and messaging for non-responders. You have now closed the loop on a conversion leak — entirely through conversation.

## Part 6: Automated QA & Validation

### 6.1 — Data freshness and ingestion health check

**Prompt**

> Are there any data quality issues with the datasets feeding my audiences? Check ingestion health for weBank: CRM and weBank: Customer Actions

**Expected result**

Coworker reports ingestion health for each dataset:

| Dataset | Status | Details |
| --- | --- | --- |
| **weBank: CRM** | Healthy | 39 records ingested, 32 to profile, zero failures |
| **weBank: Customer Actions** | Minor flag | 441 records ingested; 35 had expired timestamps; approximately 8% excluded due to TTL window |

Recommendation: Review TTL settings or check the source system for stale records.

### 6.2 — Validate the journey before publishing

**Prompt**

> Review the Platinum Upgrade journey for errors or quality issues — check for missing wait timers, dead-end paths, missing channel configurations, and audience eligibility gaps

**Expected result**

Coworker inspects the journey structure and flags issues such as:

| Issue type | Example |
| --- | --- |
| Dead-end paths | Paths that do not end with an end node |
| Channel configuration | Actions missing channel surface configurations |
| Wait timers | Timers that could cause SLA issues |
| Content | Nodes with missing content |

## Part 7: Monitoring & Governance

### 7.1 — Track audience health over time

**Prompt**

> Show me how the "Propensities: Credit Card Upgrade High" audience has changed over the last 30 days

**Expected result**

Coworker returns a time-series view of audience growth or decline with trend analysis, helping you identify whether the ML model's scoring is drifting or upstream data changes are affecting qualification.

### 7.2 — Diagnose a change

**Prompt**

> Why did the "Account Value: +500K" audience drop recently?

**Expected result**

Coworker performs causal analysis by decomposing the change across:

| Factor | Question |
| --- | --- |
| Data freshness | Was there an ingestion gap? |
| Merge policy changes | Did profile stitching shift? |
| Upstream source changes | Did CRM data stop flowing? |
| Actual customer behavior | Did account values genuinely decline? |

This replaces 1–2 days of analyst triage.

