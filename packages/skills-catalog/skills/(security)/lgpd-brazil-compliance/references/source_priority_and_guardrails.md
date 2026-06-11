# Source Priority and Guardrails

This file governs **how** the skill reasons about sources and **what** conclusions it must avoid. Re-read before finalizing any report.

## 1. Official-Source-First Rule

When making an important legal or regulatory conclusion:

1. Cite the underlying **Brazilian official source** — LGPD article(s), ANPD regulation, or ANPD official guidance.
2. Do not cite this skill's internal reference files as legal authority.
3. Prefer **binding instruments** (LGPD; ANPD Resoluções) over non-binding guidance.
4. Prefer **non-binding ANPD guidance** over FAQs or educational material.
5. Prefer **FAQs / educational material from ANPD** over any non-Brazilian or unofficial source.
6. Prefer **Brazilian official sources** over GDPR-based assumptions in every case.

If you cannot identify an applicable official Brazilian source for a conclusion, **soften the conclusion** (use `unclear` or `best practice`) rather than fabricate authority.

## 2. Handling Ambiguity

When the law or ANPD position is ambiguous, silent, or context-dependent:

- Say so **explicitly** in the finding.
- Use `status: unclear` or `classification: context-dependent`.
- Describe the competing reasonable interpretations briefly.
- Suggest what additional evidence or formal legal advice would resolve the ambiguity.

Do not pick a side as if it were settled.

## 3. Handling Outdated or Unofficial Sources

- If a source you would normally cite appears outdated, moved, or replaced, **flag it** in the finding and recommend verification on the current ANPD site.
- If only unofficial materials (vendor whitepapers, law-firm articles, foreign DPA guidance) are available, **do not** use them as the basis for a mandatory legal conclusion. They can be cited as **informative context**, clearly labeled as non-official.
- Never present a third-party summary as the regulation itself.

## 4. GDPR vs. LGPD

- GDPR is **not binding in Brazil**.
- GDPR concepts may be informative, but LGPD has its own definitions, legal bases, transfer mechanisms, and incident rules.
- Where LGPD and GDPR diverge, **LGPD controls**. Examples to watch:
  - Legal bases lists differ (LGPD Art. 7 and Art. 11).
  - International transfer mechanisms follow the ANPD International Transfer regulation, not GDPR SCCs by default.
  - Incident notification follows the ANPD incident regulation, not the GDPR 72-hour rule by default.
  - "Sensitive personal data" categories under LGPD Art. 5, II differ in scope from GDPR Art. 9.

## 5. Common False Conclusions to Avoid

Hard-stop these errors:

- **Issuing a "LGPD compliant" global certification.** Never. Use the schema status values per finding: `compliant` / `partially compliant` / `non-compliant` / `unclear` / `not applicable`.
- **Treating GDPR conclusions as automatically valid in Brazil.**
- **Treating `Termos de Uso` as a universal LGPD obligation.** They are not.
- **Claiming every cookie requires consent.** ANPD Cookie Guidance distinguishes strictly necessary cookies.
- **Claiming every deletion request must erase all records immediately.** Lawful retention exceptions exist.
- **Assuming legitimate interest is a valid basis for sensitive personal data** without an official Brazilian source clearly supporting it. LGPD Art. 11 has its own list.
- **Assuming small-agent status removes core LGPD principles**, transparency duties, security expectations, or data subject rights.
- **Inventing deadlines, duties, or mandatory controls** that are not clearly supported by official Brazilian sources.
- **Merging ECA Digital, CDC, Marco Civil, sector regulation, or employment law duties into LGPD findings** without an official Brazilian source linking them.
- **Treating a RIPD as automatically mandatory** for every application. It is risk-based and context-dependent.
- **Treating ISO/SOC certifications by themselves as satisfying LGPD security duties.**

## 6. Final Pre-Submission Checklist

Before producing the final report, verify:

- [ ] Applicability under LGPD Art. 3 is analyzed and stated.
- [ ] Role classification (`controlador` / `operador` / joint / unclear) is stated for the activities reviewed.
- [ ] Evidence types available are listed; scope limitations are stated.
- [ ] Each finding has all schema fields (`area`, `status`, `severity`, `confidence`, `classification`, evidence observed, missing evidence, why it matters, remediation, official source).
- [ ] Each legal/regulatory conclusion cites an official Brazilian source (not an internal reference file).
- [ ] No certification language used.
- [ ] No GDPR assumption presented as binding in Brazil.
- [ ] Sensitive personal data treated under LGPD Art. 11, not Art. 7.
- [ ] Cookies assessed under ANPD Cookie Guidance (not "every cookie = consent").
- [ ] Adjacent legal issues are flagged as **adjacent**, not as LGPD obligations.
- [ ] Ambiguous items are marked `unclear` or `context-dependent`, with explanation.
- [ ] Open questions / missing evidence are listed.
