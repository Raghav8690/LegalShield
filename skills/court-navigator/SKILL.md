---
name: court-navigator
description: "Provides step-by-step guidance for navigating court processes including small claims, civil court, consumer forums, family court, and employment tribunals across India, US, UK, Canada, and Australia."
allowed-tools: Read Write
---

# Court Navigator Skill

## Purpose
Guide users through the complete process of taking a legal matter to court — from deciding whether
to file, to preparing documents, to what to expect on the day. Demystify the court system for
people who have never been to court before.

## When to Use
Use this skill when a user wants to take a matter to court or understand the process. Common triggers:
- "How do I file in small claims court?"
- "What do I bring to court?"
- "How does this process work?"
- "Can I take this to court?"
- "How do I sue someone?"
- "What happens in court?"

## Court Types Covered

### Small Claims Court
| Country | Court Name | Typical Limit |
|---------|-----------|---------------|
| India | Consumer Disputes Redressal Forum (District) | ₹50 lakhs (Consumer Protection Act 2019) |
| US | Small Claims Court (varies by state) | $2,500–$25,000 (state dependent) |
| UK | County Court (Small Claims Track) | £10,000 |
| Canada | Small Claims Court (provincial) | $10,000–$50,000 (province dependent) |
| Australia | Civil and Administrative Tribunal (state) | $10,000–$40,000 (state dependent) |

### Other Courts
- Civil Court (basic procedures)
- Employment Tribunal / Labor Court
- Consumer Disputes Redressal Commission (India — District, State, National)
- Family Court (overview only — always recommend lawyer)
- Administrative Tribunals

## Execution Steps

### Step 1 — Confirm Eligibility
- Confirm jurisdiction and claim amount
- Determine correct court based on claim value and type
- Check if the user's matter qualifies (some matters can't go to small claims)
- Confirm statute of limitations hasn't expired

### Step 2 — Pre-Filing Checklist
Walk the user through preparation before filing:
1. ☐ Have you sent a demand letter? (If not, offer draft-letter skill)
2. ☐ Have you calculated your total claim amount? (Include damages, interest, costs)
3. ☐ Have you gathered all evidence? (Contracts, receipts, photos, communications)
4. ☐ Do you know the full legal name and address of the other party?
5. ☐ Have you checked if you're within the time limit to file?

### Step 3 — Filing Instructions (Jurisdiction-Specific)

**India — Consumer Forum:**
1. Draft complaint in prescribed format (or use eDaakhil portal: edaakhil.nic.in)
2. Pay filing fee (based on claim amount — often minimal, ₹100–₹5,000)
3. Submit at District Consumer Disputes Redressal Forum
4. Attach: complaint copies (3), evidence copies, ID proof, demand letter copy
5. Forum issues notice to opposite party within 21 days

**US — Small Claims:**
1. Get claim form from local courthouse or court website
2. Fill in: your info, defendant info, claim amount, brief description
3. Pay filing fee ($30–$75 typically; fee waiver available for low income)
4. File at courthouse serving defendant's location
5. Serve the defendant (court may serve or you arrange service)

**UK — County Court:**
1. File claim online at Money Claims Online (MCOL) or paper N1 form
2. Pay filing fee (based on claim amount; fee remission available)
3. Court serves claim on defendant
4. Defendant has 14 days to respond

**Canada — Small Claims:**
1. Complete plaintiff's claim form (varies by province)
2. Pay filing fee ($75–$225 typically)
3. File at courthouse in correct jurisdiction
4. Arrange service on defendant

**Australia — Tribunal:**
1. Check your state's civil & administrative tribunal website
2. Complete application form online
3. Pay application fee (may be waived for hardship)
4. Tribunal notifies the respondent

### Step 4 — Hearing Preparation
Guide the user on what to expect:
- **Organize evidence** — Chronological order, extra copies for judge and other party
- **Prepare a timeline** — Written summary of events with dates
- **Practice your statement** — 3-5 minutes, factual, calm
- **Dress appropriately** — Business casual or formal
- **Arrive early** — At least 30 minutes before hearing time
- **Bring** — All documents, ID, pen and paper, calculator

### Step 5 — What Happens at the Hearing
- Judge/mediator will ask both parties to present their side
- Present facts calmly and chronologically
- Refer to your evidence and hand copies to the judge
- Answer questions directly — don't argue with the other party
- Stay calm and respectful regardless of what the other party says

### Step 6 — After the Hearing
- **If you WIN** — Explain enforcement options (garnishment, liens, etc.)
- **If you LOSE** — Explain appeal options and deadlines
- **If the other party doesn't pay** — Post-judgment collection procedures

## Output Format
```
## Court Navigator: [Court Type]

**Jurisdiction:** [Country, State]
**Court:** [Specific court name]
**Claim Limit:** [Amount]

### Pre-Filing Checklist
☐ [Item 1]
☐ [Item 2]
...

### How to File (Step by Step)
1. [Step with specific details]
2. [Step with specific details]
...

### Filing Fee
💰 [Amount and fee waiver info]

### What to Bring to Court
📋 [Complete list]

### What to Expect at Your Hearing
[Day-of guidance]

### After the Hearing
✅ If you win: [Enforcement guidance]
❌ If you lose: [Appeal options]
```

## Tone
Steady, encouraging, and detailed. Many users are terrified of court. Normalize the process,
explain everything in plain language, and reassure them that small claims court is designed
for regular people without lawyers.
