---
title: Privacy, Security, and Governance in AI Assistant
description: Learn about the privacy, security, and governance practices for AI Assistant.
TQID: https://experienceleague.adobe.com/ViaEXSy4OEyTzSKlYAq0T6PbewPx1PJtyzE8E0wXbvM
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: Experience Cloud
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
---
# Privacy, Security, and Governance in AI Assistant

AI Assistant in Adobe Experience Platform is built with privacy, security, and governance at the forefront.

Read this document to learn about the customer trust-focused capabilities that you can expect from AI Assistant:

* No personal data is being used by AI Assistant today, even for training purposes.
* AI Assistant is unaware of consumer data.
* All existing [access control](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home) policies will be honored by AI Assistant.
  * Any new attribute-based access control policies are reflected in AI Assistant after a maximum of 24 hours&ast;
* AI Assistant is a HIPAA-ready feature when used in combination with Adobe Experience Platform Healthcare Shield.
* You can view a log of your previous interactions with AI Assistant with a 30-day retention policy.
* AI Assistant is grounded in sandbox-specific data and public Adobe documentation when answering to user prompts. Data is not shared across sandboxes.
* Prompts that you provide to AI Assistant are not shared to other customers.

&ast; *This implies that if any new labels are added to fields and objects or any new policies are created, then it will take AI Assistant up to 24 hours to honor them. During those 24 hours, users with newly restricted access can still access those fields and objects.*
