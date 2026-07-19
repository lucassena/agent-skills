# Official Brazilian Sources — Map

This file is a **navigation aid** to identify the right Brazilian primary or official source for a given LGPD review topic. It is **not** itself legal authority. When citing in a finding, cite the underlying source (law article, ANPD regulation, ANPD guidance), not this file.

> Always confirm the latest version directly on the official source. ANPD publishes regulations, guidelines, FAQs, and educational materials that are updated periodically. If a source appears outdated, missing, or moved, say so in the finding rather than fabricating a citation.

## Source Type Hierarchy

1. **Binding law** — LGPD (Lei nº 13.709/2018) and other federal laws.
2. **Binding regulation** — ANPD Resoluções do Conselho Diretor (CD/ANPD).
3. **Official guidance** — ANPD Guias Orientativos, Notas Técnicas, Pareceres.
4. **Official FAQs / educational material** — useful interpretive context; not binding by itself.
5. **Other official Brazilian government materials** — only when they directly restate or host ANPD/LGPD content.

Anything outside this hierarchy (blog posts, vendor whitepapers, foreign DPAs, GDPR analyses) is **not** an official Brazilian source for the purposes of this skill.

## Source Map

For each entry below, capture in your finding citation, when possible:

- official source title
- official URL (verify it currently resolves)
- publication or last-modified date, when available
- legal/regulatory type
- relevant articles, sections, or topics
- what the source should and should not be used for
- whether the source is binding regulation, official guidance, FAQ, glossary, or educational material

---

### LGPD — Lei nº 13.709/2018

- **Type**: Federal law (binding).
- **Publisher**: Presidência da República / Casa Civil (Planalto).
- **Official URL**: https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709compilado.htm
- **Covers**: Definitions; principles; legal bases; sensitive personal data; data subject rights; processing by the public sector; international transfers; controlador/operador; encarregado; security and incidents; sanctions; ANPD.
- **When to consult**: Any mandatory legal conclusion. Always the first source for any LGPD claim.
- **Key articles often relevant**:
  - Art. 3 — territorial applicability
  - Art. 5 — definitions (personal data, sensitive personal data, titular, controlador, operador, encarregado)
  - Art. 6 — principles
  - Art. 7 — legal bases for personal data
  - Art. 8 — consent requirements
  - Art. 9 — transparency / information to the data subject
  - Art. 11 — sensitive personal data and its specific legal bases
  - Art. 14 — children and adolescents
  - Art. 18 — data subject rights (`titular`)
  - Art. 20 — automated decisions and review
  - Arts. 33–36 — international transfers
  - Art. 37 — records of processing operations by controlador and operador
  - Art. 38 — relatório de impacto à proteção de dados pessoais (RIPD)
  - Arts. 41–42 — encarregado; civil liability
  - Arts. 46–49 — security, good practices, incidents
- **Freshness caveat**: Has received amendments; always check the consolidated text.

---

### ANPD — Official site and regulations index

- **Type**: Regulator (authority).
- **Official URL**: https://www.gov.br/anpd/pt-br
- **Regulations index URL**: https://www.gov.br/anpd/pt-br/acesso-a-informacao/institucional/atos-normativos/regulamentacoes_anpd
- **Covers**: All ANPD-issued regulations, guidelines, technical notes, FAQs, news, and consultations.
- **When to consult**: To find binding ANPD regulations and official guidance.
- **Use for**: Locating the most recent version of any ANPD instrument cited below.
- **Do not use for**: Unofficial interpretations or third-party summaries hosted elsewhere.

---

### ANPD Regulation on Security Incidents (Comunicação de Incidente de Segurança)

- **Type**: ANPD Resolução (binding regulation).
- **Official title**: Resolução CD/ANPD nº 15, de 24 de abril de 2024 — Regulamento de Comunicação de Incidente de Segurança.
- **Official URL**: https://www.in.gov.br/en/web/dou/-/resolucao-cd/anpd-n-15-de-24-de-abril-de-2024-556243024
- **Fallback / repository URL**: https://dspace.mj.gov.br/handle/1/12879
- **ANPD index URL**: https://www.gov.br/anpd/pt-br/acesso-a-informacao/institucional/atos-normativos/regulamentacoes_anpd
- **Covers**: Criteria, deadlines, form, content, and process for communicating personal data security incidents to ANPD and to data subjects; risk assessment for relevant harm.
- **When to consult**: Reviewing incident response, breach notification timelines and contents, controller/operator responsibilities in incidents.
- **Do not use for**: Generic cybersecurity controls — those are governed by Art. 46 LGPD and good practices, not by the incident regulation alone.

---

### ANPD Regulation on the Encarregado (DPO)

- **Type**: ANPD Resolução (binding regulation).
- **Official title**: Resolução CD/ANPD nº 18, de 16 de julho de 2024 — Regulamento sobre a atuação do encarregado pelo tratamento de dados pessoais.
- **Official URL**: https://www.in.gov.br/en/web/dou/-/resolucao-cd/anpd-n-18-de-16-de-julho-de-2024-572632074
- **ANPD index URL**: https://www.gov.br/anpd/pt-br/acesso-a-informacao/institucional/atos-normativos/regulamentacoes_anpd
- **Covers**: Definition, role, designation, publication, attributes, and exemptions for the `encarregado`. Interaction with small processing agents.
- **When to consult**: Assessing whether an `encarregado` must be appointed, how their contact must be disclosed, and the scope of their duties.

---

### ANPD Regulation on International Data Transfers

- **Type**: ANPD Resolução (binding regulation).
- **Official title**: Resolução CD/ANPD nº 19, de 23 de agosto de 2024 — Regulamento de Transferência Internacional de Dados e cláusulas-padrão contratuais.
- **Official URL**: https://www.gov.br/anpd/pt-br/acesso-a-informacao/institucional/atos-normativos/regulamentacoes_anpd/resolucao-cd-anpd-no-19-de-23-de-agosto-de-2024
- **Fallback / index URL**: https://www.gov.br/anpd/pt-br/acesso-a-informacao/institucional/atos-normativos/regulamentacoes_anpd
- **Covers**: Legal mechanisms for international transfers, adequacy, standard contractual clauses, specific guarantees, and exceptions under LGPD Arts. 33–36.
- **When to consult**: Reviewing cloud providers, analytics, support tools, subprocessors, or any operational access from outside Brazil.
- **Transition note**: The 12-month grace period expired **August 23, 2025** — SCCs (cláusulas-padrão contratuais, Art. 33, II, b) are now required for transfers **that rely on this specific mechanism**. Organizations using Art. 33, II, b as their transfer basis and that have not yet implemented Resolução nº 19/2024 SCCs are operating out of compliance. This note does **not** apply to transfers covered by other mechanisms: adequacy decisions (Art. 33, I — e.g., transfers to the EU under Resolução nº 32/2026), other specific guarantees, legal exceptions, or any other applicable basis under Arts. 33–36.
- **Do not assume**: That GDPR adequacy decisions or SCCs automatically satisfy LGPD.

---

### ANPD Adequacy Decision — European Union (Resolução CD/ANPD nº 32/2026)

- **Type**: ANPD Resolução CD (binding regulation).
- **Official title**: Resolução nº 32, de 26 de janeiro de 2026 — Dispõe sobre o reconhecimento da União Europeia como organismo internacional com grau de proteção de dados pessoais adequado.
- **Official URL**: https://www.in.gov.br/web/dou/-/resolucao-n-32-de-26-de-janeiro-de-2026-683334547
- **Published**: Diário Oficial da União, 27/01/2026, Edição 18, Seção 1, Página 49.
- **Legal basis**: LGPD Art. 33, I (transfer to countries with adequate protection).
- **Covers**: Recognizes the EU member states, Iceland, Liechtenstein, and Norway (EEA), and EU institutions as providing adequate data protection for purposes of international transfer. Enables transfers under LGPD Art. 33, I without requiring SCCs or specific guarantees.
- **Scope exclusion**: Does **not** apply to transfers for public security, national defense, state security, or criminal investigation/repression purposes (Art. 2).
- **Monitoring**: ANPD must reassess the adequacy decision within 4 years of publication.
- **When to consult**: Any international transfer finding involving EU/EEA-based vendors, cloud providers, or subprocessors. Transferring to an EU-based entity may now rely on adequacy rather than SCCs, but other LGPD obligations (transparency, purpose limitation, security) still apply.
- **Do not assume**: That EU adequacy under LGPD covers transfers to non-EEA countries, or that it removes all other LGPD obligations on the Brazilian controller.

---

### ANPD Cookie Guidance (Guia Orientativo — Cookies e Proteção de Dados Pessoais)

- **Type**: ANPD official guidance.
- **Official URL**: https://www.gov.br/anpd/pt-br/documentos-e-publicacoes/guia-orientativo-cookies-e-protecao-de-dados-pessoais.pdf
- **Covers**: Classification of cookies, legal bases, consent quality, banner design, dark patterns, transparency.
- **When to consult**: Any cookie banner or tracker review.
- **Do not infer**: That every cookie requires consent. ANPD distinguishes strictly necessary cookies from those that may require consent or another legal basis.

---

### ANPD Questions and Answers on RIPD (Relatório de Impacto à Proteção de Dados Pessoais)

- **Type**: ANPD official questions and answers; non-binding interpretive material.
- **Official URL**: https://www.gov.br/anpd/pt-br/canais_atendimento/agente-de-tratamento/relatorio-de-impacto-a-protecao-de-dados-pessoais-ripd
- **Covers**: When a RIPD is appropriate, what it should contain, risk-based assessment, and the current reference parameter for identifying high-risk processing while no specific RIPD regulation establishes different criteria.
- **When to consult**: Assessing whether processing may present high risk, whether a RIPD should be considered, or how to structure and document a RIPD.
- **Do not use for**: Claiming that a RIPD is automatically mandatory whenever a single risk factor exists.

---

### ANPD Guidance on Legitimate Interest

- **Type**: ANPD official guidance.
- **Official URL**: https://www.gov.br/anpd/pt-br/centrais-de-conteudo/materiais-educativos-e-publicacoes/guia_legitimo_interesse.pdf/@@display-file/file
- **Covers**: Necessity and proportionality test, transparency, balancing, safeguards, reasonable expectations of the data subject.
- **When to consult**: Whenever a finding relies on legitimate interest as a legal basis.
- **Do not assume**: That legitimate interest covers sensitive personal data.

---

### ANPD Guidance for Small Processing Agents (Agentes de Tratamento de Pequeno Porte)

- **Type**: ANPD Resolução / official guidance.
- **Official title**: Resolução CD/ANPD nº 2, de 27 de janeiro de 2022 — Regulamento de aplicação da LGPD para agentes de tratamento de pequeno porte.
- **Official URL**: https://www.gov.br/anpd/pt-br/acesso-a-informacao/institucional/atos-normativos/regulamentacoes_anpd/resolucao-cd-anpd-no-2-de-27-de-janeiro-de-2022
- **ANPD index URL**: https://www.gov.br/anpd/pt-br/acesso-a-informacao/institucional/atos-normativos/regulamentacoes_anpd
- **Covers**: Definition of small processing agents, differentiated obligations, procedural flexibilizations, and which core duties remain.
- **When to consult**: When the organization may qualify as a small processing agent.
- **Do not assume**: That small-agent status removes core LGPD principles, basic transparency duties, security expectations, or data subject rights.

---

### ANPD Simplified Records of Processing Operations Model for Small Processing Agents

- **Type**: ANPD official model / educational-operational material.
- **Official URL**: https://www.gov.br/anpd/pt-br/assuntos/noticias/anpd-divulga-modelo-de-registro-simplificado-de-operacoes-com-dados-pessoais-para-agentes-de-tratamento-de-pequeno-porte-atpp
- **Covers**: Simplified records of personal data processing operations for `agentes de tratamento de pequeno porte` (ATPP).
- **When to consult**: Reviewing whether a small processing agent has evidence of mapped processing activities, such as data categories, purposes, legal bases, sharing, retention, security measures, and responsible areas.
- **Use with**:
  - LGPD Art. 37, for the general duty to maintain records of processing operations.
  - ANPD rules on small processing agents, especially when simplified compliance may apply.
- **Do not assume**:
  - That the simplified model applies to every organization.
  - That using the simplified model alone proves full LGPD compliance.
  - That absence of this model in reviewed materials automatically proves non-compliance, unless the review scope includes governance documentation.
- **Freshness caveat**: Always verify whether ANPD has published a newer model, updated spreadsheet, PDF, FAQ, or regulation.

---

### ANPD Guidance / Official Interpretation on Children and Adolescents

- **Type**: ANPD official guidance, technical notes, and LGPD Art. 14.
- **Official title**: Enunciado CD/ANPD nº 1, de 22 de maio de 2023.
- **Official URL**: https://www.in.gov.br/en/web/dou/-/enunciado-cd/anpd-n-1-de-22-de-maio-de-2023-485306934
- **ANPD PDF URL**: https://www.gov.br/anpd/pt-br/assuntos/noticias/anpd-divulga-enunciado-sobre-o-tratamento-de-dados-pessoais-de-criancas-e-adolescentes/Enunciado1ANPD.pdf
- **ANPD index URL**: https://www.gov.br/anpd/pt-br/acesso-a-informacao/institucional/atos-normativos/regulamentacoes_anpd
- **Covers**: Best interest standard, parental consent scenarios, transparency adapted to age, processing without consent in the child's best interest under specific conditions.
- **When to consult**: Any product directed to or likely used by children/adolescents.
- **Adjacent issue**: ECA Digital may impose additional obligations on digital platforms used by children/adolescents — flag separately, do not merge into LGPD findings unless the official source clearly supports the linkage.

---

### ANPD FAQs and Glossary

- **Type**: Educational / interpretive (not binding by itself, but official).
- **FAQ URL**: https://www.gov.br/anpd/pt-br/acesso-a-informacao/perguntas-frequentes/perguntas-frequentes
- **Glossary URL**: https://www.gov.br/anpd/pt-br/documentos-e-publicacoes/glossario-anpd
- **When to consult**: To clarify ANPD's official position on a term or process where a binding instrument is silent.
- **Do not use as**: The sole basis for a legal requirement.

---

## Non-Sources (Do Not Cite as Authority)

- Vendor blog posts, law-firm articles, consulting whitepapers.
- Foreign data protection authority guidance (e.g., EDPB, ICO, CNIL) — informative only.
- GDPR text — informative only; **not binding in Brazil**.
- Generic "LGPD checklists" of unknown provenance.

These materials may be informative context, but findings that state a legal requirement must cite a Brazilian official source.
