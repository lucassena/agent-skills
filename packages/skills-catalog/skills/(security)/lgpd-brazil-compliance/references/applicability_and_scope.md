# Applicability and Scope

Run this before producing any findings. If applicability is unclear, ask the user. If the user cannot answer, proceed with the most defensible assumption and label it clearly.

## 1. Does the Product Process Personal Data?

LGPD applies to the processing of personal data. If the product genuinely processes no personal data (purely anonymous, no identifiers, no IP-based tracking, no auth, no metadata that could identify a natural person), say so and stop. This is rare in practice.

When in doubt, treat the data as personal data and proceed.

## 2. Territorial Applicability — LGPD Article 3

LGPD applies whenever **any one** of the following is true (these are **alternative triggers**, not cumulative requirements):

1. The processing operation is **carried out in Brazil**.
2. The processing activity has the purpose of **offering or providing goods or services to**, or processing data of, **individuals located in Brazil**.
3. The **personal data being processed was collected in Brazil** (data subjects located in Brazil at the time of collection).

Notes:

- Hosting location is **not** the only factor. Even infrastructure abroad can be subject to LGPD if any trigger above applies.
- A Brazilian-Portuguese UI, BRL pricing, marketing to Brazilian audiences, `.br` domain, or Brazilian payment methods are strong indicators of trigger (2).
- Active targeting of Brazil is strong evidence for trigger (2), but it is not the only path under **Art. 3, II**. If the reviewed processing includes personal data of individuals located in Brazil, do not treat the absence of Brazil-specific marketing, pricing, or localization as automatically removing LGPD applicability. State the observed facts and explain which Art. 3 trigger is being relied on.

Cite **LGPD Art. 3** in any finding that depends on territorial applicability.

### 2b. Exclusions — Check Before Proceeding (LGPD Art. 4)

Even when Art. 3 triggers apply, LGPD **does not apply** to processing that falls exclusively within one of the following. Verify before producing any findings.

- **Art. 4, I** — Processing by a natural person exclusively for private, non-economic purposes (personal photo album, family contacts with no professional use).
- **Art. 4, II, a** — Processing exclusively for journalistic or artistic purposes.
- **Art. 4, II, b** — Processing for academic purposes. This is a partial / nuanced exclusion: LGPD Art. 4 applies, but Arts. 7 and 11 still apply. Do not stop the review entirely when legal basis or sensitive personal data issues are in scope.
- **Art. 4, III** — Processing for public safety, national defense, State security, or investigation of criminal offenses. Note: LGPD Art. 4 §§ 1–2 impose residual obligations even in this case; flag the nuance.
- **Art. 4, IV** — Applies when **all four** of the following conditions are met simultaneously: (1) processing **originates from outside Brazilian territory**; (2) not subject to communication or shared use with Brazilian processing agents; (3) not subject to international transfer to a country other than the country of origin; (4) the country of origin provides a level of personal data protection adequate to that established by LGPD. If any condition is not met, the exclusion does not apply.

If an exclusion applies, cite **LGPD Art. 4** + inciso, state clearly it is out of scope, and do **not** proceed with the 15-area review. If the exclusion is partial or nuanced, such as academic processing under **Art. 4, II, b**, narrow the scope, cite the applicable residual articles, and continue only for the relevant areas.

## 3. Role Classification

Classify the organization's role for each processing activity:

- **Controlador** — decides on the purposes and essential means of processing.
- **Operador** — processes personal data on behalf of the controlador, under instructions.
- **Joint controllers** — two or more entities jointly determine purposes and essential means. LGPD does not use the term explicitly the same way as GDPR; describe the factual cooperation and the resulting shared duties.
- **Unclear** — cannot be determined from available evidence; flag and request more input.

A single product can act as **controlador** for some activities and **operador** for others. Map per activity when relevant. Cite **LGPD Art. 5** (definitions) and Arts. 37–42 for related duties.

## 4. Evidence-Type Scoping

State explicitly which kinds of evidence were available, and adjust confidence accordingly.

| Evidence type                                                      | What it supports                                                                                                  | Common limitations                                                                              |
| ------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| **Code-only** review                                               | Behaviors observable in code: forms, fields collected, cookies set, API calls, retention jobs, security controls. | Cannot verify operational practice, vendor contracts, or what users actually see in production. |
| **Documents-only** review (privacy policy, DPA, internal policies) | Claims about transparency, legal bases, retention, rights, governance.                                            | Cannot verify that the product actually behaves as documented.                                  |
| **Screenshots / UI walkthroughs**                                  | User-facing experience, banner behavior, rights flows.                                                            | Snapshot only; cannot verify backend processing or retention.                                   |
| **Production behavior** (live testing)                             | End-to-end behavior across UI, network, and storage.                                                              | Limited visibility into backend storage and vendor flows.                                       |
| **Mixed**                                                          | Best coverage; ideal for high-confidence findings.                                                                | Still bounded by what was shared.                                                               |

For any review:

- State the evidence types available.
- Where coverage is partial, mark findings as `unclear` with `medium` or `low` confidence and list the missing evidence.

## 5. Out-of-Scope Items

Adjacent topics may surface during review. They are **adjacent**, not LGPD findings, unless an official Brazilian source clearly links them. Flag them separately:

- **ECA Digital** — digital platforms likely used by children/adolescents.
- **Consumer law (CDC)** — refunds, advertising, dark patterns from a consumer perspective.
- **Health regulation** — additional duties for health data flows.
- **Financial regulation** — Bacen / CVM rules and bank secrecy.
- **Marco Civil da Internet** — application-provider duties (log retention, content takedown, neutrality).
- **Employment law** — workplace monitoring and employee data.

Do not merge these into LGPD findings. Mention them in `Open questions / evidence needed` or as `adjacent` notes.

## 6. When to Stop and Ask

Pause and ask the user when any of the following is missing and material:

- Whether the product targets users in Brazil.
- Whether sensitive personal data is processed.
- Whether children/adolescents are likely users.
- Whether there are international vendors or subprocessors.
- Whether there are solely automated decisions with legal or significant effects.
- The role of the organization (`controlador` / `operador`) for the activities under review.

If the user prefers to proceed without answers, continue with explicit assumptions labeled in `Scope and assumptions`.
