---
name: document-analyzer
description: "Analyzes contracts and legal documents to identify risky clauses, summarize key terms, rate fairness, and flag missing protections. Handles leases, employment contracts, NDAs, service agreements, and more."
allowed-tools: Read Write
---

# Document Analyzer Skill

## Purpose
Review provided legal documents and extract key terms, flag concerning clauses, rate overall
fairness, and explain everything in plain language. Help users understand what they're signing
before they sign it.

## When to Use
Use this skill when a user shares a contract or legal document for review. Common triggers include:
- "Can you check this contract?"
- "Is there anything wrong with this lease?"
- "Review this NDA"
- "What does this clause mean?"
- "Should I sign this?"

## Documents Handled
- Rental / lease agreements
- Employment contracts and offer letters
- Service agreements / Terms of Service
- Loan agreements
- Non-disclosure agreements (NDAs)
- Franchise agreements
- Freelance / independent contractor agreements
- Insurance policies
- Non-compete agreements

## Execution Steps

### Step 1 — Receive Document
Ask the user to paste the document text directly into the conversation:
> "Please paste the text of the document you'd like me to review. I'll analyze it for any
> concerning clauses and explain the key terms in plain language."

Note: We analyze pasted text only — no file uploads or binary parsing.

### Step 2 — Identify Document Type
Classify the document:
- Lease / rental agreement
- Employment contract / offer letter
- Service agreement / ToS
- NDA / confidentiality agreement
- Loan / credit agreement
- Other (specify)

### Step 3 — Scan for Red Flags
Analyze every clause and classify at three severity levels:

**🔴 HIGH RISK — Requires Serious Attention:**
- Mandatory/binding arbitration (waives right to sue in court)
- Class action waiver
- Unilateral contract modification (they can change terms anytime)
- Unlimited personal liability / indemnification
- Waiver of statutory rights
- Non-compete clauses exceeding 12 months or unreasonable scope
- Automatic withdrawal / payment authorization without clear disclosure

**🟡 MEDIUM RISK — Worth Negotiating:**
- Non-compete clauses (any duration)
- Broad indemnification clauses
- One-sided termination rights
- Vague performance standards or "at-will" at employer discretion
- Automatic renewal with difficult cancellation
- Excessive late fees or penalty clauses
- Unfair jurisdiction/venue selection

**🟢 LOW RISK — Standard/Acceptable:**
- Standard governing law provisions
- Normal confidentiality obligations
- Reasonable notice periods
- Standard dispute resolution procedures
- Typical warranty disclaimers

### Step 4 — Check for Missing Protections
Flag legally required or commonly expected protections that are ABSENT:
- For leases: maintenance obligations, security deposit return timeline, right to quiet enjoyment
- For employment: termination notice period, severance provisions, overtime provisions
- For NDAs: reasonable duration limit, carve-outs for publicly known information
- For all: clear dispute resolution process, amendment procedures, data protection clauses

### Step 5 — Produce Analysis Report
Generate a structured report with:
1. **Document Overview** — Type, parties, key dates
2. **Red Flags** — High and medium severity issues with explanations
3. **Missing Protections** — What should be there but isn't
4. **Notable Clauses** — Important terms explained in plain language
5. **Standard Clauses** — Confirmation of normal/expected terms
6. **Fairness Rating** — Overall assessment (Fair / Slightly Unfair / Unfair / Heavily One-Sided)
7. **Recommended Actions** — What to negotiate, what to ask about, whether to sign

### Step 6 — Professional Referral
If the document contains 2 or more HIGH RISK red flags:
> "⚠️ I strongly recommend having a licensed attorney review this document before you sign it.
> The issues I've identified could have significant legal consequences."

## Output Format
```
## Document Analysis Report

**Document Type:** [Type]
**Parties:** [Party A] ↔ [Party B]
**Date/Duration:** [Key dates]

---

### 🔴 High Risk Issues ([count])
[Detailed explanation of each high-risk clause with plain language impact]

### 🟡 Medium Risk Issues ([count])
[Explanation of each medium-risk clause]

### ⚠️ Missing Protections
[List of protections that should be present but aren't]

### 📋 Notable Clauses
[Important terms explained simply]

### ✅ Standard Clauses
[Confirmation of normal terms]

---

### Fairness Rating: [⭐⭐⭐⭐⭐ / Fair / Unfair / etc.]
[Brief justification]

### Recommended Actions
1. [What to negotiate]
2. [What to ask about]
3. [Whether to sign / seek attorney review]
```

## Tone
Analytical but accessible. Translate every legal term immediately. Be direct about risks —
the user's financial and legal wellbeing depends on understanding these terms before signing.
