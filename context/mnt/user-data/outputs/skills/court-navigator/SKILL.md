---
name: court-navigator
description: "Provides step-by-step guidance for navigating court processes including small claims, civil, employment tribunals, and consumer forums."
allowed-tools: Read Write
---

# Court Navigator Skill

## Purpose
Guide users through the process of taking a matter to court — from deciding whether to file,
through preparation, to what happens on the day and after.

## Execution Steps

### Step 1 — Determine Appropriate Court

Ask: What is the dispute about and how much is involved?

**Small Claims Court (ideal for most user situations):**
| Jurisdiction | Max Claim Amount | Court Name |
|---|---|---|
| India | No fixed limit (Consumer Forum) | District Consumer Disputes Redressal Commission |
| US – California | $12,500 | Small Claims Court |
| US – New York | $10,000 | Small Claims Court |
| US – Texas | $20,000 | Justice of the Peace Court |
| UK | £10,000 | County Court (Small Claims Track) |
| Canada – Ontario | $35,000 | Small Claims Court |
| Australia – NSW | $20,000 | NSW Civil and Administrative Tribunal (NCAT) |

**When NOT to use small claims:**
- Criminal matters — wrong court entirely
- Injunctions (court orders to stop behavior) — need civil court
- Claims above the limit — need regular civil court + likely a lawyer

### Step 2 — Pre-Filing Checklist

Before filing, the user should have:
- [ ] Written demand letter sent to the other party (offer to draft via draft-letter skill)
- [ ] Response deadline passed (typically 14–30 days)
- [ ] All evidence organized (contracts, receipts, photos, text messages, emails)
- [ ] Claim amount calculated (main loss + any additional damages allowed by law)
- [ ] Witness information if applicable (names and contact details)

### Step 3 — Filing Instructions by Jurisdiction

**India — Consumer Forum:**
1. Download complaint form from National Consumer Helpline (consumerhelpline.gov.in)
2. Fill Form 1 with full details of complaint
3. Attach: bill/receipt, correspondence with company, ID proof
4. Pay filing fee (₹100–₹5000 based on claim amount)
5. File at District Consumer Forum (in-person or online via edaakhil.nic.in)
6. Keep acknowledgment receipt — hearing date will be communicated

**US — Small Claims (General):**
1. Go to local courthouse clerk's office or court website
2. Fill out plaintiff's claim form (varies by state)
3. Pay filing fee ($30–$100 typically; fee waivers available for low income)
4. Court serves the defendant OR you arrange service (certified mail in most states)
5. Get your court date — typically 30–70 days out

**UK — County Court Online:**
1. Go to moneyclaim.gov.uk
2. Create account and submit claim online
3. Pay issue fee (£35–£455 based on claim amount; remission available)
4. Defendant has 14 days to respond
5. If no response: apply for default judgment
6. If disputed: mediation offered first, then hearing scheduled

### Step 4 — Preparing Your Case

**What to bring to court:**
- All original documents (contracts, receipts, invoices)
- Printed copies of all written communication (emails, texts — printed with dates visible)
- A written timeline of events (chronological, factual, no emotional language)
- Any photos or videos (on phone or printed)
- Witnesses (confirm availability and notify court if required)
- Your demand letter and proof it was sent

**How to present your case:**
1. Introduce yourself and state what you are claiming and why
2. Present facts chronologically — stick to facts, not feelings
3. Reference your evidence as you present each fact
4. State the exact remedy you are seeking (specific amount or action)
5. Be respectful to the judge at all times — say "Your Honor"
6. Let the other party speak without interrupting

### Step 5 — After the Judgment

**If you win:**
- Court issues a judgment in your favor
- Other party has set time to pay (typically 14–30 days)
- If they don't pay: you can apply for enforcement (wage garnishment, bank levy, property lien)

**If you lose:**
- You can appeal within a set deadline (typically 30 days)
- Ask for written reasons for the judgment
- Consult a lawyer before deciding to appeal — costs escalate

### Step 6 — Provide Jurisdiction-Specific Resources
Always close with:
- Official court website link for the user's jurisdiction
- Filing fee information and fee waiver availability
- Local legal aid contact if user needs further help (hand off to find-legal-aid skill)
