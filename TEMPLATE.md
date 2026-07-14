# Note Template & Conventions

This file defines the single format used for every document note in this repository. Copy the skeleton at the bottom to start a new note.

---

## 1. File placement & naming

- Path: `regulators/<issuer>/` or `standards/<body>/`
- Filename: `YYYY-MM_short-slug.md`
  - `YYYY-MM` = **publication date of the source document** (not the date I wrote the note)
  - Slug: lowercase, hyphenated, ≤ 6 words. Example: `2026-01_good-ai-practice-drug-development.md`
- Draft vs final guidance: when a draft is finalized, create a **new file** for the final version and add a pointer in the old note's changelog. Never overwrite history.

## 2. Front matter (YAML)

```yaml
---
title: "Full official document title"
issuer: FDA            # FDA | EMA | ICH | EU | NIST | ISO | MFDS | KR-GOV | BfArM | TGA | HSA | CDISC | ...
domain: [ai]           # ai | rwe | dtx | standards  (one or more)
doc_type: draft-guidance   # draft-guidance | final-guidance | regulation | standard | reflection-paper | framework
published: 2026-01
legal_status: non-binding  # binding | non-binding | voluntary-standard
jurisdiction: US
source_url: ""
tags: [ai-governance, drug-development, validation]
note_status: in-progress   # in-progress | published
last_reviewed: 2026-07-14
---
```

### Tag taxonomy (extend as needed, but reuse before inventing)

`ai-governance` · `validation` · `transparency` · `lifecycle-management` · `data-provenance` · `data-standards` · `rwe` · `drug-development` · `medical-device` · `pharmacovigilance` · `human-oversight` · `risk-management` · `korea` · `eu` · `us` · `ich` · `apac`

## 3. Section structure

Every note has exactly these sections, in this order.

### TL;DR
≤ 3 bullets. Written last. The third bullet should be the practice implication, not a summary point.

### 1. Document profile
A table: issuer, publication date, legal status, comment period (if open), scope (who/what it applies to), relationship to other documents (supersedes / complements / implements).

### 2. What the document says
The faithful summary. Rules:
- Follow the source document's own structure (its section numbers) so readers can trace back.
- No opinion here. If a sentence contains "should", it must be the *document's* "should", not mine.
- Quote sparingly (short phrases only) and always with section citations like `(§ III.B)`.
- Length discipline: this section should be *shorter* than Section 3. If the summary dominates, the note has failed its purpose.

### 3. What it means in practice — an evidence-generation reading
The interpretation. Explicitly framed as my opinion. Recommended sub-lenses (use those that apply, delete the rest):
- **Study design** — does this change how protocols, estimands, or analysis plans are written?
- **Data & provenance** — new expectations for data lineage, AI-derived variables, curation documentation?
- **Validation burden** — what evidence of model/variable/endpoint performance will be expected, and against what reference standard?
- **Evidentiary standard** — what level of evidence does this document treat as sufficient (RCT vs RWE vs single-arm + external control vs DiGA-style provisional), and for what claim?
- **Documentation & audit** — what artifacts must exist when a regulator or sponsor asks?
- **Who is affected** — sponsor, CRO, data holder, device/DTx manufacturer, vendor: whose workload changes?

> Domain note: not every lens applies to every document. For a **DTx** guidance the *evidentiary standard* and *study design* lenses usually dominate; for an **AI** guidance, *validation burden* and *provenance*; for an **RWE** guidance, *study design* and *provenance*. Delete the lenses that don't apply.

Each claim in this section should be arguable — a reader should be able to disagree with it. If nobody could disagree, it belongs in Section 2.

### 4. Cross-references
Links to related notes in this repo, with one line on the relationship ("stricter than", "fills the gap left by", "conflicts with").

### 5. Watchlist & open questions
Concrete things to monitor: comment deadlines, promised follow-up guidance, ambiguities the field is debating. Phrase as questions where possible.

### 6. Changelog
`YYYY-MM-DD — what changed`. First entry is the note's creation.

## 4. Writing rules

1. **Fact/opinion separation is the product.** Sections 2 and 3 never bleed into each other.
2. English is the working language; Korean regulatory terms appear in parentheses on first use, e.g., "Korea AI Framework Act (AI 기본법)".
3. Link the primary source in front matter and on first mention. Never rely on secondary coverage for a claim about what a document says.
4. Prefer prose over bullet walls in Section 3 — interpretation reads as argument, not as a checklist.
5. Every note update touches three places: the note itself, `index/coverage-map.md`, and (if topical) `index/by-topic.md`.

---

## Skeleton (copy from here)

```markdown
---
title: ""
issuer:
doc_type:
published:
legal_status:
jurisdiction:
source_url: ""
tags: []
note_status: in-progress
last_reviewed:
---

# <Short title>

## TL;DR
-
-
-

## 1. Document profile

| | |
|---|---|
| Issuer | |
| Published | |
| Legal status | |
| Comment period | |
| Scope | |
| Relationship to other documents | |

## 2. What the document says

## 3. What it means in practice — an evidence-generation reading

### Study design

### Data & provenance

### Validation burden

### Documentation & audit

## 4. Cross-references

## 5. Watchlist & open questions

## 6. Changelog
- YYYY-MM-DD — Note created.
```
