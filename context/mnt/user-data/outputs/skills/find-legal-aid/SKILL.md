---
name: find-legal-aid
description: "Finds free and low-cost legal aid organizations, hotlines, and resources by user location."
allowed-tools: Read Write
---

# Find Legal Aid Skill

## Purpose
Connect users to real, free, or affordable legal help in their location — including government
legal aid, NGOs, law school clinics, bar association programs, and helplines.

## Execution Steps

### Step 1 — Confirm Location and Legal Issue Type
Ask:
- Country and state/city
- Type of legal issue (housing, employment, consumer, family, criminal, immigration)
- Whether they have any income constraints (for income-based aid eligibility)

### Step 2 — Match to Resources by Jurisdiction

---

## INDIA

**National:**
- **NALSA (National Legal Services Authority)**
  - Website: nalsa.gov.in
  - Free legal aid for eligible persons (income below ₹1 lakh/year, SC/ST, women, disabled, children)
  - Services: Lawyer representation, legal advice, mediation
  - Helpline: 15100

- **National Consumer Helpline**
  - Website: consumerhelpline.gov.in
  - Helpline: 1800-11-4000 (toll-free)
  - For: Consumer disputes, fraud, defective products/services

- **eDaakhil (Online Consumer Complaints)**
  - Website: edaakhil.nic.in
  - File consumer complaints online without visiting forum

**Maharashtra-specific:**
- Maharashtra State Legal Services Authority (MSLSA): mslsa.nic.in
- District Legal Services Authorities (DLSA): In every district headquarters
- Lok Adalat: Free alternate dispute resolution — fast, binding, no court fees

**For Women:**
- National Commission for Women: ncw.nic.in | Helpline: 7827170170
- iCall (Tata Institute): icallhelpline.org | Mental health + referrals

---

## UNITED STATES

**National:**
- **LawHelp.org** — lawhelp.org — Find free legal aid by state
- **Legal Services Corporation** — lsc.gov — Federally funded legal aid locator
- **American Bar Association Free Legal Help** — findlegalhelp.org
- **Law School Clinics** — Most ABA-accredited law schools run free clinics; search "[your city] law school legal clinic"

**By Issue Type:**
- Housing: **HUD-approved housing counselors** — hud.gov/findacounselor
- Employment: **Department of Labor Wage and Hour Division** — dol.gov/agencies/whd
- Immigration: **CLINIC (Catholic Legal Immigration Network)** — cliniclegal.org
- Domestic Violence: **National DV Hotline** — thehotline.org | 1-800-799-7233

---

## UNITED KINGDOM

- **Citizens Advice** — citizensadvice.org.uk | Free advice on any legal issue
- **Legal Aid Agency** — Check eligibility: gov.uk/check-legal-aid
- **Law Centres Network** — lawcentres.org.uk — Free legal help for disadvantaged communities
- **Shelter (Housing)** — shelter.org.uk | 0808 800 4444 (free)
- **ACAS (Employment)** — acas.org.uk | Free employment dispute mediation
- **MoneyHelper (Debt/Finance)** — moneyhelper.org.uk

---

## CANADA

- **Community Legal Education Ontario (CLEO)** — cleo.on.ca
- **Legal Aid Ontario** — legalaid.on.ca | 1-800-668-8258
- **Law Society Referral Service** — lsrs.lso.ca — 30 min free consultation
- **Pro Bono Ontario** — probonoontario.org — Free legal help for individuals
- **Settlement.org** — For newcomers and immigration legal help

---

## AUSTRALIA

- **Community Legal Centres Australia** — clcs.org.au — Find local free legal help
- **Legal Aid Commission** — Each state has one; search "[state] Legal Aid"
- **Law Access NSW** — lawaccessnsw.gov.au | 1300 888 529
- **Tenants' Union** — Each state has one; search "[state] Tenants Union"
- **Fair Work Commission** — fwc.gov.au — Free employment dispute help

---

### Step 3 — Output Format

```
📍 LEGAL AID RESOURCES — [Location]
Issue Type: [Category]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━

🆓 FREE LEGAL AID

1. [Organization Name]
   Services: [What they help with]
   Eligibility: [Who qualifies]
   Contact: [Phone / Website]
   Notes: [Wait times, appointment process, etc.]

2. [Organization Name]
   ...

━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📞 HELPLINES (Call Now)

• [Helpline name]: [Number] — [What it's for]
• [Helpline name]: [Number] — [What it's for]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━

💡 TIP: When you call or visit, bring:
• ID proof
• All documents related to your issue
• Written summary of your situation (dates, names, what happened)
```

### Step 4 — Closing Encouragement
Always close with an empowering message:
> "You don't have to face this alone. These organizations exist specifically to help people
> in your situation, and many have helped thousands of people successfully resolve cases just
> like yours. Don't hesitate to reach out to multiple organizations until you find the right fit."
