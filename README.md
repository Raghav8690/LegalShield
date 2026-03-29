# ⚖️ LegalShield Agent
> *"A lawyer in your pocket for the 99%"*

**Built for the gitagent Hackathon** · **Category:** Social Impact · **Deployed via:** clawless

[![gitagent standard](https://img.shields.io/badge/gitagent-compliant-blue)](https://gitagent.sh)
[![clawless ready](https://img.shields.io/badge/clawless-ready-orange)](https://clawless.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

## 🚨 The Problem

- **80%** of low-income individuals face their legal problems entirely alone.
- Lawyers cost **$150–$500/hour** — out of reach for most people.
- People lose their homes to illegal evictions, accept wage theft, and lose money to consumer fraud simply because they don't know their rights or the legal system terrifies them.

## 🛡️ The Solution

**LegalShield** is an AI-powered legal companion agent built on the **gitagent standard** and deployed serverlessly in the browser via **clawless**.

It democratizes access to legal knowledge. It helps everyday people understand their rights, draft basic legal correspondence, analyze contracts for risky clauses, and know exactly when they absolutely need a real lawyer.

---

## ✨ Features (Skills & Tools)

LegalShield comes with 7 carefully designed skills, functioning across 5 major jurisdictions (India, US, UK, Canada, Australia):

1. 📖 **`understand-rights`** — Explains legal rights in plain English by country/state.
2. ✉️ **`draft-letter`** — Generates demand letters, eviction disputes, and complaints with proper legal citations.
3. 📄 **`document-analyzer`** — Reads pasted contracts/NDAs and flags risky clauses (High/Medium/Low risk).
4. 🗂️ **`case-classifier`** — Determines urgency (🔴 IMMEDIATE, 🟡 MODERATE, 🟢 LOW) and whether a lawyer is required.
5. 🏛️ **`court-navigator`** — Explains small claims court & tribunal filing processes step by step.
6. 🤝 **`find-legal-aid`** — Connects users to verified free/low-cost legal resources in their specific location.
7. 🆘 **`crisis-detector` (Bonus!)** — A safety-first override skill that detects signals of domestic violence or immediate danger and provides emergency hotlines *before* giving legal info.

---

## 🚀 How to Run & Deploy

LegalShield uses the **gitagent standard** and is built to run entirely inside a browser using **Clawless** (WebContainers). No Python, no Docker, no servers required.

### Option 1: Run in Browser (Zero Install)

1. Go to [play.clawless.io](https://play.clawless.io)
2. Paste this repository URL in the top search bar: `https://github.com/Raghav8690/LegalShield`
3. Click the gear icon ⚙️ on the right side and input your `ANTHROPIC_API_KEY`.
4. Clawless will automatically boot the WebContainer, read the `agent.yaml`, and instantiate **Lex**.
5. Start chatting in the terminal at the bottom!

### Option 2: Run Locally (CLI)

```bash
# 1. Clone the repository
git clone https://github.com/Raghav8690/LegalShield
cd LegalShield

# 2. Set your API Key
export ANTHROPIC_API_KEY="sk-ant-..." 
# (Note: Use $env:ANTHROPIC_API_KEY="sk-ant-..." if using Windows PowerShell)

# 3. Install the engine globally (Highly recommended for Windows users to avoid TTY issues)
npm install -g gitclaw

# 4. Run the agent
gitclaw run
```

---

## 📚 Demo Scenarios to Try

Once the agent is running, try pasting these prompts to see the agent in action:

**Demo 1: Illegal Eviction (Rights + Crisis Detection)**
> *"My landlord told me I have 3 days to leave or he'll change the locks. I'm in Pune, Maharashtra. Can he do this? I'm really scared."*

**Demo 2: Wage Theft (Letter Drafting + Case Classifier)**
> *"My employer hasn't paid me for the last 3 weeks. They keep saying 'payroll issues'. I'm in Houston, Texas."*

**Demo 3: Contract Analysis (Document Analyzer)**
> *"I just got a job offer and they sent me an employment contract. Can you check it before I sign? It says: EMPLOYMENT TYPE: At-will employment. NON-COMPETE: Employee agrees not to work for any competing business for a period of 24 months. ARBITRATION: Binding arbitration only, no jury trial."*

*(See the `examples/` folder for transcript previews)*

---

## ⚖️ Ethics & Guardrails (`RULES.md`)

LegalShield is built with strict ethical guidelines:
- **Identity:** It explicitly states it is an AI, not a licensed attorney.
- **Safety First:** The `crisis-detector` skill overrides all logic if physical danger is detected.
- **No Legal Advice:** It provides legal *information* and *guidance*, never specific legal *advice* or outcome predictions.
- **Jurisdiction Lock:** It will not explain rights until the user's country and state are confirmed.
- **Honesty:** It will tell you if your case is weak and clearly states when you *must* hire a real lawyer.

---

## 🛠️ Repository Structure

```text
legalshield-agent/
├── agent.yaml                       # GitAgent manifest
├── SOUL.md                          # Agent persona (Lex)
├── RULES.md                         # 10 Must Always + 10 Must Never constraints
├── skills/
│   ├── understand-rights/SKILL.md
│   ├── draft-letter/SKILL.md
│   ├── document-analyzer/SKILL.md
│   ├── case-classifier/SKILL.md
│   ├── court-navigator/SKILL.md
│   ├── find-legal-aid/SKILL.md
│   └── crisis-detector/SKILL.md     # Bonus Hackathon addition
├── tools/
│   ├── jurisdiction-lookup.yaml
│   └── document-reader.yaml
├── examples/                        # Demo transcripts
└── context/                         # Original problem statement rules
```

## Team
Built for the gitagent hackathon.
