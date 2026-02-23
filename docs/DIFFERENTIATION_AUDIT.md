# DCIT — Differentiation Audit (Template)
Status: Template (No conclusions asserted)
Scope: Comparative structural extraction only (no doctrine modification)

---

# Selection Methodology

Candidate frameworks will be selected based on:

- Academic citation frequency
- Relevance to digital forensic reconstruction
- Explicit reconstruction or event correlation scope
- Availability of formal documentation or primary sources

Strong candidates that present potential structural overlap with DCIT will be prioritized.
Straw-man comparisons are prohibited.

---

# Audit Integrity Rule

Comparisons must be based on documented, published primary sources.
No inference beyond documented claims is permitted.
If documentation is ambiguous, the result must be recorded as Undetermined.

DCIT canonical documents remain read-only authority during this audit.

---

# Redundancy Threshold Definition

Redundancy risk is considered High only if a candidate framework:

- Enforces post-event-only restriction,
- Prohibits expressive or semantic content processing,
- Prohibits attribution and intent inference,
- Restricts outputs to non-probabilistic necessary-condition reasoning,
- Enforces case isolation,
- Requires deterministic reproducibility,
- Defines explicit invalidation or failure criteria.

Partial overlap does not constitute redundancy.

---

# 1) DCIT Reference Baseline (Extraction Targets)

## DCIT Structural Commitments (Must Hold)

- Post-event only (closed artifact sets; no streaming ingestion; no monitoring)
- Case isolation (no cross-case learning; no shared state)
- Artifact-only inputs; expressive/semantic content prohibited
- Output states restricted to: Necessary / Impossible / Undetermined
- No probability, no rankings, no confidence scores, no risk scores
- No attribution, no identity inference, no intent inference
- No narrative generation
- Deterministic reproducibility under identical inputs

---

# 2) Comparison Set (Populate Later)

Select representative models/frameworks from:

- Digital forensic reconstruction methodologies
- DFIR correlation frameworks
- Formal constraint-based reconstruction approaches
- Incident reconstruction standards or guidance

Do not cherry-pick weak comparisons.

---

# 3) Extraction Schema (One Record Per Candidate)

## Candidate Record

- Candidate Name:
- Type:
- Source(s):
- Year / Version:

### A) Scope Posture
- Post-event only? (Y/N/Partial)
- Allows monitoring / live ingestion? (Y/N/Partial)
- Closed artifact sets required? (Y/N/Partial)

### B) Evidence Model
- Artifact-only? (Y/N/Partial)
- Permits message bodies / content inspection? (Y/N/Partial)
- Permits semantic interpretation? (Y/N/Partial)

### C) Output Epistemics
- Output types:
- Uses probability / likelihood / confidence? (Y/N/Partial)
- Uses ranking / scoring? (Y/N/Partial)
- Permits narrative conclusions? (Y/N/Partial)

### D) Attribution & Intent
- Actor attribution in scope? (Y/N/Partial)
- Identity inference in scope? (Y/N/Partial)
- Intent inference in scope? (Y/N/Partial)

### E) Cross-Case Behavior
- Cross-case learning / baselines allowed? (Y/N/Partial)
- Persistent knowledge base / model? (Y/N/Partial)

### F) Determinism & Reproducibility
- Determinism explicitly required? (Y/N/Partial)
- Reproducibility requirements described? (Y/N/Partial)
- Parameter disclosure required? (Y/N/Partial)

### G) Failure / Invalidation Criteria
- Explicit compliance failure conditions? (Y/N/Partial)
- Explicit scope invalidation triggers? (Y/N/Partial)

### H) Closest Overlap With DCIT
- Overlap surface:
- Key deltas:
- Potential redundancy risk level: (Low / Medium / High) — justified with extracted facts only

---

# 4) Summary Matrix (Populate Later)

| Candidate | Post-event only | No monitoring | No content | No probability | No attribution | 3-state outputs | Case-isolated | Deterministic | Explicit failure criteria |
|----------|------------------|--------------|------------|----------------|----------------|-----------------|--------------|--------------|---------------------------|
| (TBD)    |                  |              |            |                |                |                 |              |              |                           |

---

# 5) Audit Conclusion (Leave Blank Until Populated)

Conclusion options:

A) Structurally differentiated  
B) Redundancy risk detected  
C) Undetermined — additional sources required

---

This audit does not modify DCIT doctrine.
