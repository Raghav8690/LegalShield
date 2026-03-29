---
name: draft-letter
description: "Drafts professional legal correspondence for disputes and formal complaints. Supports demand letters, eviction disputes, wage claims, consumer complaints, cease & desist notices, and more."
allowed-tools: Read Write
---

# Draft Letter Skill

## Purpose
Generate professional, legally appropriate letters for common dispute scenarios. Uses proper legal
language, cites applicable law, and customizes to the user's specific situation.

## When to Use
Use this skill when a user needs a formal letter for a legal dispute. Common triggers include:
- "Write a letter to my landlord"
- "Draft a complaint to my employer"
- "I need a demand letter"
- "Help me write a formal complaint"
- "I want to send a cease and desist"

## Letter Types Supported
- Security deposit demand letter
- Eviction dispute / cease & desist notice
- Employer wage claim letter
- Consumer fraud complaint
- General cease & desist notice
- Insurance claim dispute
- Academic appeal letter
- GDPR / data deletion request
- Debt collector violation notice
- Workplace harassment complaint
- Defective product complaint

## Execution Steps

### Step 1 — Gather Required Information
Collect the following from the user (use [PLACEHOLDER] format for anything missing):
- **User's full name** and address
- **Recipient's name** and address (landlord, employer, company, etc.)
- **Key facts** — What happened, when, amounts involved
- **Jurisdiction** — Country and state/city
- **Desired outcome** — What the user wants (refund, payment, action to stop, etc.)

### Step 2 — Identify Applicable Law
Based on jurisdiction and letter type, identify the specific statute to cite:
- India: Consumer Protection Act 2019, Rent Control Acts, Payment of Wages Act 1936
- US: State landlord-tenant law, FLSA, FTC Act, FDCPA, state consumer protection acts
- UK: Consumer Rights Act 2015, Housing Act 1988, Employment Rights Act 1996
- Canada: Provincial tenancy acts, employment standards acts
- Australia: Australian Consumer Law, Fair Work Act 2009

### Step 3 — Draft the Letter
Structure every letter with these sections:
1. **Header** — Date, sender address, recipient address
2. **Subject line** — Clear, direct subject (e.g., "Formal Demand for Return of Security Deposit")
3. **Opening** — Identify yourself, state purpose of letter
4. **Facts** — Chronological account of what happened (concise, factual, no emotion)
5. **Legal basis** — Cite the specific applicable law and how it applies
6. **Demand** — State exactly what you want and by when (usually 14-30 days)
7. **Consequence** — State what you will do if demand is not met (e.g., file complaint, go to court)
8. **Closing** — Professional sign-off

### Step 4 — Format for Use
- Use formal letter formatting
- Mark all user-specific fields with `[PLACEHOLDER]` format
- Keep letter under 400 words — brevity is powerful in legal correspondence
- Use professional but accessible language

### Step 5 — Provide Delivery Instructions
After the letter, always include:
- **How to send:** Certified mail/registered post + email (for proof of delivery)
- **Deadline to set:** Typically 14-30 days for response
- **What to do if ignored:** File complaint with relevant authority, proceed to court
- **Record keeping:** Keep copies of everything sent and received

## Output Format
```
## Your Letter: [Letter Type]

**Jurisdiction:** [Country, State]
**Applicable Law:** [Statute name]

---

[DATE]

[YOUR NAME]
[YOUR ADDRESS]

[RECIPIENT NAME]
[RECIPIENT ADDRESS]

**Subject: [Clear subject line]**

Dear [Recipient],

[Letter body with facts, legal basis, demand, and consequence]

Sincerely,
[YOUR NAME]

---

### How to Send This Letter
📮 **Method:** [Certified mail + email]
⏰ **Response deadline:** [14-30 days]
📂 **Keep copies:** [What to retain]
⚠️ **If no response:** [Next steps - court, complaint, etc.]
```

## Tone
Professional, firm, but not aggressive. The letter should command respect while remaining factual.
The user instructions (outside the letter) should be warm and empowering.
