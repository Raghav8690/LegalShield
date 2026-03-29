# Example: Employment Contract Review

> This example demonstrates LegalShield's `document-analyzer` skill with red flag detection,
> fairness rating, and negotiation guidance.

---

## User Message

> "I just got a job offer and they sent me an employment contract. Can you check it before I sign?
> Here's the relevant parts:
>
> EMPLOYMENT AGREEMENT
>
> 1. POSITION: Software Developer, reporting to CTO
> 2. COMPENSATION: $85,000 annual salary, paid bi-weekly
> 3. START DATE: April 1, 2025
>
> 4. EMPLOYMENT TYPE: At-will employment. Either party may terminate this agreement at any time
>    for any reason with or without cause and with or without notice.
>
> 5. NON-COMPETE: Employee agrees not to work for any competing business, either directly or
>    indirectly, for a period of 24 months following termination of employment, within a 200-mile
>    radius of any company office location.
>
> 6. INTELLECTUAL PROPERTY: All work product, inventions, ideas, and creations made by Employee
>    during the term of employment, whether during work hours or personal time, shall be the
>    exclusive property of the Company.
>
> 7. ARBITRATION: Any disputes arising from this agreement shall be resolved exclusively through
>    binding arbitration administered by the American Arbitration Association. Employee waives
>    any right to a jury trial or class action participation.
>
> 8. SEVERANCE: None.
>
> 9. CONFIDENTIALITY: Employee shall not disclose any proprietary information for a period of
>    5 years following termination.
>
> 10. MODIFICATION: Company reserves the right to modify the terms of this agreement at any time
>     with 7 days written notice."

---

## Lex Response

Thanks for sharing this before signing — reviewing contracts before committing is one of the
smartest things you can do. I've analyzed the agreement, and I want to flag some important
concerns.

---

## Document Analysis Report

**Document Type:** Employment Contract
**Parties:** You (Employee) ↔ Company (Employer)
**Position:** Software Developer · $85,000/year

---

### 🔴 High Risk Issues (4)

**1. Excessive Non-Compete Clause (Section 5)**
> 24 months, 200-mile radius, any competing business

This is **extremely aggressive**. Most enforceable non-competes are 6-12 months with a
reasonable geographic scope. A 24-month, 200-mile restriction could effectively prevent
you from working in your field for 2 years after leaving.

**Impact:** If you leave or get fired, you may be unable to work as a software developer
for 2 years within 200 miles of any company office. At $85K salary, that's potentially
**$170,000 in lost income**.

⚠️ Note: Some states (like California) ban non-competes entirely. Check your state law.

---

**2. Binding Arbitration + Class Action Waiver (Section 7)**
> Binding arbitration only, waives jury trial and class action rights

This means if the company wrongs you (unpaid wages, discrimination, harassment), you
**cannot sue in court**. You're forced into private arbitration, which statistically favors
employers. You also can't join other employees in a class action.

**Impact:** You lose your right to a public trial and to collective legal action.

---

**3. Overbroad IP Assignment (Section 6)**
> All inventions "whether during work hours or personal time"

This clause claims ownership of **everything you create** — including personal projects,
side businesses, and open-source contributions done on your own time with your own equipment.

**Impact:** Any app, code, or invention you create at home on weekends would legally
belong to the company.

---

**4. Unilateral Modification (Section 10)**
> Company can modify terms with just 7 days notice

The company can change your compensation, job duties, non-compete terms, or any other
provision with only 7 days notice — and you have no say.

**Impact:** Your salary, role, or restrictions could be changed at any time.

---

### 🟡 Medium Risk Issues (2)

**5. At-Will with Zero Severance (Sections 4 & 8)**
While at-will employment is standard in the US, the combination of at-will + zero severance
+ aggressive non-compete is concerning. You can be fired without notice or cause, get zero
severance, AND be unable to work elsewhere for 24 months.

**6. 5-Year Confidentiality (Section 9)**
5 years is on the longer end. Standard is 2-3 years. While confidentiality clauses are normal,
the duration should be proportionate.

---

### ⚠️ Missing Protections
- ❌ **No termination notice period** — They can fire you with zero notice
- ❌ **No severance provisions** — Nothing if you're laid off
- ❌ **No overtime policy** — Important for a salaried developer position
- ❌ **No benefits details** — Health insurance, PTO, retirement not addressed
- ❌ **No IP carve-out** — No exception for personal projects on your own time

---

### ✅ Standard Clauses
- ✅ Compensation clearly stated ($85K, bi-weekly)
- ✅ Start date specified
- ✅ Reporting structure defined
- ✅ Confidentiality included (though duration is long)

---

### Fairness Rating: ⭐⭐ / Heavily One-Sided

This contract is **heavily weighted in the company's favor**. The combination of an aggressive
non-compete, binding arbitration, overbroad IP assignment, and unilateral modification rights
gives the company extraordinary control while leaving you with minimal protections.

---

### Recommended Actions

1. **Negotiate the non-compete** — Ask to reduce to 12 months maximum, narrow the geographic
   scope, and limit to truly competing businesses (not any tech company)

2. **Request an IP carve-out** — Standard language: "Excluding inventions made entirely on
   Employee's own time without use of Company resources, unless directly related to Company business"

3. **Push back on binding arbitration** — At minimum, request that the company pays all
   arbitration costs and that arbitration is in your city

4. **Request severance terms** — Industry standard: 2 weeks per year of service for layoffs

5. **Clarify benefits** — Get health insurance, PTO, sick days, and retirement details in writing

### ⚠️ Professional Recommendation

> **I strongly recommend having an employment attorney review this contract before signing.**
> With 4 high-risk issues, the potential impact on your career and income is significant.
> Many employment lawyers offer a flat-fee contract review ($200-500) — a worthwhile investment
> for protection over the life of your employment.

---

*Would you like me to help you find free or low-cost legal resources in your area for a contract
review?*

---

## What This Example Demonstrates

| Skill Used | How |
|-----------|-----|
| `document-analyzer` | Full contract analysis with 3-tier risk classification |
| `case-classifier` | Fairness rating and professional recommendation |
| `find-legal-aid` | Offered to connect with local legal resources |
