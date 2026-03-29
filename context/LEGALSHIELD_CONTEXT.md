# LegalShield Agent — Complete Project Documentation

> **Hackathon Submission | gitagent Standard | Deployed via clawless**
> Built for the gitagent Hackathon · Category: Social Impact · Domain: Legal Access

---

## Table of Contents

1. [Project Overview](#1-project-overview)
2. [The Problem We Solve](#2-the-problem-we-solve)
3. [Solution Architecture](#3-solution-architecture)
4. [Agent Identity — Meet Lex](#4-agent-identity--meet-lex)
5. [Complete Feature List](#5-complete-feature-list)
6. [Skills — Deep Dive](#6-skills--deep-dive)
7. [Repository Structure](#7-repository-structure)
8. [Hackathon Compliance](#8-hackathon-compliance)
9. [Technical Stack](#9-technical-stack)
10. [Deployment Guide](#10-deployment-guide)
11. [Demo Scenarios](#11-demo-scenarios)
12. [Limitations & Ethics](#12-limitations--ethics)
13. [Future Roadmap](#13-future-roadmap)

---

## 1. Project Overview

**LegalShield** is an AI-powered legal companion agent that lives in a git repo, defined using the
**gitagent standard**, brought to life with **gitclaw**, and deployed serverlessly in the browser
via **clawless**.

LegalShield democratizes access to legal knowledge for the billions of people who face legal
problems every year but cannot afford an attorney. It helps users understand their rights,
draft legal letters, analyze documents for risky clauses, navigate court processes, and — most
importantly — know exactly when they need a real lawyer.

**One-line pitch:**
> *"A lawyer in your pocket for the 99% — free, instant, and available in every browser."*

---

## 2. The Problem We Solve

### The Justice Gap Is Massive

- **80%** of low-income individuals in the US face their legal problems entirely alone
- **1.5 billion** people globally have an unmet civil legal need every year (World Justice Project, 2023)
- The average cost of an attorney in the US ranges from **$150–$500/hour** — out of reach for most
- In India, millions face tenant evictions, wage theft, and consumer fraud with zero legal recourse
- Legal aid organizations are severely understaffed and overwhelmed

### The Consequences Are Real

- Families lose their homes due to illegal evictions they didn't know they could fight
- Workers accept non-payment of wages because they don't know their rights
- Consumers lose money to fraud because the complaint process seems too complicated
- Tenants live in uninhabitable conditions because they fear the legal system

### Existing Solutions Fall Short

| Existing Solution | Problem |
|---|---|
| Google Search | Generic, not personalized, contradictory results |
| LegalZoom / Rocket Lawyer | Expensive subscriptions, US-only, still confusing |
| Law firm websites | Marketing-focused, not actionable |
| Government websites | Complex, bureaucratic, hard to navigate |
| General AI assistants | Not specialized, no legal document skills, no safety guardrails |

**LegalShield fills this gap** with a purpose-built, safety-first, jurisdiction-aware AI agent.

---

## 3. Solution Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                    LegalShield Agent                         │
│                  (gitagent Standard)                         │
├─────────────────┬───────────────────────────────────────────┤
│   SOUL.md       │  Agent Identity: Lex                       │
│                 │  Warm, knowledgeable, non-judgmental       │
├─────────────────┼───────────────────────────────────────────┤
│   RULES.md      │  Hard Constraints                          │
│                 │  Safety-first, jurisdiction-aware,         │
│                 │  never gives specific legal advice         │
├─────────────────┼───────────────────────────────────────────┤
│   agent.yaml    │  Manifest: name, model, skills, tags       │
├─────────────────┼───────────────────────────────────────────┤
│   skills/       │  6 Core Skills (see Section 6)             │
│                 │  understand-rights, draft-letter,          │
│                 │  document-analyzer, case-classifier,       │
│                 │  court-navigator, find-legal-aid           │
└─────────────────┴───────────────────────────────────────────┘
         │                          │
         ▼                          ▼
   gitclaw SDK                  clawless
  (Node.js runtime)       (Browser / WebContainer)
         │                          │
         └──────────┬───────────────┘
                    ▼
           Running LegalShield Agent
           Accessible in any browser
```

---

## 4. Agent Identity — Meet Lex

The LegalShield agent is named **Lex** — a knowledgeable, calm, and empathetic legal companion.

### Personality Traits

- **Calm under pressure** — Users come in crisis; Lex is always steady and grounding
- **Empathy-first** — Always acknowledges stress before diving into legal details
- **Plain-language specialist** — Translates legalese into everyday language
- **Honest about limits** — Never overpromises; clearly distinguishes information from advice
- **Action-oriented** — Every response ends with clear, concrete next steps

### What Makes Lex Different From a General AI

| Capability | General AI | Lex (LegalShield) |
|---|---|---|
| Legal domain depth | Broad but shallow | Deep and specialized |
| Jurisdiction awareness | Often ignores it | Always confirms location first |
| Safety guardrails | Generic | Crisis detection + safety escalation |
| Document skills | None | Analyzes, drafts, explains legal docs |
| Legal ethics compliance | None | Built into RULES.md |
| Court navigation | None | Step-by-step process guidance |

---

## 5. Complete Feature List

### Core Features

#### F1 — Rights Explainer
- Explains legal rights in plain language for any situation
- Jurisdiction-aware (India, US, UK, Canada, Australia)
- Covers: housing, employment, consumer, family, criminal, immigration
- Cites relevant laws and statutes by name

#### F2 — Legal Letter Drafter
- Generates professional legal correspondence
- Types: demand letters, eviction dispute letters, employer complaints,
  consumer fraud complaints, cease & desist notices, security deposit demands
- Customizable with user's specific details
- Includes proper legal language and citation of applicable law

#### F3 — Document Analyzer
- Reads contracts, lease agreements, employment offers, terms of service
- Flags risky clauses (one-sided arbitration, unfair termination, hidden fees)
- Summarizes key terms in plain language
- Rates document fairness and highlights top concerns

#### F4 — Case Classifier & Urgency Detector
- Evaluates the user's situation description
- Classifies: civil vs criminal, dispute type, jurisdiction
- Determines urgency level (immediate action needed / moderate / low)
- Provides honest assessment of case strength
- Tells users definitively when they need a real lawyer

#### F5 — Court Navigator
- Step-by-step guidance for navigating court processes
- Covers: small claims, civil court, family court, employment tribunal
- Explains: filing procedures, deadlines, what to bring, how to present a case
- Provides checklists and document preparation guidance

#### F6 — Legal Aid Finder
- Finds free and low-cost legal resources by location
- Connects users to: legal aid organizations, bar association referral programs,
  law school clinics, NGO legal services, government legal help desks
- Provides hotlines, websites, and physical addresses where available

### Safety Features

#### S1 — Crisis Detection
- Scans every message for signals of domestic violence, immediate danger, or mental health crisis
- Triggers immediate safety resource response when detected
- Provides local emergency numbers, hotlines, shelter resources

#### S2 — Legal Ethics Guardrails (RULES.md enforcement)
- Never claims to be a lawyer
- Never makes outcome predictions
- Always recommends professional counsel for serious matters
- Never assists with illegal activity

#### S3 — Jurisdiction Lock
- Requires location confirmation before giving jurisdiction-specific advice
- Flags when laws differ significantly between locations
- Defaults to general principles when jurisdiction is unclear

### User Experience Features

#### U1 — Plain Language Mode
- All legal explanations default to plain language
- Legal terms are always immediately explained when used
- Readability tuned to general adult reading level

#### U2 — Step-by-Step Guidance
- Complex processes always broken into numbered steps
- Progress acknowledgment ("You've completed step 1, now here's step 2...")
- Never overwhelming — pacing adapted to user's apparent stress level

#### U3 — Document Download Ready
- Drafted letters formatted for immediate use
- Includes placeholders clearly marked for user customization
- Professional formatting suitable for official submission

---

## 6. Skills — Deep Dive

### Skill 1: `understand-rights`

```yaml
name: understand-rights
description: "Explains legal rights in plain language for any situation and jurisdiction"
allowed-tools: Read Write
```

**What it does:**
Takes a user's described situation and jurisdiction, identifies the relevant area of law,
and explains their rights clearly with citations to applicable statutes.

**Input:** Natural language description of situation + country/state
**Output:** Plain language rights explanation + relevant law citations + next steps

**Example trigger:** *"My landlord hasn't returned my security deposit after 45 days. I'm in Mumbai, India."*

---

### Skill 2: `draft-letter`

```yaml
name: draft-letter
description: "Drafts professional legal correspondence for disputes and formal complaints"
allowed-tools: Read Write
```

**What it does:**
Generates professional, legally appropriate letters for common dispute scenarios.
Uses proper legal language, cites applicable law, and customizes to the user's specifics.

**Letter types supported:**
- Security deposit demand letter
- Eviction dispute notice
- Employer wage claim letter
- Consumer fraud complaint
- Cease & desist notice
- Insurance claim dispute
- Academic appeal letter
- GDPR/data deletion request

**Input:** Situation details, user name, recipient details, jurisdiction
**Output:** Complete, ready-to-send letter with instructions for delivery

---

### Skill 3: `document-analyzer`

```yaml
name: document-analyzer
description: "Analyzes contracts and legal documents to identify risky clauses and summarize key terms"
allowed-tools: Read Write
```

**What it does:**
Reviews provided legal documents and extracts key terms, flags concerning clauses,
rates overall fairness, and explains everything in plain language.

**Documents handled:**
- Rental/lease agreements
- Employment contracts
- Service agreements / Terms of Service
- Loan agreements
- Non-disclosure agreements (NDAs)
- Franchise agreements

**Red flags it detects:**
- Unilateral contract modification clauses
- One-sided arbitration requirements (waives your right to sue)
- Automatic renewal with difficult cancellation
- Excessive penalty clauses
- Unfair jurisdiction selection (forces disputes in distant location)
- Missing tenant/employee protections required by law

---

### Skill 4: `case-classifier`

```yaml
name: case-classifier
description: "Classifies legal situations, assesses urgency, and determines whether professional legal help is needed"
allowed-tools: Read Write
```

**What it does:**
Evaluates user's described situation and produces a structured assessment including
type of legal issue, urgency level, realistic case strength, and professional referral guidance.

**Urgency levels:**
- 🔴 **IMMEDIATE** — Statute of limitations deadline near, active emergency, criminal charge
- 🟡 **MODERATE** — Dispute in progress, deadline within 30 days, ongoing violation
- 🟢 **LOW** — Informational, dispute not yet filed, preventive guidance

**Output includes:**
- Legal issue category and subcategory
- Jurisdiction confirmed
- Urgency rating with explanation
- Honest case strength assessment (Weak / Moderate / Strong)
- Clear professional lawyer recommendation (Yes/No + reason why)
- Immediate next 3 actions

---

### Skill 5: `court-navigator`

```yaml
name: court-navigator
description: "Provides step-by-step guidance for navigating court processes including small claims, civil, and employment tribunals"
allowed-tools: Read Write
```

**What it does:**
Guides users through the complete process of taking a matter to court — from deciding
whether to file, to preparing documents, to what to say on the day.

**Court types covered:**
- Small claims court (US, India, UK, Canada)
- Civil court (basic procedures)
- Employment tribunal / labor court
- Consumer disputes forum (India-specific)
- Family court basics

**Guidance provided:**
- Eligibility and jurisdictional limits (e.g., small claims max amounts by state)
- How and where to file
- Filing fees and fee waiver eligibility
- Documents to prepare and organize
- How to serve the opposing party
- What to expect on court day
- How to present your case simply and effectively
- What to do if you win (enforcement) or lose (appeals)

---

### Skill 6: `find-legal-aid`

```yaml
name: find-legal-aid
description: "Finds free and low-cost legal resources, organizations, and hotlines by user location"
allowed-tools: Read Write
```

**What it does:**
Connects users to real legal help organizations in their area — from government-funded
legal aid to NGOs, law school clinics, and pro bono programs.

**Resources by country:**
- **India:** NALSA, State Legal Services Authorities, district legal aid cells, NGO partners
- **US:** Legal Aid Society, LAWHELP.org, local bar association referral programs, law school clinics
- **UK:** Citizens Advice, Legal Aid Agency, law centers
- **Canada:** Legal Aid Ontario, CLEO, law school clinics
- **Australia:** Community Legal Centres, Legal Aid commissions by state

**Output format:**
- Organization name
- Services offered
- Eligibility criteria (income-based, issue-based)
- Contact information (phone, website, address)
- Estimated wait times where known

---

## 7. Repository Structure

```
legalshield-agent/
├── agent.yaml                    # Agent manifest
├── SOUL.md                       # Agent identity: Lex
├── RULES.md                      # Hard constraints and ethical guardrails
├── README.md                     # This file
├── LEGALSHIELD_CONTEXT.md        # Full project context (this document)
│
├── skills/
│   ├── understand-rights/
│   │   └── SKILL.md
│   ├── draft-letter/
│   │   └── SKILL.md
│   ├── document-analyzer/
│   │   └── SKILL.md
│   ├── case-classifier/
│   │   └── SKILL.md
│   ├── court-navigator/
│   │   └── SKILL.md
│   └── find-legal-aid/
│       └── SKILL.md
│
├── tools/
│   ├── jurisdiction-lookup.yaml  # Tool schema for jurisdiction resolution
│   └── document-reader.yaml     # Tool schema for document ingestion
│
└── examples/
    ├── eviction-dispute.md       # Example conversation
    ├── wage-theft-claim.md       # Example conversation
    └── contract-review.md       # Example conversation
```

---

## 8. Hackathon Compliance

This project fully satisfies all requirements of the gitagent hackathon:

| Requirement | LegalShield Implementation |
|---|---|
| ✅ **gitagent standard** | Full `agent.yaml`, `SOUL.md`, `RULES.md` defined |
| ✅ **agent.yaml manifest** | Name, version, description, model, skills, tags all defined |
| ✅ **SOUL.md identity** | Detailed personality, values, expertise, communication style |
| ✅ **RULES.md constraints** | 10 Must Always + 10 Must Never rules — legally critical |
| ✅ **skills/ directory** | 6 fully defined skills with YAML frontmatter + instructions |
| ✅ **gitclaw compatible** | Node-compatible skills, standard runtime |
| ✅ **clawless deployment** | Node.js only, no Python, no binaries — fully WebContainer ready |
| ✅ **Real-world problem** | Solves the global legal access crisis — 1.5 billion underserved |
| ✅ **Validated** | `npx gitagent validate` passes |

---

## 9. Technical Stack

| Component | Technology |
|---|---|
| Agent Standard | gitagent v0.1.0 |
| Runtime | gitclaw (Node.js) |
| Serverless Deployment | clawless (WebContainers) |
| AI Model | claude-sonnet-4-5-20250929 |
| Skills Format | YAML frontmatter + Markdown instructions |
| Tools Format | YAML schema definitions |
| Document Handling | Node.js compatible text processing |
| Browser Compatibility | All modern browsers via WebContainers |

### Why clawless Works for LegalShield

All LegalShield skills are designed to be Node.js compatible:
- No Python dependencies
- No system binaries (no `apt-get`, no Docker)
- No file system writes beyond conversation state
- Text processing via pure Node.js
- Document analysis via text input (paste content) — no binary parsing needed

---

## 10. Deployment Guide

### Local Development

```bash
# Clone the repo
git clone https://github.com/your-org/legalshield-agent
cd legalshield-agent

# Install gitclaw
npm install gitclaw

# Validate the agent
npx gitagent validate
npx gitagent info

# Run locally
npx gitclaw run
```

### Browser Deployment (clawless)

```bash
# Install clawless
npm install clawless

# Deploy to browser
npx clawless deploy

# Access at the provided URL — zero infrastructure required
```

### Environment Notes

- Requires Node.js 18+
- No API keys needed in repo (handled by gitclaw runtime)
- No external service dependencies for core skills
- Optional: Add jurisdiction lookup API key for enhanced legal resource finding

---

## 11. Demo Scenarios

These scenarios demonstrate LegalShield's capabilities in a hackathon demo context.

### Demo 1: Illegal Eviction (India)
> *User: "My landlord told me I have 3 days to leave or he'll change the locks. I'm in Pune, Maharashtra. Can he do this?"*

**Lex response flow:**
1. Confirms jurisdiction (Maharashtra, India)
2. Explains that self-help eviction (changing locks without court order) is illegal under Maharashtra Rent Control Act
3. Explains tenant's rights — landlord must file in court
4. Offers to draft a cease & desist letter to the landlord
5. Provides contact for Maharashtra Rent Control Authority
6. Urgency: 🔴 IMMEDIATE — advises documenting threats

---

### Demo 2: Unpaid Wages (US)
> *User: "My employer hasn't paid me for the last 3 weeks. They keep saying 'payroll issues'. I'm in Texas."*

**Lex response flow:**
1. Confirms jurisdiction (Texas, US)
2. Explains Texas Payday Law — employer must pay wages on scheduled payday
3. Explains right to file a wage claim with Texas Workforce Commission
4. Offers to draft a formal wage demand letter to employer
5. Provides Texas TWC wage claim filing link and deadline (180 days from due date)
6. Urgency: 🟡 MODERATE — deadline clock is running

---

### Demo 3: Contract Review
> *User: [pastes employment contract] "Can you check this contract before I sign it?"*

**Lex response flow:**
1. Analyzes pasted contract text
2. Flags: mandatory arbitration clause (waives right to sue), 12-month non-compete (overly broad), at-will termination with no severance
3. Summarizes: 3 major red flags, 2 minor concerns, 4 standard clauses
4. Suggests negotiation points
5. Recommends attorney review before signing given red flags

---

### Demo 4: Consumer Fraud (UK)
> *User: "I paid £800 for a laptop from an online seller. It arrived broken. They're refusing to refund. UK."*

**Lex response flow:**
1. Confirms jurisdiction (UK)
2. Explains Consumer Rights Act 2015 — item must be of satisfactory quality
3. Explains right to full refund within 30 days, or repair/replacement after
4. Offers to draft formal complaint letter to seller citing the Act
5. Explains chargeback process through bank as parallel option
6. Provides Citizens Advice contact and Trading Standards reporting link

---

## 12. Limitations & Ethics

### What LegalShield Is

- A legal information and guidance tool
- An empowerment resource for people to understand their rights
- A document drafting assistant for common legal correspondence
- A navigation guide for public legal processes
- A triage tool for determining when professional help is needed

### What LegalShield Is Not

- A licensed attorney or law firm
- A substitute for professional legal representation in serious matters
- A legal advice service (legal advice = advice specific to your case from a licensed attorney)
- A substitute for emergency services in crisis situations

### Ethical Commitments

1. **Transparency** — Always identifies as AI; never impersonates a lawyer
2. **Safety** — Crisis situations always trigger immediate safety resources first
3. **Honesty** — Will tell users when their case is weak or when they genuinely need a lawyer
4. **Privacy** — Minimizes personal data collection; does not retain sensitive details
5. **Accessibility** — Plain language, no legal jargon, available in any browser for free
6. **Non-discrimination** — Provides equal quality assistance regardless of the user's background

---

## 13. Future Roadmap

### Phase 2 (Post-Hackathon)
- **Multilingual support** — Hindi, Marathi, Tamil, Spanish, French
- **Voice interface** — For users with low literacy
- **WhatsApp bot integration** — Reach users without browser access
- **Offline mode** — Downloadable rights guides for areas with poor connectivity

### Phase 3
- **Real lawyer connection** — Verified pro bono attorney matching
- **Case tracking** — Follow a dispute from start to resolution
- **Community legal wiki** — Crowdsourced jurisdiction-specific guidance
- **NGO partnerships** — Integration with legal aid networks globally

### Phase 4
- **Courthouse document filing** — Direct integration with e-filing systems
- **AI-powered hearing prep** — Mock question and answer preparation
- **Multi-jurisdiction support** — International legal comparison tools

---

## About This Document

This document (`LEGALSHIELD_CONTEXT.md`) serves two purposes:

1. **For hackathon judges** — A complete explanation of the project, its problem statement,
   technical implementation, and feature set.

2. **For the AI agent (Lex)** — When provided as context to the LegalShield agent, this document
   gives the AI full awareness of its scope, capabilities, limitations, skills, and ethical
   commitments. The AI should use this document to understand what it can and cannot do,
   which skill to invoke for which situation, and how to represent itself accurately to users.

---

*LegalShield — Justice for Everyone.*
*Built with gitagent · Powered by gitclaw · Deployed with clawless*
