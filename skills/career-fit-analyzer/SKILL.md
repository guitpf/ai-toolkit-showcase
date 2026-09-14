---
name: career-fit-analyzer
description: >
  Produce a structured career fit analysis report for a specific job posting, benchmarked
  against the user's professional background. Use this skill whenever the user shares a job
  description and asks whether to apply, how to tailor their materials, how to prepare for
  interviews, or any variation of "should I go for this role?" — even if they don't use the
  word "fit" explicitly. Also trigger when the user pastes a job ad and asks for feedback,
  gap analysis, or differentiators. Always use this skill for job evaluation tasks; do not
  attempt to freehand career analysis without it.
---

# Career Fit Analyzer

A skill for senior career strategist–style analysis of job postings against the user's profile.
Output is a structured, direct report with five named sections. No sugarcoating. Quantify wherever
possible. Write as a senior career strategist who respects the user's time.

---

## Required inputs

Before producing the report, confirm you have both:

1. **The job posting** — full text preferred; URL acceptable if you can fetch it.
2. **The user's profile** — CV/résumé, LinkedIn summary, or a freeform description of their
   background, tools, and experience. If the user's background is already known from memory,
   use it but confirm any critical details that could affect the analysis (current title, YoE,
   specific tools used).

If either is missing, ask for it before proceeding. Do not produce a speculative report.

---

## Output format

Deliver the report in five sections, in this exact order. Use H2 headings. Be direct and specific.

---

### 1. Fit Verdict

**Format:** One-line verdict (`Strong / Moderate / Weak match`) followed by 2–3 sentences of
rationale, ending with an explicit `→ Apply` or `→ Do not apply` recommendation.

**Guidance:**
- Base the verdict on hard skills overlap, seniority alignment, and culture/values fit combined.
- "Strong" = 80%+ overlap, no disqualifying gaps.
- "Moderate" = 60–80% overlap or one meaningful gap that is reframeable.
- "Weak" = <60% overlap or a structural mismatch (seniority, industry, geography, etc.).

---

### 2. Hard Skills & Tools Match

**Format:** Side-by-side comparison table with three columns:

| What the role requires | What the user brings | Match level |
|---|---|---|

**Match levels:** ✅ Exact match · 🟡 Partial match · ❌ Missing

**Guidance:**
- List every tool or platform explicitly named in the JD (e.g., Meta Ads Manager, GA4, TikTok Ads,
  Google Ads, Power BI, Looker, Klaviyo, Salesforce, etc.).
- For partial matches, briefly note the gap (e.g., "uses GA4 but not certified" or "knows Meta but
  not TikTok Ads Manager specifically").
- Flag any tool marked ❌ that is listed as a *must-have* vs. *nice-to-have* in the JD — these
  are higher-risk gaps.

---

### 3. Soft Skills, Culture & Values Fit

**Format:** Prose with embedded comparisons. 3–5 paragraphs max.

**Guidance:**
- Identify culture signals in the JD (startup vs. corporate, ownership mindset, speed, data-driven,
  collaborative, international, etc.).
- Map the user's working style, background, and international experience to those signals.
- Be explicit about where the fit is strong and where it is ambiguous or weak.
- Note any red flags (e.g., role requires heavy in-office presence, user prefers remote).

---

### 4. Top 3 Differentiators to Lead With

**Format:** Numbered list. One clear differentiator per item, with a 1–2 sentence explanation of
*why it matters to this specific role/company*, not just why it's impressive in general.

**Guidance:**
- Differentiators must be specific to this JD and this hiring manager's likely priorities.
- Avoid generic strengths ("hard worker", "fast learner"). Ground each in evidence from the user's
  background.
- Order by likely impact on the hiring decision.

---

### 5. Gaps & Reframing Strategies

**Format:** Numbered list. For each gap: name it honestly, then give concrete reframing language
(for CV, cover letter, or interview).

**Guidance:**
- Include all ❌ and key 🟡 items from Section 2 that are material to the role.
- Also include soft/structural gaps (e.g., industry switch, seniority mismatch, shorter tenure).
- Reframing language should be copy-pasteable or close to it — not abstract advice.
- If a gap is genuinely disqualifying, say so. Don't spin the unspinnable.

---

## Tone & style

- Senior, direct, specific. Like a trusted advisor who has seen 500 hiring processes.
- No filler phrases ("Great question!", "It's worth noting that...").
- Quantify wherever the user's background allows (revenue managed, team size, % growth, etc.).
- Use the user's actual job titles and company names — don't genericize.
- When writing in German context (German job market, German-language JD), note any German-specific
  conventions (e.g., Anschreiben expectations, Lebenslauf format, seniority norms).

---

## Edge cases

- **JD is vague or missing key details:** Work with what's there; flag the ambiguity explicitly in
  the relevant section rather than fabricating requirements.
- **User profile is thin:** Ask one focused follow-up question to get the most critical missing
  piece (usually: YoE in the core discipline, or specific tools used).
- **Role is in a different country/language than the user:** Add a brief note in Section 3 on
  relocation, visa, or language requirements if relevant.
- **User asks for CV/cover letter tailoring after the report:** That is a separate task. Complete
  the fit report first, then offer to move to materials.
