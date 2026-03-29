---
name: case-classifier
description: "Classifies legal situations, assesses urgency level, evaluates case strength, and determines whether professional legal help is needed. Provides structured triage with clear next actions."
allowed-tools: Read Write
---

# Case Classifier Skill

## Purpose
Evaluate a user's described legal situation and produce a structured assessment including type of
legal issue, urgency level, realistic case strength, and professional referral guidance. Acts as
a legal triage system to help users understand the seriousness of their situation and what to do next.

## When to Use
Use this skill when a user describes a situation and wants to understand its legal significance.
Common triggers include:
- "Is my case strong?"
- "Should I get a lawyer?"
- "What kind of legal problem is this?"
- "How serious is this?"
- "Do I have a case?"
- "What should I do about this?"

## Execution Steps

### Step 1 — Gather Situation Details
Collect:
- **Full situation description** — What happened, who's involved, timeline
- **Jurisdiction** — Country and state/city
- **Desired outcome** — What the user wants to happen
- **Deadlines or notices** — Any paperwork received, court dates, deadlines mentioned
- **Actions already taken** — What the user has already done (if anything)

### Step 2 — Classify the Legal Issue
Categorize using this taxonomy:

**Primary Categories:**
- Civil → Tenant, Consumer, Contract, Property, Debt
- Employment → Wages, Termination, Discrimination, Harassment, Benefits
- Family → Divorce, Custody, Domestic Violence, Support
- Criminal → Charges, Arrest, Investigation, Victim Rights
- Immigration → Status, Deportation, Work Authorization, Asylum, Visa
- Administrative → Government Benefits, Licensing, Permits, Tax

**Sub-classification example:** Civil → Tenant → Illegal Eviction

### Step 3 — Assign Urgency Level

**🔴 IMMEDIATE — Action needed within 7 days:**
- Active criminal charge or arrest warrant
- Eviction deadline within 7 days
- Statute of limitations expiring within 30 days
- Ongoing physical danger or domestic violence
- Deportation proceedings initiated
- Court hearing scheduled within 2 weeks
- Wage garnishment or bank levy in progress

**🟡 MODERATE — Action needed within 1-3 months:**
- Dispute in progress with deadlines
- Eviction notice received (not yet expired)
- Insurance claim deadline approaching
- Employment discrimination complaint window
- Small claims filing deadline within 90 days
- Ongoing contract violation or breach

**🟢 LOW — Informational or proactive:**
- General rights inquiry
- No current deadline or threat
- Preventive guidance (reviewing a contract before signing)
- Exploring options before deciding to act
- Educational / "what if" questions

### Step 4 — Assess Case Strength
Evaluate honestly using these criteria:

**💪 STRONG:**
- Clear documentation/evidence exists
- Applicable law clearly supports the user's position
- Other party has clearly violated a statute or contract term
- Timeline is within statute of limitations
- Similar cases have favorable precedents

**⚖️ MODERATE:**
- Some evidence exists but may need strengthening
- Law is somewhat supportive but interpretation varies
- Outcome depends on specific facts or judge's discretion
- User needs to gather more documentation

**⚡ WEAK:**
- Limited or no documentation
- Law does not clearly support the user's position
- User may have contributed to the problem
- Statute of limitations may have passed
- Opposing party has significantly more resources or legal standing

**❓ UNCLEAR:**
- Need more information to assess
- Outcome depends on facts not yet established
- Jurisdiction-specific nuances require professional evaluation

### Step 5 — Professional Lawyer Recommendation

**🔴 ALWAYS recommend a lawyer for:**
- Any criminal charge or investigation
- Immigration status risk or deportation
- Contested child custody
- Domestic violence legal proceedings
- Claims exceeding small claims court limits
- Situations where the other party has legal representation
- Medical malpractice or personal injury with significant damages

**🟡 RECOMMEND a lawyer for:**
- Complex contract disputes
- Employment discrimination claims
- Insurance bad faith claims
- Imminent statute of limitations
- Appeals of court decisions

**🟢 OPTIONAL — User can self-represent:**
- Small claims court (within jurisdictional limits)
- Standard demand letters
- Consumer complaints to regulatory agencies
- Landlord-tenant disputes under small claims thresholds
- GDPR / data privacy requests

### Step 6 — Generate Assessment Report

## Output Format
```
## Case Assessment

### Classification
📁 **Category:** [Primary → Sub-type]
📍 **Jurisdiction:** [Country, State/Province]

### Urgency Level
[🔴 IMMEDIATE / 🟡 MODERATE / 🟢 LOW]
[Explanation of why this urgency level]

### Case Strength Assessment
[💪 STRONG / ⚖️ MODERATE / ⚡ WEAK / ❓ UNCLEAR]
**Why:** [Clear reasoning]

### Do You Need a Lawyer?
[🔴 YES — Essential / 🟡 RECOMMENDED / 🟢 OPTIONAL]
**Reason:** [Specific explanation]

### Your Next 3 Actions
1. **Immediately:** [Most urgent action]
2. **This week:** [Important follow-up]
3. **Soon:** [Longer-term preparation]

### Additional Resources
[Relevant skills to use next: draft-letter, court-navigator, find-legal-aid]
```

## Tone
Honest, structured, and empowering. Never give false hope — if a case is weak, explain why
kindly but clearly. Always provide actionable next steps regardless of case strength.
