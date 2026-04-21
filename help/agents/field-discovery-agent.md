---
title: Field Discovery Agent
description: Learn how to use the Field Discovery Agent to find, evaluate, and select XDM fields in Adobe Experience Platform using natural language queries in AI Assistant.
keywords: field discovery, XDM, AI Assistant, AEP agents, entity linking, field recommendations, audience creation, segmentation
solution: Experience Platform
role: User, Admin, Developer
---

# Field Discovery Agent

<!--
  WRITER GUIDANCE — Intro paragraph (required; no stacked heading):
  Write 3–4 sentences that answer: what FDA is, how users interact with it (via natural
  language in AI Assistant), and establish its dual role — directly invocable by the
  user AND an underlying capability that other AEP agents call automatically. Close with
  a single boundary statement: FDA surfaces field information and returns ranked
  suggestions; it does not modify schemas, datasets, or audiences, and respects all
  existing access controls and sandbox context. Do not list features here; keep it
  goal-oriented and audience-appropriate for a marketer reading this for the first time.
  Reference: Execution Brief §1 (Core Objective), §5.1–5.2 (What it is / What it does).
-->

## Availability and permissions {#availability-and-permissions}

<!--
  WRITER GUIDANCE:
  State the product entitlements and permissions required to use FDA directly in AI
  Assistant. List the minimum required items as a bulleted prerequisite list (IMS org,
  sandbox context, AI Assistant access, and any specific FDA permission if one exists
  separately from AI Assistant). If no separate FDA-specific permission exists, state
  that clearly and cross-link to the Agent Orchestrator access guide rather than
  duplicating the full permission steps. Add an [!AVAILABILITY] callout above this
  section if FDA has any trial, limited-access, or license-tier restrictions.
  Reference: Execution Brief §3 (Audience & Prerequisites); Placement Evaluation §3
  (agent-orchestrator.md cross-link pattern).
-->

## Field Discovery Agent skills {#field-discovery-agent-skills}

<!--
  WRITER GUIDANCE:
  Open with 1–2 sentences scoping what this table covers before presenting it (style
  guide: never place a table directly under a heading without introductory prose). Then
  present a four-column skills table: Skill | Description | When to use it | Expected
  output. Populate one row per core skill: Identification, Recommendation,
  Classification, and Enrichment. Descriptions should be one sentence, user-goal
  framed (e.g., "Identifies the XDM fields that best match a business concept you
  describe in natural language."). Expected output should describe what the agent
  returns — not what it does internally. Model the table format directly on the Data
  Distiller Agent skills table.
  Reference: Execution Brief §2 In-Scope (core use cases); §5.2 (What it does).
-->

## How Field Discovery Agent works {#how-field-discovery-agent-works}

<!--
  WRITER GUIDANCE:
  This section is the primary transparency section. It must explain the agent's
  process at a conceptual level without exposing implementation details (no embeddings,
  no vector DB internals — these are explicitly out-of-scope per the Brief). Structure
  this as a short prose explanation covering three stages: (1) intent interpretation —
  how the agent reads natural language and maps it to a searchable concept; (2) search
  scope — what it searches across (schemas, datasets, metadata); (3) ranking — how it
  prioritizes results using semantic relevance signals. Use qualitative language for
  ranking ("fields with stronger metadata coverage are ranked higher") rather than
  algorithmic specifics. The goal is trust-building, not technical disclosure.
  Reference: Execution Brief §2 In-Scope (semantic matching, ranking logic);
  Out-of-Scope (deep technical architecture, full EL implementation details).
-->

## Understand your results {#understand-your-results}

<!--
  WRITER GUIDANCE:
  Open with 1–2 sentences explaining that FDA returns a structured result set and that
  understanding the result format helps users evaluate and act on recommendations
  confidently. Then introduce the three sub-sections below. Do not stack headings —
  include this bridging prose before the first H3.
  Reference: Execution Brief §2 In-Scope (Explanation of results); §1 Success Metric
  ("Users understand why results are ranked a certain way").
-->

### Relevance buckets

<!--
  WRITER GUIDANCE:
  Explain the three relevance tiers — high, medium, and low — and what each signals
  to the user about a field's fit for their query. Describe the practical implication
  of each bucket: what a user should do when a high-relevance field appears vs. when
  all results are medium or low. Avoid stating the exact algorithmic threshold for
  buckets (out-of-scope). One short paragraph or a three-row definition table is
  appropriate. If the UI labels these buckets visually (e.g., color coding or a badge),
  note that here and reference the screenshot placed in the next sub-section.
  Reference: Execution Brief §2 In-Scope (Relevance buckets: high / medium / low).
-->

### Sample values

<!--
  WRITER GUIDANCE:
  Describe that FDA returns sample values alongside field suggestions to help users
  verify a field contains the data they expect. Explain what sample values represent
  (example data drawn from the field in the user's sandbox). Include an [!IMPORTANT]
  callout immediately before or within this sub-section noting that sample values may
  contain personally identifiable information (PII) and are governed by the user's
  existing dataset permissions — users should not share sample values outside secure
  workflows. Do not state exact PII field categories; keep the note general and
  governance-oriented.
  Reference: Execution Brief §2 In-Scope (Sample values with PII caveats).
-->

### Usage context

<!--
  WRITER GUIDANCE:
  Explain that FDA provides usage context for each suggested field, showing where the
  field appears across the data ecosystem: schema → dataset → audience → destination.
  Describe why this matters to the reader — a field that appears in an active audience
  used in a live destination is more likely to be a reliable, meaningful field than one
  that exists only in a schema definition. Keep this practical and business-context
  framed for the primary (marketer) audience. One short paragraph is sufficient.
  Reference: Execution Brief §2 In-Scope (Usage context: schema → dataset → audience
  → destination).
-->

### Results in AI Assistant

<!--
  WRITER GUIDANCE:
  Describe the finalized UI result structure: the tables, expanders, and links that
  appear in the AI Assistant response panel when FDA returns results. Walk through the
  interface elements in the order a user encounters them. For each UI element (table,
  expander, link), name it using [!UICONTROL] notation, describe what it contains,
  and explain how to interact with it (using "select" not "click"). Place the
  screenshot(s) immediately after the instruction they illustrate. Include descriptive
  alt text for each image. This sub-section is the primary reference for users who
  have results on screen and need to know what they are looking at.
  Reference: User-provided clarification (UI in final state: tables, expanders, links);
  Adobe Style Guide §9 (Visual Elements), §5 (UI References).
-->

## Use Field Discovery Agent {#use-field-discovery-agent}

<!--
  WRITER GUIDANCE:
  Describe the end-to-end workflow for invoking FDA directly in AI Assistant, from
  opening AI Assistant to reviewing and acting on a result. Use a numbered list only if
  the steps are strictly sequential and platform-action-based; otherwise use prose with
  clear step markers per the style guide. Include: how to state intent (explicit natural
  language is required — model on the Data Distiller "state your intent explicitly"
  pattern), how to submit a query, and how to verify FDA handled the request using the
  Reasoning complete dropdown in the AI Assistant reasoning panel. Include a screenshot
  of the reasoning panel with FDA indicated, with alt text. Cross-link to the AI
  Assistant UI guide for users who need orientation on the interface itself.
  Reference: Execution Brief §2 In-Scope (What FDA is and when to use it — standalone);
  Placement Evaluation §3 (cross-link to ai-assistant-ui.md).
-->

## Supported use cases {#supported-use-cases}

<!--
  WRITER GUIDANCE:
  Open with 1–2 sentences stating that this section provides task-based guidance for
  each of FDA's four core skills. Introduce the sub-sections without stacking headings.
  Each H3 below should follow the same internal structure: (1) a one-sentence goal
  statement, (2) when to use this skill, (3) what to type in AI Assistant (example
  prompt in blockquote format), (4) what the agent returns (expected output aligned to
  the skills table above), (5) any relevant screenshot immediately after the described
  action. Do not reproduce the full result UI explanation here — cross-link to
  "Understand your results" for field-level result interpretation.
  Reference: Execution Brief §2 In-Scope (Core use cases: Identification,
  Recommendation, Classification, Enrichment).
-->

### Identify fields for a business concept

<!--
  WRITER GUIDANCE:
  Cover the Identification skill: the user describes a business concept in plain
  language (e.g., "customers in California" or "email opt-outs") and FDA returns
  XDM fields that semantically match that concept. Describe the scenario from the
  marketer's perspective — they have a segmentation goal but don't know which field
  holds the relevant data. Include at least one representative example prompt in
  blockquote format and describe the shape of the response (relevance-ranked field
  list). Draw examples from the demo transcript where available.
  Reference: Execution Brief §2 In-Scope (Identification); §5.2 (interprets user
  intent, returns ranked field suggestions).
-->

### Get field recommendations for a use case

<!--
  WRITER GUIDANCE:
  Cover the Recommendation skill: the user describes a use case or goal (e.g., "I want
  to build a loyalty audience" or "I'm modeling purchase propensity") and FDA recommends
  fields that are relevant to that goal. Distinguish this from Identification —
  Recommendation operates at the use-case or workflow level, not just a single concept.
  Describe the output: a prioritized list of fields with relevance context. Include a
  representative example prompt and output shape.
  Reference: Execution Brief §2 In-Scope (Recommendation).
-->

### Classify fields

<!--
  WRITER GUIDANCE:
  Cover the Classification skill: FDA categorizes fields by type, semantic role, or
  data category. Describe a realistic scenario — a data engineer or marketing ops user
  who needs to understand the type of data held in a set of fields before using them in
  a query or segment definition. Describe the output format (classification labels,
  categories). Include a representative example prompt.
  Reference: Execution Brief §2 In-Scope (Classification); §3 Audience (Secondary:
  Data Engineers / AEP implementers).
-->

### Enrich field context

<!--
  WRITER GUIDANCE:
  Cover the Enrichment skill: the user asks about a specific field and FDA returns
  enriched context — sample values, schema location, datasets where it appears, and
  audience or destination associations. This skill directly supports the "understand
  your results" transparency goal. Describe the scenario: a user has identified a
  candidate field and wants to verify it's the right one before using it. Include a
  representative example prompt and connect the output to the relevance buckets and
  usage context concepts already defined.
  Reference: Execution Brief §2 In-Scope (Enrichment; Sample values; Usage context).
-->

## Field Discovery Agent in other agents {#field-discovery-in-other-agents}

<!--
  WRITER GUIDANCE:
  Open with 2–3 sentences explaining FDA's role as an underlying capability: when other
  AEP agents need to resolve natural language references to XDM fields, audiences, or
  entities, they call FDA automatically — the user does not need to invoke FDA
  separately. State that users who interact with these agents benefit from FDA without
  needing to know it is running. Then introduce the sub-sections below without stacking
  headings. For each agent, explain specifically what FDA does in that context (what
  entity type it resolves and why), not just that it is used. Label the Data Engineering
  Agent as a future use case. This section is new to the agent doc pattern in this repo;
  cross-linking back to this section from audience.md and other affected agent docs is
  required (see Placement Evaluation §3).
  Reference: Execution Brief §2 In-Scope (Relationship to other agents); User-provided
  clarification (confirmed agent list and per-agent FDA usage).
-->

### Knowledge Base Audience Agent

<!--
  WRITER GUIDANCE:
  Describe FDA's role in the Knowledge Base Audience Agent: FDA (via entity linking)
  discovers the XDM fields required to define segment conditions so the Audience Agent
  can generate audiences. Explain this from the user's perspective — when a user asks
  the Audience Agent to create an audience based on a natural language description, FDA
  resolves the field references behind the scenes. Cross-link to the Audience Agent doc
  (audience.md) for users who want full audience creation guidance.
  Reference: User-provided clarification (Knowledge Base Audience Agent uses FDA for
  field discovery required to create segments and generate audiences).
-->

### Goal-Based Audience Agent

<!--
  WRITER GUIDANCE:
  Describe FDA's role in the Goal-Based Audience Agent: similar to the Knowledge Base
  Audience Agent, FDA resolves XDM fields needed to create segment definitions when a
  user states a business goal. Distinguish this from the Knowledge Base agent if a
  meaningful distinction exists for users (e.g., goal-based starts from a business
  objective rather than an audience name). If the distinction is not user-visible, note
  that FDA operates the same way in both and keep this brief to avoid redundancy.
  Reference: User-provided clarification (Goal-Based Audience Agent uses FDA for field
  discovery for audience generation).
-->

### Operational Insights

<!--
  WRITER GUIDANCE:
  Describe FDA's role in Operational Insights: entity linking identifies all named
  entities in a user's natural language query — datasets, schemas, journeys, attributes,
  sources, and audiences — so the Operational Insights agent can resolve the correct
  objects. Explain why this matters to the user: when a user refers to an audience by
  an approximate name or a dataset by a partial name, FDA resolves the correct entity
  rather than returning no result or the wrong one.
  Reference: User-provided clarification (Op-insights uses EL to identify all entity
  names: datasets, schemas, journeys, attributes, sources, audiences).
-->

### Time Series

<!--
  WRITER GUIDANCE:
  Describe FDA's role in Time Series: entity linking identifies true audience entities
  from user natural language queries, handling cases where a user uses an audience ID
  or an inexact audience name. Explain the user benefit: the Time Series agent can
  resolve ambiguous audience references accurately, reducing the risk of querying the
  wrong audience.
  Reference: User-provided clarification (Time Series uses EL for identifying true
  audience entities from NLQ, handling audience IDs and inexact names).
-->

## In scope and out of scope {#in-scope-and-out-of-scope}

<!--
  WRITER GUIDANCE:
  Open with one sentence stating that this section summarizes FDA's supported and
  unsupported capabilities, and cross-link to "Supported use cases" and "Guardrails
  and limitations" for full details. Then present two sub-sections below. Use bulleted
  lists for each (not tables, which are better reserved for the skills section).
  Reference: Execution Brief §2 (Scope Boundaries); Adobe Style Guide §3 (progressive
  disclosure; cross-linking).
-->

### In scope

<!--
  WRITER GUIDANCE:
  List what FDA supports: all four skills (Identification, Recommendation,
  Classification, Enrichment), result ranking and explanation, sample value surfacing
  (within permissions), usage context display, and operation as an underlying capability
  within other agents. Keep items concise — one clause per bullet.
  Reference: Execution Brief §2 In-Scope.
-->

### Out of scope

<!--
  WRITER GUIDANCE:
  List what FDA does not support. Draw directly from the Execution Brief out-of-scope
  items and translate them into user-facing language: FDA does not modify schemas or
  datasets, does not create audiences or segments, does not expose internal embedding
  architecture, and does not guarantee SLA-bound hydration windows. Cross-link to
  "Guardrails and limitations" for the constraints that most affect outcomes.
  Reference: Execution Brief §2 Out-of-Scope.
-->

## Guardrails and limitations {#guardrails-and-limitations}

<!--
  WRITER GUIDANCE:
  Open with one sentence stating that FDA operates within platform-level constraints
  that affect result quality and availability. Then introduce the three sub-sections
  below without stacking headings. This section must set accurate expectations without
  overpromising on timing or coverage. Avoid hard SLA numbers (out-of-scope per the
  Brief); use qualitative language with directional guidance (e.g., "results may take
  time to reflect recent schema changes").
  Reference: Execution Brief §2 In-Scope (Limitations / constraints); Out-of-Scope
  (Exact SLA guarantees).
-->

### Knowledge base hydration

<!--
  WRITER GUIDANCE:
  Explain that FDA relies on a knowledge base that is periodically updated with schema
  and metadata from the user's AEP environment. New schemas, fields, or datasets may
  not appear in FDA results immediately after creation — results reflect the state of
  the knowledge base at the time of the query. Do not state a specific hour count.
  Use language such as "results may take time to reflect recent changes." Include a
  [!NOTE] if the delay window is expected to change, and advise users to resubmit
  queries if a newly added field is not appearing.
  Reference: Execution Brief §2 In-Scope (KB hydration delay); §4 Non-Blocking
  Unknowns (exact KB hydration timing: currently ~24h but changing → document as
  "may take time").
-->

### Metadata quality and coverage

<!--
  WRITER GUIDANCE:
  Explain that FDA's result quality depends on the quality and completeness of field
  metadata in the user's AEP environment. Fields with descriptive names, populated
  display names, and dataset associations rank higher and return more useful context.
  Fields with poor metadata (e.g., unnamed, undescribed, or isolated in a schema with
  no dataset) may not surface or may rank lower. Provide one or two actionable data
  hygiene recommendations (e.g., use friendly display names in schemas). Keep guidance
  practical and brief — this is a constraint section, not a configuration guide.
  Reference: Execution Brief §2 In-Scope (Dependence on metadata quality); §4
  Non-Blocking Unknowns (ranking algorithm specifics: can describe qualitatively).
-->

### Access and PII constraints

<!--
  WRITER GUIDANCE:
  State that FDA respects all existing AEP access controls and sandbox context: users
  only see fields from schemas and datasets they have permission to access. Reiterate
  (briefly, linking back to "Sample values") that sample values may include PII and
  are governed by the same dataset-level permissions. State that FDA does not bypass
  field-level security or profile-enabled restrictions. This sub-section is concise —
  two to four sentences maximum; it reinforces trust and governance rather than
  introducing new content.
  Reference: Execution Brief §5.2 (agent respects access controls); Placement
  Evaluation §3 (PII sample value conflict flag).
-->

## Example prompts {#example-prompts}

<!--
  WRITER GUIDANCE:
  Open with one sentence advising users to state their intent clearly and specifically
  (specificity improves results — this is the core prompting principle from the Brief).
  Then organize prompts by skill using H3 subsections below. Each prompt should be in
  blockquote format. For each skill, provide 3–5 example prompts ranging from broad
  to specific, demonstrating how prompt specificity affects result precision. Do not
  include expected outputs here — cross-link to the relevant supported use case
  sub-section for full context. Prompts should be realistic for the primary audience
  (marketer) and include at least one prompt per skill that a data engineer would
  recognize as relevant (secondary audience).
  Reference: Execution Brief §2 In-Scope (Example prompts and outputs); §3 Audience;
  Adobe Style Guide §6 (descriptive link text; cross-linking).
-->

### Identification prompts

<!--
  WRITER GUIDANCE (applies to all four prompt H3s):
  Provide 3–5 example prompts in blockquote format, ordered from less specific to more
  specific. The last prompt in each group should model the level of specificity the
  Best practices section recommends. No additional prose is needed within each H3 —
  let the prompts speak for themselves and keep this section scannable.
-->

### Recommendation prompts

### Classification prompts

### Enrichment prompts

## Best practices {#best-practices}

<!--
  WRITER GUIDANCE:
  Write this section as a bulleted list of actionable, prescriptive guidance for
  getting accurate results from FDA. Organize bullets around the three key behaviors
  the Brief identifies: (1) prompt specificity (more specific language produces better-
  ranked results), (2) use of domain terminology that matches schema metadata, and
  (3) iterating on results (using enrichment to verify a field before using
  identification to find more fields in the same area). Do not restate generic AI
  guidance that applies to all agents — focus on FDA-specific behavior. Each bullet
  should be one sentence, imperative voice, with a brief rationale clause where
  helpful. Cross-link back to "How Field Discovery Agent works" to reinforce why
  specificity helps (it improves semantic matching).
  Reference: Execution Brief §2 In-Scope (Best practices for prompting: specificity
  improves results); Adobe Style Guide §4 (lists: parallel structure, no stacking).
-->

## Troubleshooting {#troubleshooting}

<!--
  WRITER GUIDANCE:
  Structure this section as a definition-style list using bold problem statements
  followed by a one-to-two sentence resolution, matching the Data Distiller
  troubleshooting pattern. Cover at minimum: (1) expected fields not appearing in
  results — likely KB hydration delay; cross-link to "Knowledge base hydration";
  (2) all results showing low relevance — likely a metadata quality issue; cross-link
  to "Metadata quality and coverage" and advise refining the prompt; (3) FDA not
  invoked — user submitted a query but the reasoning panel shows a different agent
  was called; advise stating intent more explicitly and cross-link to "Use Field
  Discovery Agent"; (4) sample values not appearing — access permission issue;
  cross-link to "Access and PII constraints." Add a final closing sentence directing
  users to the reasoning panel to confirm which agent handled their request, with a
  cross-link to the AI Assistant UI guide.
  Reference: Execution Brief §1 Success Metric (fewer support/escalation questions);
  Placement Evaluation §11 (troubleshooting identified as a missing standard section
  in 5 of 6 existing agent docs).
-->
