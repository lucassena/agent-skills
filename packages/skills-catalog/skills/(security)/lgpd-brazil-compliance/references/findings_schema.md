# Findings Schema

Every finding must follow this schema. Cite the underlying official Brazilian source (LGPD article, ANPD regulation, or ANPD guidance), not this skill's internal reference files.

## Fields

| Field                       | Required | Allowed values / format                                                                                                                    |
| --------------------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| `area`                      | yes      | One of the 15 review areas (or a clearly named sub-area).                                                                                  |
| `status`                    | yes      | `compliant` / `partially compliant` / `non-compliant` / `unclear` / `not applicable`                                                       |
| `severity`                  | yes      | `high` / `medium` / `low` / `none` (`none` should be used when `status` is `not applicable`)                                               |
| `confidence`                | yes      | `high` / `medium` / `low`                                                                                                                  |
| `classification`            | yes      | `legal requirement` / `ANPD regulation` / `ANPD guidance` / `best practice` / `context-dependent`                                          |
| `evidence observed`         | yes      | Concrete facts from code, docs, UI, or context.                                                                                            |
| `missing evidence`          | yes      | What additional input would change the conclusion.                                                                                         |
| `why it matters`            | yes      | Practical impact on `titulares`, regulator exposure, or operational risk.                                                                  |
| `recommended remediation`   | yes      | Actionable, proportionate steps. If `status` is `not applicable`, use `none` with a short justification or monitoring note only if useful. |
| `official source reference` | yes      | LGPD article(s) or ANPD instrument(s); include title and, when possible, URL and date.                                                     |

## Status Definitions

- **compliant** — Reviewed evidence appears **aligned** with the applicable LGPD/ANPD requirement or guidance. Never used to issue a formal certification.
- **partially compliant** — Some elements appear aligned; others are missing or weak.
- **non-compliant** — Reviewed evidence appears **not aligned** with a clearly applicable requirement.
- **unclear** — Evidence is insufficient or ambiguous; conclusion cannot be reached without more input.
- **not applicable** — The requirement does not apply to this product/scope; include a one-line justification.

## Severity Definitions

- **high** — Likely material harm to `titulares`, clear breach of a legal requirement, regulator-relevant exposure, or systemic safeguard failure.
- **medium** — Real but bounded risk; partial compliance with a legal requirement; weak controls around a clearly applicable obligation.
- **low** — Best-practice gap, minor transparency improvement, or low-likelihood / low-impact issue.
- **none** — Use only when `status` is `not applicable`, meaning no LGPD risk prioritization is needed for that requirement in the reviewed scope.

## Confidence Definitions

- **high** — Conclusion is supported by directly observed evidence (code, document text, UI behavior).
- **medium** — Conclusion is supported by partial evidence plus reasonable inference, clearly labeled.
- **low** — Conclusion relies primarily on inference or limited context; explicitly flag this.

## Classification Definitions

- **legal requirement** — Anchored in LGPD or another binding Brazilian federal law.
- **ANPD regulation** — Anchored in a binding ANPD Resolução do Conselho Diretor (CD/ANPD), such as Resoluções nº 2, 15, 18, 19, or 32. These carry regulatory force as secondary legislation.
- **ANPD guidance** — Anchored in non-binding ANPD instruments: Guias Orientativos, Notas Técnicas, FAQs, or educational materials. Informs but does not legally mandate.
- **best practice** — Not legally required, but recommended for risk reduction or `titular` experience.
- **context-dependent** — Applicability depends on facts the reviewer does not fully control (e.g., audience, scale, sector).

## Example Findings

### Example 1 — Cookies (ANPD guidance)

```yaml
area: Cookies and tracking technologies
status: partially compliant
severity: medium
confidence: high
classification: ANPD guidance
evidence observed: |
  Cookie banner shows "Aceitar" as the primary action; rejection requires
  opening a secondary modal with three nested toggles. Google Analytics
  loads before any user interaction.
missing evidence: |
  Cookie inventory; categorization of strictly necessary vs. consent-based
  cookies; whether analytics is configured in a way that avoids personal data
  processing.
why it matters: |
  ANPD Cookie Guidance disfavors imbalanced banners and pre-activation of
  non-essential trackers; this creates regulator exposure and weakens the
  validity of any consent obtained.
recommended remediation: |
  Provide a one-click "Rejeitar" at the first banner level; do not load
  non-essential trackers before consent; publish a cookie inventory aligned
  with banner categories.
official source reference: |
  ANPD — Guia Orientativo sobre Cookies e Proteção de Dados Pessoais
  (consult ANPD official site for the latest version).
```

### Example 2 — Sensitive personal data (legal requirement)

```yaml
area: Sensitive personal data
status: non-compliant
severity: high
confidence: medium
classification: legal requirement
evidence observed: |
  The signup form collects "religião" and "orientação sexual" as optional
  fields. The privacy notice lists "legítimo interesse" as the legal basis
  for "todos os dados coletados".
missing evidence: |
  Documented Art. 11 legal basis for these fields; demonstrated necessity;
  evidence of additional safeguards (access restriction, audit logging).
why it matters: |
  LGPD Art. 11 establishes specific legal bases for sensitive personal data.
  Legitimate interest is not among them. Processing these fields without an
  Art. 11 basis exposes the controller to regulator and titular claims.
recommended remediation: |
  Remove the fields unless a clearly necessary purpose exists; if necessary,
  rely on an Art. 11 basis (e.g., specific and highlighted consent) and add
  proportionate safeguards. Consider whether a RIPD is appropriate.
official source reference: |
  LGPD (Lei nº 13.709/2018), Art. 5, II; Art. 11.
```

### Example 3 — Account deletion (legal requirement)

```yaml
area: Account lifecycle and user controls
status: partially compliant
severity: medium
confidence: high
classification: legal requirement
evidence observed: |
  Users can request deletion via email. The privacy notice mentions
  deletion but does not specify what is retained or for how long after
  account closure.
missing evidence: |
  Retention schedule; explanation of legal retention exceptions; SLA for
  responding to deletion requests.
why it matters: |
  LGPD Art. 18 grants the titular the right to request deletion of personal
  data — including data that is unnecessary, excessive, or non-compliant
  (item IV), and data processed under consent (item VI) — subject to lawful
  retention exceptions. Lack of transparency on what is retained and why
  weakens the right's meaningful exercise.
recommended remediation: |
  Add a self-service deletion path; publish a clear post-deletion statement
  describing what is retained, why, and for how long; document an SLA.
official source reference: |
  LGPD (Lei nº 13.709/2018), Art. 18, items IV (deletion of unnecessary,
  excessive, or non-compliant data) and VI (deletion of data processed
  under the titular's consent); Art. 16 (lawful conservation after end of
  processing: legal or regulatory obligation, research, third-party
  transfer, or controller's exclusive anonymized use).
```

### Example 4 — Children and adolescents (not applicable)

```yaml
area: Children and adolescents
status: not applicable
severity: none
confidence: medium
classification: legal requirement
evidence observed: |
  Product is a B2B corporate SaaS sold exclusively to legal entities via
  enterprise contracts. The signup flow requires a CNPJ and a corporate
  email domain; no consumer-facing registration path exists.
missing evidence: |
  Contractual terms explicitly prohibiting use by individuals under 18;
  confirmation that no consumer-facing interface or public URL exists.
why it matters: |
  LGPD Art. 14 and its heightened protections apply when children or
  adolescents are likely users. The B2B-only model and structural access
  controls make this scenario outside the reviewed scope on the current
  evidence.
recommended remediation: |
  none
official source reference: |
  LGPD (Lei nº 13.709/2018), Art. 14 (not applicable here based on
  current evidence; reassess if a consumer-facing interface is added).
```

### Example 5 — International transfers (unclear)

```yaml
area: International transfers
status: unclear
severity: high
confidence: low
classification: legal requirement
evidence observed: |
  The application uses Stripe for payments and an unspecified third-party
  email delivery provider. Both vendors are US-based. The privacy notice
  mentions "parceiros terceiros" without identifying them or their locations.
missing evidence: |
  Full list of subprocessors and their countries of operation; whether
  the international transfer regulation's requirements (adequacy decision,
  standard contractual clauses, or specific guarantees) have been satisfied
  for each vendor; whether any ANPD-recognized transfer mechanism is in place.
why it matters: |
  LGPD Arts. 33–36 restrict transfers of personal data to countries or
  international bodies that do not provide an adequate level of protection
  unless a recognized transfer mechanism applies. Without visibility into
  the subprocessor chain, it is not possible to determine whether transfers
  are lawful. The ANPD International Transfer Regulation governs the
  applicable mechanisms; GDPR SCCs do not automatically satisfy LGPD
  requirements.
recommended remediation: |
  Map all vendors with access to personal data of Brazilian titulares;
  identify each vendor's country of operation; verify whether an ANPD-
  recognized transfer mechanism applies; disclose international transfers
  and their legal basis in the Aviso de Privacidade.
official source reference: |
  LGPD (Lei nº 13.709/2018), Arts. 33–36; ANPD — Resolução CD/ANPD nº 19
  (Regulamento de Transferência Internacional de Dados Pessoais, 2024 —
  verify current version on the ANPD official site).
```
