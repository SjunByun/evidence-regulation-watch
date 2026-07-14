Evidence Regulation Watch

How new kinds of data and technology become regulatory-grade evidence — AI, real-world evidence, and digital therapeutics, read through the lens of study design.


What this is

A living knowledge base tracking regulatory and standards documents across three converging domains:


AI in drug development & medical devices — validation, lifecycle management, governance
Real-world evidence (RWE) — from claims/EMR observational studies to regulatory acceptance (ICH M14 and beyond)
Digital therapeutics (DTx) & digital health technologies — evidence requirements for approval and reimbursement


These are usually tracked separately. I keep them together because they are the same question asked three ways: what does it take for a novel data source or technology to count as evidence a regulator will accept?

Every note separates two things that are usually blurred:


What the document says — a faithful, sourced summary.
What it means in practice — my interpretation as a study designer: how this changes protocol writing, data provenance requirements, validation burden, and what a sponsor or regulator will actually ask for.


The second part is the point. Summaries are abundant; translation into evidence-generation practice is not.

What this is not


Not legal advice, and not regulatory consulting.
Not a news feed. Documents are added when I have read them and have something to say about their practical consequences.
Not the views of my employer. All interpretation is my own.


Why I keep this

Evidence generation is being rebuilt around new inputs: NLP-extracted variables in observational studies, model-generated endpoints, DTx trials whose intervention is software, RWD flowing into regulatory submissions. Someone has to answer the question regulators will ask — "how do you know this is valid?" — in the language of epidemiology and study design, not model benchmarks or product marketing.

That translation layer — between novel data/technology and regulatory-grade evidence — is where I work. I am a pharmacoepidemiologist (PhD) with 11 years across hospital data analysis and CRO-based RWE, specializing in causal inference (target trial emulation, propensity score methods, SCCS, negative control outcomes), OMOP CDM, claims–EMR integration, and ICH M14 implementation. This repository is where I think through what the emerging regulatory landscape demands of that work.

Domain priorities

Depth over breadth, deliberately:

DomainDepthRationaleRWE regulationDeepMy core practice area; ICH M14 implementation is a daily concernAI in evidence generationDeepWhere my current research sits (AI-derived variables in causal studies)DTx / digital healthSelectiveCovered through the evidence-requirements lens, not product regulation in fullData standards (CDISC, OMOP, ICH M11)FoundationalThe plumbing all three domains depend on

How to navigate

Entry pointUse it when…index/coverage-map.mdYou want the master list of all documents and their statusindex/by-domain.mdYou care about one domain (AI / RWE / DTx / standards)index/by-theme.mdYou care about a theme (validation, transparency, provenance…) across domainsindex/timeline.mdYou need effective dates, comment deadlines, and what is coming nextanalyses/You want cross-cutting synthesis rather than single-document notes

Documents are filed by issuer under regulators/ and standards/, named YYYY-MM_short-slug.md by publication date.

Coverage map (snapshot)

Status: 🟢 published note · 🟡 in progress · ⚪ planned

DocumentIssuerDomainPublishedStatusGuiding Principles of Good AI Practice in Drug DevelopmentFDAAI2026-01🟡Considerations for the Use of AI to Support Regulatory Decision-Making for Drug and Biological ProductsFDAAI2025-01⚪AI-Enabled Device Software Functions: Lifecycle ManagementFDAAI · device2025-01⚪EU AI Act — high-risk classification of medical AIEUAI2024⚪ICH M14 (RWE for safety of medicines)ICHRWE—⚪FDA RWE guidance series (data standards, EHR/claims, registries)FDARWE2021–2024⚪EMA / DARWIN EU — RWE frameworkEMARWE—⚪MFDS RWE guidance (식약처 실사용증거 가이드라인)MFDSRWE—⚪FDA — Digital Health Technologies for Remote Data Acquisition in Clinical InvestigationsFDADTx · RWE2023-12⚪MFDS Digital Therapeutics guidance (디지털치료기기 허가·심사 가이드라인)MFDSDTx—⚪Germany DiGA fast-track — evidence requirementsBfArMDTx—⚪NIST AI Risk Management FrameworkNISTAI2023⚪ISO/IEC 42001 · 42005 · 22989ISOAI—⚪Korea AI Framework Act (AI 기본법)KoreaAI2024-12⚪CDISC / ICH M11 protocol standardization & RWD integrationCDISC·ICHStandards—⚪

The authoritative, always-current version of this table lives in index/coverage-map.md.

Note format

Every note follows the same structure (defined in TEMPLATE.md):


TL;DR → 1. Document profile → 2. What the document says → 3. What it means in practice (clearly marked as interpretation) → 4. Cross-references → 5. Watchlist & open questions → 6. Changelog



Sections 2 and 3 are strictly separated so readers can always tell source from opinion.

About the author

Seongjun Byun (변성준) — RWE Team Lead at a Korean CRO. PhD in pharmacoepidemiology (Sungkyunkwan University). 26 peer-reviewed publications in RWE/RWD. Speaker at DIA Korea, PHUSE, and Korean Statistical Society meetings on causal inference, ICH M14 implementation, and RWD study design.


LinkedIn: (link)
Selected talks & papers: (link)


Disclaimer

Personal project. Interpretations are my own professional opinions, provided for discussion, and do not constitute legal or regulatory advice, nor represent the position of any employer or client. Always consult the primary source documents, which are linked in each note.

License

Notes and analyses: CC BY 4.0. Quoted regulatory text remains the property of its issuers.
