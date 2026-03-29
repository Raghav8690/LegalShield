---
name: find-legal-aid
description: "Finds free and low-cost legal resources, organizations, and hotlines by user location. Covers India, US, UK, Canada, and Australia with verified contact information."
allowed-tools: Read Write
---

# Find Legal Aid Skill

## Purpose
Connect users to real, verified free and low-cost legal help organizations in their area.
Many people don't know that free legal resources exist — this skill bridges that gap.

## When to Use
Use this skill when a user needs professional legal help but can't afford it. Common triggers:
- "I can't afford a lawyer"
- "Where can I get free legal help?"
- "Are there free legal services near me?"
- "I need a lawyer but I have no money"
- "Is there legal aid in my city?"

## Execution Steps

### Step 1 — Confirm Location & Issue
- Confirm exact location: country + state/city
- Identify the type of legal issue (this determines which resources are most relevant)
- Ask if they have any income/eligibility information ready (some services are means-tested)

### Step 2 — Match to Resources

#### India 🇮🇳
| Organization | Services | Contact |
|-------------|----------|---------|
| **NALSA** (National Legal Services Authority) | Free legal aid for eligible persons | nalsa.gov.in · Helpline: 15100 |
| **State Legal Services Authorities** | Free lawyers, Lok Adalat, mediation | Search: "[state name] legal services authority" |
| **District Legal Aid Cells** | Local free legal advice | Available at every district court |
| **eDaakhil** | Online consumer complaint filing | edaakhil.nic.in |
| **Consumer Helpline** | Consumer dispute guidance | 1800-11-4000 (toll-free) |
| **National Commission for Women** | Women's legal rights and complaints | ncw.nic.in · Helpline: 7827-170-170 |
| **Lok Adalat** | Alternative dispute resolution (free) | Through NALSA / State Legal Services |
| **DLSA Free Legal Aid Clinics** | Walk-in legal consultations | At district courts across India |

**Eligibility for free legal aid (India):** SC/ST community, women, children, disabled persons,
industrial workers, persons with annual income below ₹3 lakhs, victims of human trafficking,
disaster victims, persons in custody.

#### United States 🇺🇸
| Organization | Services | Contact |
|-------------|----------|---------|
| **LawHelp.org** | Find local legal aid by state | lawhelp.org |
| **Legal Services Corporation (LSC)** | Federally funded civil legal aid | lsc.gov |
| **ABA Free Legal Answers** | Online Q&A with volunteer lawyers | abafreelegalanswers.org |
| **Local Bar Association Referral** | Reduced-fee attorney referrals | Search: "[county] bar association referral" |
| **Law School Clinics** | Free help from supervised law students | Search: "[city] law school clinic" |
| **National DV Hotline** | Domestic violence legal help | 1-800-799-7233 |
| **EEOC** | Employment discrimination complaints | eeoc.gov |
| **CFPB** | Consumer financial complaints | consumerfinance.gov/complaint |

**Income eligibility:** Most legal aid requires income ≤ 125% of federal poverty level.

#### United Kingdom 🇬🇧
| Organization | Services | Contact |
|-------------|----------|---------|
| **Citizens Advice** | Free legal information and guidance | citizensadvice.org.uk |
| **Legal Aid Agency** | Funded representation for eligible cases | gov.uk/legal-aid |
| **Law Centres** | Free specialist legal advice | lawcentres.org.uk |
| **Shelter** | Housing and homelessness legal help | shelter.org.uk · 0808 800 4444 |
| **ACAS** | Employment dispute resolution | acas.org.uk · 0300 123 1100 |
| **LawWorks** | Pro bono legal clinics | lawworks.org.uk |
| **Rights of Women** | Free legal advice for women | rightsofwomen.org.uk |

#### Canada 🇨🇦
| Organization | Services | Contact |
|-------------|----------|---------|
| **Legal Aid Ontario** | Funded legal representation | legalaid.on.ca · 1-800-668-8258 |
| **Pro Bono Ontario** | Free legal advice clinics | probonoontario.org |
| **CLEO** | Legal information resources | cleo.on.ca |
| **Law Society Referral Service** | Free 30-min consultation | lsrs.info |
| **Provincial Legal Aid** | Varies by province | Search: "[province] legal aid" |
| **Community Legal Clinics** | Free local legal services | Search: "[city] community legal clinic" |

#### Australia 🇦🇺
| Organization | Services | Contact |
|-------------|----------|---------|
| **Community Legal Centres** | Free local legal advice | clcs.org.au |
| **State Legal Aid Commissions** | Funded legal representation | Search: "[state] legal aid commission" |
| **Fair Work Commission** | Employment dispute resolution | fwc.gov.au · 13 13 94 |
| **Tenants Advice Services** | Housing and rental legal help | Search: "[state] tenants advice" |
| **Law Society Referral** | Reduced-fee consultations | Search: "[state] law society" |

### Step 3 — Provide Preparation Guidance
Always tell the user what documents to bring when contacting legal aid:
- ID (government-issued)
- Any court papers or legal notices received
- Relevant contracts, leases, or agreements
- Communications (emails, texts, letters)
- Income documentation (for eligibility check)
- Timeline of events (written out)

### Step 4 — Close with Empowerment
Always end with an encouraging, empowering message:
> "You are taking the right step by seeking help. These organizations exist specifically to help
> people in your situation. You are not alone, and you deserve legal support regardless of your
> financial situation. Reaching out takes courage — you've already taken the hardest step."

## Output Format
```
## Free Legal Resources: [Location]

**Your Location:** [City, State, Country]
**Legal Issue:** [Issue type]

### Organizations That Can Help

| Organization | What They Do | How to Reach Them |
|-------------|-------------|-------------------|
| [Name] | [Services] | [Contact info] |
...

### What to Bring When You Contact Them
📋 [Checklist of documents]

### Eligibility Notes
ℹ️ [Income requirements or other eligibility criteria]

---

💪 *You are not alone. These resources exist for you. Reaching out is the hardest step — and you've already taken it.*
```

## Tone
Warm, hopeful, and practical. Many users feel shame about not being able to afford legal help.
Counter that with dignity, validation, and concrete resources.
