---
name: case-classifier
description: "Classifies legal situations by type and urgency, assesses case strength honestly, and determines whether professional legal help is required."
allowed-tools: Read Write
---

# Case Classifier Skill

## Purpose
Give users a structured, honest assessment of their legal situation — what kind of legal
issue it is, how urgent it is, how strong their position appears, and whether they need a lawyer.

## Execution Steps

### Step 1 — Gather Situation Details
Ask the user to describe:
- What happened (key facts and timeline)
- Who is involved (individual vs company vs government)
- What outcome they want
- Their location (country + state)
- Any deadlines or notices they've already received

### Step 2 — Classify the Legal Issue

**Primary Categories:**
- Civil Dispute (landlord/tenant, employer/employee, consumer/business)
- Criminal Matter (charges, arrest, police interaction)
- Family Matter (divorce, custody, domestic situation)
- Immigration Matter (visa, status, deportation concern)
- Administrative Matter (government agency dispute, benefits denial)
- Constitutional / Rights Violation

**Sub-classification examples:**
- Civil → Tenant → Illegal Eviction
- Civil → Employment → Wage Theft
- Civil → Consumer → Online Fraud
- Criminal → Misdemeanor → Traffic / Minor Offense
- Criminal → Felony → Serious charge (ALWAYS recommend immediate attorney)

### Step 3 — Assess Urgency

**🔴 IMMEDIATE ACTION REQUIRED if:**
- Statute of limitations expires within 30 days
- Court date or response deadline is imminent
- Active criminal charge or arrest
- Ongoing physical danger or harassment
- Eviction notice with short deadline
- Child custody emergency

**🟡 MODERATE URGENCY if:**
- Deadline within 1–3 months
- Ongoing but not immediately escalating dispute
- Documents need to be preserved now
- Employer/landlord threatening action

**🟢 LOW URGENCY / INFORMATIONAL if:**
- User wants to understand rights proactively
- Dispute hasn't officially started yet
- No immediate deadlines

### Step 4 — Assess Case Strength (Honestly)

Rate as: **Strong / Moderate / Weak / Unclear**

**Strong indicators:**
- Clear written evidence (contracts, texts, emails)
- Other party violated a specific law with a defined remedy
- User followed proper procedures
- Pattern of behavior documented

**Weak indicators:**
- No written evidence — he said / she said
- User also contributed to the problem
- Statute of limitations may have passed
- Dispute amount may not justify legal costs

**Always be honest.** If the case appears weak, say so kindly:
> "Based on what you've described, this may be a difficult case to pursue because [reason]. Here's what would strengthen it: [actions]."

### Step 5 — Professional Lawyer Recommendation

**Recommend a lawyer immediately if:**
- Any criminal charge (no exceptions)
- Immigration status at risk (no exceptions)
- Child custody is contested (no exceptions)
- Claim value exceeds small claims court limits
- Other party has legal representation
- Statute of limitations is nearly expired
- Case involves constitutional rights violation

**Can self-represent with LegalShield guidance if:**
- Small claims court (typically under $10,000–$25,000 depending on jurisdiction)
- Standard demand letter situations
- Consumer complaint filings
- Basic tenant dispute correspondence

### Step 6 — Output Format

```
⚖️ CASE ASSESSMENT — LegalShield

━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Issue Type:     [Category → Subcategory]
Jurisdiction:   [Country, State]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

🚨 URGENCY: [🔴 IMMEDIATE / 🟡 MODERATE / 🟢 LOW]
[One-sentence explanation of why]

📊 CASE STRENGTH: [Strong / Moderate / Weak / Unclear]
[2–3 sentences on why, what evidence helps or hurts]

👨‍⚖️ DO YOU NEED A LAWYER?
[YES — highly recommended because: ... ]
[OPTIONAL — you can self-represent but a lawyer would help because: ...]
[NOT REQUIRED — you can handle this with guidance]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🎯 YOUR NEXT 3 ACTIONS:
1. [Most critical step]
2. [Second step]
3. [Third step]

Available LegalShield skills for next steps:
→ [Relevant skill recommendations]
```
