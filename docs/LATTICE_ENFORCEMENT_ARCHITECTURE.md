# LATTICE Enforcement Architecture
Lawful Artifact Temporal & Technical Imprint Constraint Engine

## I. Status

This document defines enforcement architecture for LATTICE, the implementation instrument of Distributed Constraint Imprint Theory (DCIT).

This document does not modify DCIT doctrine.
It operationalizes compliance constraints defined in:

- DCIT Canon
- DCIT Structural Laws
- DCIT Compliance Contract
- DCIT Failure Conditions

---

## II. Architectural Posture

LATTICE is a deterministic, post-event, closed-set artifact processor.

It enforces:

- Case isolation
- Artifact allowlisting
- Expressive/semantic prohibition
- Attribution prohibition
- Non-probabilistic output closure
- Deterministic reproducibility
- Manifest-based auditability

LATTICE MUST prevent surveillance drift at the architectural level.

---

## III. Case Intake Policy (Mode Selection)

At case initialization, the user MUST select exactly one CASE_MODE.

The selected mode is immutable for the life of the case and is recorded in the execution manifest.

### Mode 0 — STRICT (Default)

If any prohibited field class is detected within the artifact set:

- Processing HALTS.
- No CIR is created.
- No constraint extraction occurs.
- An Inadmissible Input Report is generated.

This is the default and safest mode.

---

### Mode 1 — PARTITION

If prohibited field classes are detected:

- Prohibited fields are quarantined.
- Allowed fields proceed into CIR.
- Reconstruction proceeds exclusively on allowed fields.

Requirements:

- Quarantine MUST be structural and sealed.
- Prohibited content MUST NOT enter CIR.
- Prohibited content MUST NOT be parsed semantically.
- A Quarantine Manifest MUST be generated.
- The presence of quarantined content MUST be disclosed in the final report header.

---

### Mode Locking Rule

- CASE_MODE is written to the execution manifest at intake.
- CASE_MODE cannot be changed mid-case.
- Re-running a case under a different mode requires a new case identifier.
- Mode selection MUST appear in all output reports.

---

## IV. Prohibited Field Taxonomy (v0.1)

The following artifact classes are PROHIBITED:

1. Expressive Content
   - Message bodies
   - Communication content
   - Free-text narrative fields
   - Speech transcripts
   - Email body payloads
   - Chat content
   - Document content fields

2. Semantic Derivatives
   - Embeddings
   - Content-derived feature vectors
   - NLP classifications

3. Identity or Actor Fields
   - Person names
   - Suspect identifiers
   - Actor labels
   - Owner fields
   - Behavioral classifications

4. Risk/Probability Fields
   - Confidence scores
   - Likelihood rankings
   - Risk scores
   - Most likely descriptors

Detection MUST be structural (schema-based or container-based), not semantic.

---

## V. Artifact Allowlist (v0.1)

Permitted artifact classes include:

- Timestamps (monotonic or recorded)
- Event identifiers (non-identity)
- Resource metrics (CPU, memory, IO, queue depth, replication lag)
- Synchronization records
- State transition markers
- System process state changes (technical only)
- Network transport metadata (excluding payload content)
- Hashes and integrity markers
- Size, offset, and structural metadata

No field containing expressive semantic content may enter CIR.

---

## VI. Canonical Internal Representation (CIR v0.1)

CIR is the internal normalized structure used for constraint extraction.

CIR MAY contain:

- Technical event ID
- Technical timestamp
- Resource delta values
- Structural state transitions
- Synchronization markers
- Technical identifiers not linked to personhood
- Artifact hash references
- Case-bound baseline parameters

CIR MUST NOT contain:

- Message text
- Identity-linked identifiers
- Behavioral labels
- Intent markers
- Content-derived features
- Probabilistic values

CIR construction MUST be deterministic.

---

## VII. Enforcement Gates

### Gate 0 — Closed-Set Validation

Verifies:

- No streaming endpoints configured
- No live ingestion channels
- Artifact set hash recorded
- Case isolation directory created

Failure → Halt.

---

### Gate 1 — Prohibited Field Detection

Scans artifacts structurally for prohibited field classes.

Outputs:

- PROHIBITED_PRESENT (true/false)
- Field paths
- Field class
- Count
- Hash/offset references (optional)

No content values may be exposed.

Branching behavior:

- STRICT → Halt
- PARTITION → Quarantine + continue

---

### Gate 2 — CIR Validation

Ensures CIR contains only allowlisted field classes.

If prohibited class detected → Compliance failure.

---

### Gate 3 — Output Boundary Enforcement

Ensures outputs contain only:

- Necessary
- Impossible
- Undetermined

Rejects:

- Probability values
- Rankings
- Narrative text
- Attribution language
- Behavioral descriptors

---

## VIII. Deterministic Execution Model

Each run MUST record:

- Input artifact manifest hash
- Parser/normalizer version manifest
- Parameter manifest
- CASE_MODE
- Output manifest hash

Given identical manifests, outputs MUST be materially identical.

If not, compliance fails.

---

## IX. Quarantine Model (PARTITION Mode)

Quarantine MUST:

- Store only structural references (hashes, sizes, offsets)
- Prevent any semantic parsing
- Be inaccessible to constraint extraction logic
- Be sealed per case
- Be included in execution manifest

Quarantined content MUST NOT influence reconstruction.

---

## X. Output Artifacts

Permitted output artifacts:

- Constraint graphs
- Feasibility windows
- Exclusion zones
- Minimal action requirement statements
- Execution manifest
- Quarantine manifest (if applicable)

No narrative reconstruction is permitted within LATTICE.

---

## XI. Separation Statement

LATTICE enforces DCIT boundaries.
It does not expand, reinterpret, or relax DCIT doctrine.

If enforcement mechanisms drift beyond this architecture, DCIT compliance is invalid.
