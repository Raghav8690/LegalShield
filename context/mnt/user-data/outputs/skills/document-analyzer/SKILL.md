---
name: document-analyzer
description: "Analyzes contracts and legal documents to identify risky clauses, summarize key terms, and rate overall fairness."
allowed-tools: Read Write
---

# Document Analyzer Skill

## Purpose
Review legal documents provided by the user, identify concerning clauses, summarize key
terms in plain language, and give an honest assessment of the document's fairness.

## Execution Steps

### Step 1 — Accept Document Input
Ask the user to paste the full text of the document, or the relevant sections they're concerned about.
Note: LegalShield works with pasted text (compatible with clawless/WebContainer environment).

### Step 2 — Identify Document Type
Classify the document:
- Rental / Lease Agreement
- Employment Contract / Offer Letter
- Service Agreement / Terms of Service
- Non-Disclosure Agreement (NDA)
- Loan or Finance Agreement
- Purchase Agreement
- Franchise Agreement
- Privacy Policy

### Step 3 — Analyze for Red Flags

**High Severity Red Flags (🔴) — Advise serious caution:**
- Mandatory binding arbitration clause (waives right to sue in court)
- Class action waiver (prevents joining others in a lawsuit)
- Unilateral contract modification (other party can change terms without your consent)
- Unlimited liability clause on the weaker party
- IP ownership grabbing all work created even outside employment
- Jurisdiction clause forcing disputes in a distant location
- Automatic renewal with unreasonably difficult cancellation

**Medium Severity (🟡) — Note and explain:**
- Non-compete clauses (scope, duration, geography)
- Liquidated damages clauses (pre-set penalties)
- Indemnification clauses (who pays if something goes wrong)
- Limitation of liability on the stronger party
- One-sided termination rights
- Vague "reasonable" standards with no definition

**Low Severity (🟢) — Mention as context:**
- Standard governing law clauses
- Standard confidentiality provisions
- Normal notice period requirements

### Step 4 — Identify Missing Protections
Flag legally required terms that are ABSENT:
- India rentals: Missing rent receipt obligation, missing maintenance responsibilities
- US employment: Missing overtime provisions where required by FLSA
- UK consumer contracts: Missing 14-day cooling off right under Consumer Contracts Regulations

### Step 5 — Summary Report Format

```
📋 DOCUMENT ANALYSIS REPORT
Document Type: [Type]
Jurisdiction: [If identifiable]
Date Analyzed: [Today's date]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━

🔴 HIGH RISK CLAUSES ([count])
1. [Clause name] — [Plain language explanation] — [Specific concern]
   → What it means for you: [Impact in practical terms]

🟡 NOTABLE CLAUSES ([count])
1. [Clause name] — [Plain language explanation]
   → Consider negotiating: [What to ask for]

🟢 STANDARD CLAUSES ([count])
[Brief list — no need for alarm]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━

⚖️ OVERALL ASSESSMENT
Fairness Rating: [Unfavorable / Somewhat Unfavorable / Balanced / Favorable]
[2–3 sentence plain-language summary]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📌 RECOMMENDED ACTIONS
1. [Most important action — negotiate, clarify, or refuse this clause]
2. [Second action]
3. [Whether to get a lawyer to review before signing]
```

### Step 6 — Closing Guidance
- If 2+ red flags: Strongly recommend attorney review before signing
- If arbitration clause present: Always flag this as a significant rights waiver
- Offer to explain any specific clause in more detail
- Offer to draft a negotiation email if user wants to push back on terms
