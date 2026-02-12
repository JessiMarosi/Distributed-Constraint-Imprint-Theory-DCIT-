# DCIT Compliance Contract

## I. Status

This document defines normative compliance requirements for any system claiming adherence to Distributed Constraint Imprint Theory (DCIT).

Normative language follows RFC-style terminology:

- MUST
- MUST NOT
- SHALL
- SHALL NOT
- REQUIRED
- PROHIBITED

Failure to satisfy these requirements invalidates DCIT compliance.

---

## II. Artifact Input Requirements

1. A DCIT-compliant system MUST operate exclusively on post-event artifact sets.

2. Artifact sets MUST be closed. Continuous ingestion, streaming telemetry, or live data feeds are PROHIBITED.

3. Permitted artifact classes include:
   - Logs
   - Metadata
   - Timestamps
   - Resource metrics
   - Synchronization records
   - State transition artifacts

4. The system MUST NOT require expressive or semantic content to derive constraints.

5. Expressive artifact classes are PROHIBITED, including:
   - Message bodies
   - Communication content
   - Speech transcripts
   - Semantic embeddings
   - Content-derived features

---

## III. Schema Constraints

1. Data schemas MUST NOT contain fields capable of storing expressive or semantic content.

2. Data schemas MUST NOT include fields designed for:
   - Identity labeling
   - Behavioral categorization
   - Intent inference
   - Risk scoring

3. If expressive or actor-linked fields are introduced, compliance SHALL fail.

---

## IV. Case Isolation Requirements

1. Each reconstruction MUST be processed in isolation.

2. The system MUST NOT:
   - Aggregate priors across cases
   - Reuse learned parameters from prior cases
   - Construct behavioral baselines across individuals or entities

3. Adaptive or learning-based cross-case systems are PROHIBITED.

---

## V. Output Requirements

1. Outputs MUST conform to necessary-condition reasoning.

2. Permitted output classifications are limited to:
   - Necessary
   - Impossible
   - Undetermined

3. Outputs MUST NOT include:
   - Probability rankings
   - Confidence scores
   - Likelihood statements
   - Risk scores
   - Most likely scenario framing

4. Outputs MUST describe system-state constraints only.

5. Actor attribution, identity claims, intent assertions, and behavioral descriptions are PROHIBITED.

---

## VI. Determinism Requirements

1. Given identical:
   - Artifact sets
   - Normalization rules
   - Configuration parameters

   The system MUST produce materially identical outputs.

2. Undocumented nondeterministic processes are PROHIBITED.

---

## VII. Monitoring Prohibition

1. The system MUST NOT support:
   - Real-time monitoring
   - Continuous telemetry
   - Background collection agents
   - Real-time alerting mechanisms

2. If such capabilities exist, the system SHALL NOT be designated as DCIT-compliant.

---

## VIII. Narrative Restriction

1. The system MUST NOT generate story-form reconstructions.

2. Permitted output artifacts include:
   - Constraint graphs
   - Feasibility windows
   - Exclusion zones
   - Minimal action requirement statements

Narrative interpretation, if required, SHALL occur outside the DCIT system boundary.

---

## IX. Compliance Validation

Any system claiming DCIT compliance MUST be evaluated against:

- DCIT Canon
- DCIT Structural Laws
- DCIT Failure Conditions
- This Compliance Contract

Failure under any document invalidates DCIT designation.

---

## X. Binding Effect

This document is binding for any implementation claiming DCIT compliance.

Deviation requires reclassification and removal of DCIT designation.