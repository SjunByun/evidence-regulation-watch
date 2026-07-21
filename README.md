# Evidence Regulation Watch

**One question: under what conditions does data produced by a new technology become evidence a regulator will accept?**

---

## What this is

Notes on regulatory documents that bear on how evidence gets made — AI in drug development, real-world data, digital health. They are usually tracked as separate fields. I track them together because they are the same question asked in different settings.

Each note has two layers, kept separate:

- **What the document says** — a summary, faithful to the source.
- **What it means in practice** — my reading as someone who designs studies: what changes in a protocol, what has to be validated, what a regulator will actually ask for.

The second layer is the point. Summaries are easy to find. Translation into study design is not.

Not legal or regulatory advice. Not the views of my employer.

## Why I keep it

Evidence is increasingly built from things that did not used to count as measurements: variables extracted by NLP from clinical notes, endpoints produced by models, curated real-world data standing in for trial data. Each one raises the same question a regulator will ask — *how do you know this is valid?* — and answering it takes epidemiology, not benchmarks.

That translation is my work. I am a pharmacoepidemiologist (PhD, Sungkyunkwan University) with eleven years across hospital data analysis and CRO-based real-world evidence: causal inference (target trial emulation, propensity score methods, SCCS, negative control outcomes), OMOP CDM, claims and EMR studies, ICH M14. This repository is where I work out what the emerging regulatory landscape asks of that practice.

## Start here

**[Where AI Meets RWE: A Map of the Regulatory Landscape Across Four Jurisdictions](analyses/2026-07_ai-and-rwe-four-jurisdictions.md)**

A timeline and comparison across the US, EU, Japan, and Korea, with the five questions no regulator has yet answered. Updated as documents appear.

## Notes

**Analyses** — synthesis across documents

- [Where AI Meets RWE: four jurisdictions](analyses/2026-07_ai-and-rwe-four-jurisdictions.md)

**FDA** — [document landscape](regulators/fda/)

- [Guiding Principles of Good AI Practice in Drug Development](regulators/fda/2026-01_fda-ema-good-ai-practice.md) (with EMA, Jan 2026) — the burden of proof moves from the model to its use
- [Assessing EHR and Medical Claims Data](regulators/fda/2024-07_rwd-ehr-claims.md) (Jul 2024) — an AI extractor is an operational definition, and inherits everything one owes

**EMA**

- [AI in the Medicinal Product Lifecycle](regulators/ema/2024-09_ai-medicinal-product-lifecycle.md) (Sep 2024) — two risk axes, and the cell where evidence generation sits

## How the notes are built

Every note follows one format, set out in [`TEMPLATE.md`](TEMPLATE.md): summary, then interpretation, then open questions, then a changelog. Document status — statute, final guidance, draft, reflection paper — is stated every time, because comparing documents of different legal weight is the most common way to get this subject wrong.

Notes are filed under [`regulators/`](regulators/) by issuing agency. Corrections are recorded in each note's changelog rather than quietly edited.

## About

**Seongjun Byun (변성준)** — RWE Team Lead at a Korean CRO. PhD in pharmacoepidemiology. 26 peer-reviewed publications. Speaker at DIA Korea, PHUSE, and Korean Statistical Society meetings on causal inference, ICH M14, and real-world data study design.


## License

Notes: CC BY 4.0. Regulatory text quoted or summarized remains the property of its issuers; primary sources are linked in every note.
