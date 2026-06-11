---
name: lgpd-brazil-compliance
description: Review products, services, codebases, flows, and privacy documents for apparent alignment with Brazil's LGPD and current ANPD guidance, then produce evidence-based findings with severity, confidence, classification, and official Brazilian citations. Use when the user asks to "review LGPD", "audit LGPD", "LGPD compliance check", "adequação à LGPD", "review privacy policy under Brazilian law", "review aviso de privacidade", "verify cookie banner LGPD", "auditar banner de cookies", "review data subject rights", "RIPD assessment", "review international transfers Brazil", or "incident notification ANPD". Do NOT use for GDPR-only reviews, formal legal opinions or certifications, pure cybersecurity audits, or non-LGPD sector-specific reviews unless directly adjacent to an LGPD issue.
license: CC-BY-4.0
metadata:
  author: Lucas Martins - github.com/lucassena
  source: https://github.com/lucassena/lgpd-brazil-compliance-skill
  version: '1.0.0'
---

# LGPD (Brazil) Compliance Review

Review whether a product, service, codebase, privacy flow, or privacy document appears aligned with Brazil's LGPD (Lei nº 13.709/2018) and current ANPD guidance. This skill produces structured compliance findings and remediation guidance, but it does not provide formal legal advice or a certification of compliance.

## Quick Start

1. Identify the review target and the evidence available.
2. Start every review by reading [./references/applicability_and_scope.md](./references/applicability_and_scope.md).
3. Load only the reference files needed for the current scope.
4. Produce findings using the schema in [./references/findings_schema.md](./references/findings_schema.md).
5. Cite the underlying Brazilian official sources, not these internal references.

## Required Inputs

Provide at least one of the following:

- Source code or repository areas to review.
- Privacy documents such as `Aviso de Privacidade`, Privacy Policy, Cookie Policy, DPA, or internal policies.
- Screenshots, UI flows, or a product description.
- A specific LGPD-related question about a behavior, feature, or document.

## Helpful Optional Inputs

- Product and business context, especially B2C vs. B2B.
- Whether the product targets users located in Brazil.
- Categories of personal data collected, especially sensitive personal data.
- Whether children or adolescents are likely users.
- Cookies, analytics, or advertising trackers in use.
- Third-party processors, subprocessors, or international vendors.
- Whether solely automated decisions with legal or significant effects exist.
- Existing role classification such as `controlador` or `operador`.
- Whether an `encarregado` is appointed.

## Workflow

### 1. Confirm applicability and scope first

Before producing any finding:

- Determine whether the target processes personal data at all.
- Analyze LGPD territorial applicability under Article 3.
- Check exclusions under Article 4 before proceeding.
- Classify the organization's role as `controlador`, `operador`, joint, or unclear.
- State the evidence types available and the limits they impose.

Read [./references/applicability_and_scope.md](./references/applicability_and_scope.md) at the start of every review.

If the target genuinely does not process personal data, say so and stop instead of forcing a 15-area review.

### 2. Ask only the clarifying questions that matter

Ask for more context only when it materially changes the review. Typical high-value questions include:

- Does the product target users in Brazil?
- What categories of personal data are processed?
- Is sensitive personal data involved?
- Are children or adolescents likely users?
- Are there international vendors or subprocessors?
- Are there solely automated decisions with legal or significant effects?

If the user prefers to proceed with incomplete information, continue with explicit assumptions and mark uncertain conclusions as `unclear`.

### 3. Gather evidence and separate fact from inference

For each topic in scope, track three buckets:

- Confirmed evidence observed in code, documents, UI, or behavior.
- Missing evidence that would change the conclusion.
- Reasonable inference, clearly labeled as inference.

Never present inference as confirmed evidence.

### 4. Review the relevant LGPD areas

Walk through the relevant parts of the 15-area framework in [./references/review_areas.md](./references/review_areas.md):

1. Transparency and notices.
2. Legal basis and purpose limitation.
3. Sensitive personal data.
4. Cookies and tracking technologies.
5. Data subject rights.
6. Account lifecycle and user controls.
7. Data retention and disposal.
8. Security and privacy safeguards.
9. Incident response and breach communication.
10. Governance and accountability.
11. Records of processing activities.
12. RIPD and high-risk processing.
13. Children and adolescents.
14. International transfers.
15. Automated decisions and profiling.

Skip an area only when it is clearly out of scope, and say why.

### 5. Write findings in the required schema

Use the schema in [./references/findings_schema.md](./references/findings_schema.md). Every finding must include:

- `area`
- `status`
- `severity`
- `confidence`
- `classification`
- `evidence observed`
- `missing evidence`
- `why it matters`
- `recommended remediation`
- `official source reference`

Use only these status values: `compliant`, `partially compliant`, `non-compliant`, `unclear`, or `not applicable`.
Use `severity: none` when `status` is `not applicable`.

### 6. Follow source-priority guardrails

When stating a legal or regulatory conclusion:

- Cite the underlying Brazilian official source such as LGPD text, ANPD regulation, or ANPD official guidance.
- Do not cite this skill's internal references as authority.
- Prefer binding instruments over non-binding guidance.
- Prefer ANPD materials over GDPR-based assumptions.
- If no official Brazilian source clearly supports a hard conclusion, soften the finding instead of inventing authority.

Re-read [./references/source_priority_and_guardrails.md](./references/source_priority_and_guardrails.md) before finalizing the report.

Use [./references/official_sources.md](./references/official_sources.md) as a navigation aid when choosing the correct official source to cite.

## Output Format

Produce the review in this order:

1. Executive summary in 3 to 8 lines, without certification language.
2. Scope and assumptions.
3. Applicability analysis.
4. Findings by area.
5. Priority risks.
6. Remediation checklist.
7. Open questions or evidence needed.
8. Official source references.

## Guardrails

- Do not issue a global verdict such as "LGPD compliant".
- Do not provide formal legal advice.
- Do not treat GDPR conclusions as automatically valid in Brazil.
- Do not claim that `Termos de Uso` are universally required by LGPD.
- Do not claim that every cookie requires consent.
- Do not claim that every deletion request requires immediate full erasure.
- Do not assume legitimate interest is valid for sensitive personal data unless an official Brazilian source clearly supports that conclusion.
- Do not invent deadlines, duties, or mandatory controls without an official Brazilian source.
- Do not merge adjacent regimes such as consumer law, ECA Digital, Marco Civil da Internet, health regulation, or employment law into LGPD findings unless an official Brazilian source clearly links them.
- If the available evidence is incomplete, say so explicitly and list what is missing.

## Reference Loading Guide

| Reference file                                                                                   | Read when                                                                                                                             |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------- |
| [./references/applicability_and_scope.md](./references/applicability_and_scope.md)               | At the start of every review, and again when classifying roles or scoping code-only, docs-only, screenshot-only, or mixed reviews.    |
| [./references/review_areas.md](./references/review_areas.md)                                     | When assessing the substantive LGPD areas, especially cookies, sensitive personal data, incident response, governance, and transfers. |
| [./references/findings_schema.md](./references/findings_schema.md)                               | When drafting or normalizing findings.                                                                                                |
| [./references/official_sources.md](./references/official_sources.md)                             | When identifying the correct official Brazilian source to cite.                                                                       |
| [./references/source_priority_and_guardrails.md](./references/source_priority_and_guardrails.md) | Whenever ambiguity appears, unofficial material conflicts with Brazilian sources, or the conclusion may overstate certainty.          |

## Examples

### Example 1: Cookie banner review

User says: "Review our cookie banner for LGPD."

Actions:

1. Read applicability and scope.
2. Inspect the UI flow and any cookie policy provided.
3. Load the cookies section in `review_areas.md`.
4. Use `findings_schema.md` to structure the result.
5. Cite ANPD cookie guidance and any directly relevant LGPD provisions.

Result:

A focused report that states whether the banner appears balanced, whether non-essential cookies seem disabled by default, what evidence is missing, and what remediation is recommended.

### Example 2: Privacy policy review

User says: "Can you review this aviso de privacidade under Brazilian law?"

Actions:

1. Read applicability and scope.
2. Review the document for transparency, legal basis, sharing, retention, rights, and transfer disclosures.
3. Load the relevant sections from `review_areas.md`.
4. Cite LGPD Articles 7, 9, 18, 33 to 36, and any ANPD materials actually used.

Result:

A document-centered LGPD review that distinguishes confirmed policy language from operational gaps that cannot be verified from the document alone.

### Example 3: Incident notification readiness

User says: "Assess whether this breach playbook is ANPD-ready."

Actions:

1. Read applicability and scope.
2. Inspect the incident plan, role assignments, and communication paths.
3. Load the incident response and governance sections in `review_areas.md`.
4. Confirm the finding structure in `findings_schema.md`.
5. Use `official_sources.md` to navigate to the ANPD incident regulation and related LGPD provisions.

Result:

A targeted readiness assessment covering reportability criteria, deadlines, `controlador` and `operador` responsibilities, and missing operational evidence.

## Troubleshooting

### There is not enough evidence to conclude

State the evidence gap, keep the scope explicit, and use `unclear` where appropriate. Do not guess.

### An unofficial source conflicts with ANPD or LGPD materials

Prefer the official Brazilian source. If the official source is ambiguous, say so and downgrade the certainty of the conclusion.

### The review surfaces adjacent legal issues

Flag them as adjacent and separate from LGPD findings unless an official Brazilian source clearly links the duty to LGPD.
