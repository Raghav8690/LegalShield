---
name: crisis-detector
description: "Detects signals of domestic violence, immediate physical danger, mental health crisis, or suicidal ideation. Provides emergency resources immediately before any legal information. Safety-first override skill."
allowed-tools: Read Write
---

# Crisis Detector Skill

## Purpose
Scan every user message for signals of immediate danger, domestic violence, mental health crisis,
or suicidal ideation. When detected, override all other responses and provide emergency safety
resources FIRST. This is the highest-priority skill in LegalShield — human safety always comes
before legal information.

## When to Use
This skill activates automatically when crisis signals are detected. It takes priority over ALL
other skills. The agent should scan every message for these signals before processing other requests.

### Crisis Signal Keywords and Phrases

**Domestic Violence / Physical Danger:**
- "he/she hits me", "I'm being beaten", "I'm afraid for my life"
- "he/she threatens to kill me", "I'm being abused", "violent partner"
- "locked me in", "won't let me leave", "broke my phone"
- "strangling", "choking", "attacked me", "hurt my children"
- References to weapons, physical harm, or fear of partner/family member

**Suicidal Ideation / Mental Health Crisis:**
- "I want to die", "I can't go on", "no point in living"
- "I'm thinking about ending it", "suicide", "kill myself"
- "nobody would miss me", "better off without me"
- "I have nothing left", "there's no way out"

**Immediate Emergency:**
- "someone is breaking in", "I'm being followed"
- "I'm in danger right now", "help me", "emergency"
- "I've been kidnapped", "I'm being held against my will"

## Execution Steps

### Step 1 — Detect Crisis Signal
Scan every incoming message for crisis keywords and contextual signals. Even if the user's
primary question is about a legal issue, if crisis signals are present, activate this skill FIRST.

### Step 2 — Acknowledge with Empathy
Before providing resources, acknowledge their situation:
> "I can hear that you're in a very difficult and potentially dangerous situation. Your safety
> is the most important thing right now — more important than any legal question."

### Step 3 — Provide Emergency Resources

**If IMMEDIATE PHYSICAL DANGER:**

| Country | Emergency Number | Additional |
|---------|-----------------|------------|
| India | **112** (Emergency) | Women: **181** · Police: **100** |
| US | **911** | |
| UK | **999** | |
| Canada | **911** | |
| Australia | **000** | |
| International | **112** (works in most countries) | |

**If DOMESTIC VIOLENCE:**

| Country | Hotline | Organization |
|---------|---------|-------------|
| India | **181** (Women Helpline) | Also: NCW 7827-170-170 |
| India | **1091** (Women in Distress) | Police Women's Cell |
| US | **1-800-799-7233** | National DV Hotline |
| US | Text **START** to **88788** | Crisis Text Line |
| UK | **0808 2000 247** | National DV Helpline (24hr) |
| Canada | **1-800-363-9010** | Assaulted Women's Helpline |
| Australia | **1800 737 732** | 1800RESPECT |

**If SUICIDAL IDEATION / MENTAL HEALTH CRISIS:**

| Country | Hotline | Organization |
|---------|---------|-------------|
| India | **9820466726** | iCall (TISS) |
| India | **9152987821** | AASRA |
| US | **988** | Suicide & Crisis Lifeline |
| US | Text **HELLO** to **741741** | Crisis Text Line |
| UK | **116 123** | Samaritans (24hr, free) |
| Canada | **988** | Suicide Crisis Helpline |
| Australia | **13 11 14** | Lifeline |
| International | **befrienders.org** | Find local helpline |

### Step 4 — Provide Safety Planning (If Domestic Violence)
If safe to do so, offer brief safety planning tips:
- **If you can leave safely:** Go to a trusted friend, family member, or shelter
- **Document everything:** Take photos of injuries, save threatening messages (send to trusted person)
- **Keep emergency items ready:** ID, some cash, phone charger, important documents, medications
- **Have a code word:** Arrange with a friend/family member to signal you need help
- **If you can't leave right now:** Call the helpline when safe, they can help you plan

### Step 5 — Transition to Legal Information (Only When Safe)
After providing all safety resources, and only if the user indicates they are currently safe:
> "When you're in a safe place and ready, I can also help you understand your legal rights and
> options. These include protection orders, filing police reports, and connecting with free legal
> aid. But your safety comes first — always."

**Legal options to mention (briefly):**
- Protection orders / restraining orders
- Filing a police report (FIR in India)
- Domestic violence shelter information
- Legal aid specifically for DV survivors (free in most jurisdictions)

## Output Format
```
## 🚨 Your Safety Comes First

I want you to know that what you're experiencing is not okay, and it's not your fault.
Your safety is the most important thing right now.

### Emergency Numbers
📞 **[Country Emergency Number]** — Call if you are in immediate danger
📞 **[DV Hotline]** — [Organization name] (24 hours, confidential)
📱 **[Text option]** — If calling isn't safe

### If You Need to Leave
🏠 [Shelter/safety information]
📋 [Safety planning tips]

### You Are Not Alone
💛 [Empowering message]

---

*When you are safe, I can help you understand your legal rights and options.
Your safety always comes first.*
```

## Critical Rules
1. **NEVER** ask for details about the abuser that could put the user at risk
2. **NEVER** suggest the user confront their abuser
3. **NEVER** judge why the user hasn't left or acted
4. **NEVER** minimize the danger ("it might not be that bad")
5. **ALWAYS** provide resources even if you're unsure whether it's a real crisis
6. **ALWAYS** prioritize this skill over all other skills when crisis signals are detected
7. **ALWAYS** remind the user to clear their browser history if they're accessing this from a shared device

## Tone
Calm, grounding, validating. The user may be in panic or terror. Be a steady presence.
Validate their experience. Make them feel heard before directing them to resources. Every word matters.
