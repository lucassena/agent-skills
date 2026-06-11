# Review Areas — Checks, Evidence, False Assumptions

For each area: what to check, what counts as **strong evidence**, **weak evidence**, **missing evidence**, and common **false assumptions to avoid**.

Always cite the underlying official Brazilian source (LGPD article or ANPD instrument) in the finding, not this file.

## Table of Contents

1. Transparency and Notices
2. Legal Basis and Purpose Limitation
3. Sensitive Personal Data
4. Cookies and Tracking Technologies
5. Data Subject Rights
6. Account Lifecycle and User Controls
7. Data Retention and Disposal
8. Security and Privacy Safeguards
9. Incident Response and Breach Communication
10. Governance and Accountability
11. Records of Processing Activities
12. RIPD and High-Risk Processing
13. Children and Adolescents
14. International Transfers
15. Automated Decisions and Profiling

---

## 1. Transparency and Notices

**What to check**

- Existence and accessibility of a `Privacy Notice` / `Aviso de Privacidade`.
- Whether the notice explains: categories of personal data; purposes; legal bases when appropriate; retention periods or criteria; sharing with third parties / `operadores`; international transfers; data subject rights; privacy contact channels; controller identity; `encarregado` when applicable.
- Plain language; layered presentation acceptable.

**Strong evidence**: A published, dated `Aviso de Privacidade` that addresses each item above with product-specific detail.
**Weak evidence**: A generic template, undated, or only linked from a footer in a hard-to-find location.
**Missing evidence**: No notice; or notice silent on key items (purposes, retention, sharing, rights).

**False assumptions to avoid**

- That `Termos de Uso` automatically satisfy LGPD transparency duties — they do not, by themselves.
- That linking to a generic group/parent-company policy is sufficient when the product has product-specific processing.

---

## 2. Legal Basis and Purpose Limitation

**What to check**

- Each relevant processing activity has a plausible legal basis under LGPD (Art. 7 for personal data; Art. 11 for sensitive personal data).
- Purposes are specific, explicit, and legitimate.
- Collection is necessary and proportionate.
- Avoidance of generic or overly broad purposes ("for any business purpose").

**Legitimate interest test** — when relied upon, evidence of:

- a specific legitimate interest;
- necessity and proportionality;
- transparency to the data subject;
- compatibility with reasonable expectations;
- safeguards and rights protections;
- balancing assessment or equivalent reasoning.

**Strong evidence**: Documented mapping of activities to legal bases; specific purposes; published legitimate-interest reasoning when used.
**Weak evidence**: A single sentence asserting "we process on the basis of legitimate interest" without further reasoning.
**Missing evidence**: No legal basis stated; or consent assumed without a real consent mechanism.

**False assumptions to avoid**

- That "consent" is the default basis for everything.
- That legitimate interest is a catch-all.
- That contract execution justifies any related processing.

---

## 3. Sensitive Personal Data (LGPD Art. 11)

**What to check**

- Whether the application processes sensitive personal data as defined by LGPD Art. 5, II (e.g., racial or ethnic origin, religious conviction, political opinion, union/religious/philosophical/political organization membership, health or sexual life data, genetic or biometric data linked to a natural person).
- Whether the analysis clearly distinguishes ordinary personal data from sensitive personal data.
- The specific legal bases under **LGPD Art. 11** are applied (not Art. 7).
- Stronger safeguards: restricted access, minimization, encryption where appropriate, audit logging, stricter retention, clear purpose limitation.
- Higher likelihood that a **RIPD** should be considered.

**Strong evidence**: Explicit identification of sensitive data flows; Art. 11 basis stated; technical safeguards proportionate to sensitivity; RIPD considered.
**Weak evidence**: Sensitive data processed but treated as ordinary personal data in policies and code.
**Missing evidence**: No assessment of whether sensitive data is processed; no distinction in safeguards.

**False assumptions to avoid**

- **Do not** assume legitimate interest is a valid legal basis for sensitive personal data unless an official Brazilian source clearly supports that conclusion. LGPD Art. 11 has its own list of bases.
- That biometric or health-adjacent data is "just personal data."
- That pseudonymized sensitive data automatically falls outside Art. 11.

---

## 4. Cookies and Tracking Technologies

**What to check** (apply ANPD Cookie Guidance)

- Whether cookies and similar trackers are present.
- Whether they are classified by purpose and necessity.
- Whether non-necessary cookies have meaningful user control.
- Whether the banner allows **rejection** of non-necessary cookies as easily as acceptance.
- Whether consent-based cookies are **disabled by default**.
- Absence of dark patterns, imbalance, nudging, pre-selected consent, or unnecessary friction to reject.
- Alignment between the banner behavior and the cookie policy.

**Strong evidence**: Granular cookie controls; reject-all available at first interaction; cookie inventory aligned with banner; no pre-checked non-essential boxes.
**Weak evidence**: "Accept" button only; reject requires multi-step navigation; banner lists categories but does not enforce them.
**Missing evidence**: No banner; or banner not aligned with actual trackers loaded.

**False assumptions to avoid**

- That every cookie requires consent. Strictly necessary cookies do not.
- That a "cookie wall" forcing acceptance is acceptable.
- That GDPR cookie practices automatically satisfy ANPD guidance.

---

## 5. Data Subject Rights (`Titular`)

**What to check** (LGPD Art. 18)

- Practical channel to request rights under LGPD Art. 18 and related paragraphs: confirmation of processing (I); access (II); correction (III); anonymization, blocking, or deletion of unnecessary, excessive, or non-compliant data (IV); portability (V); deletion of consent-based data (VI); information about sharing with third parties (VII); information about the option not to consent and the consequences of refusal (VIII); revocation of consent (IX); petition to ANPD (§1º); opposition to consent-exempt processing when there is LGPD non-compliance (§2º).
- Visibility and practicality of the workflow; no unreasonable friction.

**Strong evidence**: Self-service controls plus a clearly identified contact channel; documented intake and response process.
**Weak evidence**: Only an email address with no SLA or process; rights enumerated only in the policy.
**Missing evidence**: No channel at all.

**False assumptions to avoid**

- That deletion must always be absolute. Lawful retention exceptions exist (e.g., legal obligations, regulatory record-keeping).
- That portability applies to all data.

---

## 6. Account Lifecycle and User Controls

**What to check**

- User can export data or request access in a usable format when applicable.
- User can request account deletion or data deletion.
- The app explains: what is deleted immediately; what is retained; why; for how long.
- Consent withdrawal is as easy as consent grant.

**Strong evidence**: In-product account deletion with a clear post-deletion statement; export available where appropriate.
**Weak evidence**: Deletion only via email; no statement on what is retained.
**Missing evidence**: No deletion path; or consent can be granted in one click but withdrawal requires support tickets.

---

## 7. Data Retention and Disposal

**What to check**

- Retention periods or retention criteria exist.
- Data kept only as long as necessary or legally required.
- Evidence of deletion, anonymization, disposal, archival, or lifecycle rules.

**Strong evidence**: Retention schedule referenced in the policy; technical lifecycle jobs visible in code or operations.
**Weak evidence**: "We keep data for as long as necessary" with no further detail.
**Missing evidence**: No retention statement and no operational lifecycle.

---

## 8. Security and Privacy Safeguards

**What to check** (LGPD Art. 46)

- Reasonable administrative and technical safeguards.
- Examples: access control, least privilege, secure password handling, secret handling, encryption in transit, audit logging, backup controls, vendor access controls.

**Strong evidence**: Documented controls plus code/configuration that implements them; segregation of duties.
**Weak evidence**: Policy claims controls without implementation evidence.
**Missing evidence**: Plaintext credentials, broken auth, missing TLS, no access control.

**False assumptions to avoid**

- That a specific technology stack is required.
- That ISO/SOC certifications by themselves satisfy LGPD security duties.

---

## 9. Incident Response and Breach Communication

**What to check** (ANPD incident regulation; LGPD Arts. 46–48)

- Internal path for personal data incidents.
- Ability to assess risk or relevant harm and communicate incidents to ANPD and `titulares` when required.
- Clarity of `controlador` vs `operador` responsibilities in the flow.

**Strong evidence**: Documented incident plan referencing ANPD criteria; defined roles; templated communications.
**Weak evidence**: Generic IT incident plan with no LGPD-specific path.
**Missing evidence**: No plan; or the plan ignores `titular` communication.

**False assumptions to avoid**

- That generic cybersecurity advice satisfies the ANPD incident regulation.
- That every incident must be reported. Reportability depends on risk / relevant harm criteria defined by ANPD.

**Key operational criteria from Resolução CD/ANPD nº 15/2024 (verify against current text):**

- **Reportability threshold — CUMULATIVE**: Both criteria must be met before notification is required:
  1. The incident is reasonably likely to cause **risk or relevant harm** (risco ou dano relevante) to titulares — e.g., impeding the exercise of rights, restricting access to a service, or causing material/moral harm such as discrimination, identity theft, financial fraud, damage to image/reputation, or violation of the right to privacy; **AND**
  2. The incident involves at least one of the following data categories: **sensitive personal data**; data of **children, adolescents, or elderly persons**; **financial data**; **authentication credentials**; data protected by **legal, judicial, or professional secrecy**; or data processed **at large scale**.
- **Phase 1 — Preliminary notification to ANPD**: Within **3 business days** from the moment the controlador became aware **that the incident involved personal data**, if the preliminary assessment indicates the threshold above is met.
- **Phase 2 — Complementary notification to ANPD**: Within **20 business days from the date of the Phase 1 communication**, if complete information was not available at the time of the preliminary notification; must include justification for the delay.
- **Titular communication**: Required when the reportability threshold is met; must use plain language via communication channels normally used by the controller. If individual notification is not possible, wide public disclosure (website, app, social media, support channels) is required for a minimum of **3 months**.
- **Record-keeping**: Even when the threshold is **not** met and notification is not required, the controlador must retain incident records for **at least 5 years**.
- **Controlador responsibility**: The controlador must notify. Operadores must promptly inform the controlador so it can meet its deadlines.
- **Small processing agents** (agentes de pequeno porte per Resolução CD/ANPD nº 2/2022): all deadlines are counted **in double** — 6 business days for Phase 1, 40 for Phase 2.

> ⚠️ Always verify current Resolução nº 15 text on the ANPD site before finalizing a finding on incident response.

---

## 10. Governance and Accountability

**What to check**

- Clear `controlador` and `operador` roles.
- `Encarregado` designation and published contact channel: **mandatory for controllers in general** (Resolução CD/ANPD nº 18/2024, Art. 3), subject to dispensation for **small processing agents** that qualify under ANPD rules — even when dispensed, a communication channel for `titulares` and ANPD must be maintained; **optional for operators** (Resolução nº 18/2024, Art. 6; considered governance best practice when appointed). When appointed, the encarregado's designation and contact must be publicly disclosed (Resolução nº 18/2024, Arts. 8–9); the role must be performed with adequate authority and resources.
- Internal accountability, governance, policies, or review procedures.
- Contracts or operational expectations with `operadores` addressing personal data, security, and incident handling.
- Whether the organization may qualify as a **small processing agent** under ANPD rules — and if so, which differentiated obligations or procedural flexibilizations apply.

**False assumptions to avoid**

- That small-agent status removes core LGPD principles, transparency duties, security expectations, or data subject rights.
- That an outsourced DPO contact email alone discharges the encarregado duties.

---

## 11. Records of processing activities

**What to check** (LGPD Art. 37)

- Whether there is evidence that the organization maps or records personal data processing activities.
- Whether the records identify, when available:
  - categories of personal data;
  - purposes of processing;
  - legal bases;
  - data subjects involved;
  - sharing with third parties, processors, or operators;
  - international transfers;
  - retention periods or retention criteria;
  - security and privacy safeguards;
  - responsible business areas or systems.
- Whether the records are consistent with the privacy notice, cookie policy, product behavior, and actual data flows.
- For small processing agents, whether simplified records or ANPD-provided models may be relevant.

**Strong evidence**: A data mapping or RoPA artifact (spreadsheet, register, ANPD-model document) that covers the categories above; updated to reflect current product behavior.
**Weak evidence**: An informal list or a single paragraph in internal policies mentioning categories and purposes, without detail on sharing, transfers, or retention.
**Missing evidence**: No records artifact in scope; governance documentation was not reviewed (in this case, classify as `unclear`, not non-compliant).

**False assumptions to avoid**

- That absence of records in the reviewed materials proves non-compliance; the records may exist outside the review scope.
- That simplified records models (ANPD small-agent materials) apply to every organization.

---

## 12. RIPD and High-Risk Processing

**What to check** (LGPD Art. 38; ANPD RIPD guidance)

- Whether processing is likely high risk: sensitive data; large-scale processing; children/adolescents; significant automated decisions; public-area monitoring; other high-risk contexts.
- Whether a RIPD has been considered, produced, or is recommended.

**False assumptions to avoid**

- That RIPD is mandatory for every product.
- That RIPD is purely documentation — it must reflect real risk analysis.

---

## 13. Children and Adolescents

**What to check** (LGPD Art. 14)

- Whether the product is directed to or likely used by children/adolescents.
- Best interest standard considered.
- Notices, safeguards, and age-related flows appropriate to the audience.
- Age-assurance or age-verification relevance.

**Adjacent issue**: If the product is a digital platform directed to or with probable access by children/adolescents, flag **ECA Digital** obligations (Lei nº 15.211/2025, in force since **March 17, 2026**) as adjacent — to be reviewed separately under ECA Digital rules. Do **not** merge ECA Digital duties into LGPD findings unless the official source clearly supports the linkage.

---

## 14. International Transfers

**What to check** (LGPD Arts. 33–36; ANPD Resolução nº 19/2024; ANPD Resolução nº 32/2026)

- Whether personal data is transferred to, or accessed from, outside Brazil — directly or via vendors, cloud providers, analytics, support tools, subprocessors, or operational access.
- For each identified transfer destination, whether one of the following mechanisms applies:
  - **Adequacy** (LGPD Art. 33, I): the destination country or international body has been recognized by ANPD as providing adequate protection. **EU/EEA countries (including Iceland, Liechtenstein, Norway) and EU institutions are recognized as adequate under Resolução CD/ANPD nº 32/2026** — transfers to these destinations may rely on adequacy without additional mechanisms. Verify scope exclusions (public security, national defense, state security, criminal investigation).
  - **Adequate guarantees** (LGPD Art. 33, II): instruments regulated by ANPD (Resolução nº 19/2024) — including specific contractual clauses for a particular transfer (Art. 33, II, a), standard contractual clauses / cláusulas-padrão (Art. 33, II, b), binding corporate rules / normas corporativas globais (Art. 33, II, c), and seals, certifications, or codes of conduct (Art. 33, II, d). **The 12-month grace period for transitioning to Resolução nº 19/2024 SCCs ended August 23, 2025 — SCCs are now mandatory for all ongoing transfers relying on Art. 33, II, b.**
  - **Narrow exceptions** (LGPD Art. 33, III–IX): data subject consent for the transfer (VIII); legal obligation, contract execution, or regular exercise of rights (IX, via Art. 7, II, V, and VI); ANPD authorization of a specific transfer (V); protection of life or physical integrity (IV); and others. These are narrow, context-specific grounds — not default transfer mechanisms.
- Whether international transfers are disclosed in the `Aviso de Privacidade`.
- Whether DPAs or contractual instruments with `operadores` abroad address the applicable transfer mechanism.

**Strong evidence**: Documented subprocessor list with countries; identified transfer mechanism for each; disclosure in the privacy notice; DPAs referencing applicable ANPD instruments.
**Weak evidence**: Privacy notice mentions "international transfers" or "third-party partners" without identifying destinations or mechanisms; no subprocessor list.
**Missing evidence**: No subprocessor visibility; no disclosure; no transfer mechanism documented.

**False assumptions to avoid**

- That GDPR SCCs automatically satisfy LGPD international transfer rules — ANPD SCCs (Resolução nº 19/2024) are the Brazilian instrument.
- That hosting in Brazil eliminates international transfer risk if support staff or subprocessors are abroad.
- That all EU/EEA transfers require SCCs or specific guarantees — Resolução CD/ANPD nº 32/2026 grants adequacy for most transfers to EU/EEA, but verify scope exclusions.
- That the EU adequacy decision extends to non-EEA destinations or removes other LGPD obligations on the Brazilian controller.

---

## 15. Automated Decisions and Profiling

**What to check** (LGPD Art. 20)

- Whether the application makes decisions **solely** through automated processing that affect user interests.
- Whether the user can request review or explanation when relevant.
- Whether profiling, scoring, fraud analysis, recommendation, segmentation, or credit-related flows are materially relevant.

**False assumptions to avoid**

- That any algorithmic feature triggers Art. 20. The provision targets solely automated decisions that affect the user's interests.
- That a human "rubber stamp" automatically removes the activity from the scope of Art. 20.
