# NeoMundi / ASRO — Round 2 Protocol

## Sections 5–7 — Structural Skeleton

**Version:** skeleton-0.2
**Status:** Pre-draft. Structural skeleton only — headings, intended purpose and unresolved boundary questions. No procedural logic is committed at this stage.
**Reads against:** `protocol.md` v0.3, in which Sections 1–4 are sealed.

---

## Purpose of this file

This file is not part of the sealed scope of `protocol.md` v0.3.

It exists to make the downstream architecture of Round 2 legible before procedural commitments are made for Sections 5–7.

Section 4 has been reviewed, integrated and sealed in v0.3. It establishes the witness constraints under which reviewability conditions may be witnessed without implying validation of runtime behavior.

The binding role boundary remains:

> — NeoMundi measures runtime behavior.
> — ASRO witnesses the reviewability conditions around the measurement process.
> — Neither layer absorbs the other.

For Sections 5–7, the controlling clarification remains:

> **ASRO witnesses reviewability conditions; it does not validate runtime behavior.**

Each section below must flow from these boundaries and must not reopen them.

---

## Completed Foundation — Section 4

Section 4 is sealed in `protocol.md` v0.3.

It establishes:

* operational separation between NeoMundi and ASRO during witnessing events;
* minimum requirements for a valid witness output;
* the distinction between witness output and measurement output;
* per-artefact witness constraints;
* exclusion of ASRO self-witnessing its own attestation output;
* mandatory third-party witnessing for ASRO attestation-output custody continuity;
* timestamping constraints designed to avoid circularity.

Sections 5–7 must treat these constraints as fixed unless a future protocol version explicitly amends them.

---

## Section 5 — Admissible Evidence Categories

### 5.1 Intended purpose

To define which sealed artefacts and supporting records are admissible for Phase C independent review.

Section 5 must specify the relationship between:

* the artefact classes defined in Section 2.3;
* the witness constraints defined in Section 4;
* the evidence available to the independent Reviewer during Phase C.

### 5.2 Scope boundary

Section 5 defines **what may be treated as evidence**.

It does not:

* determine whether NeoMundi measurement results are substantively correct;
* determine whether ASRO attestation conclusions are substantively valid;
* authorise fusion of measurement output and witness output into a single judgement;
* define the comparison procedure itself;
* authorise conclusions beyond the non-claims defined in Section 1.2.

### 5.3 Open questions

* **Q5.1** — Which artefact classes are admissible as primary evidence in Phase C?
* **Q5.2** — Which artefacts are admissible only conditionally, and what conditions apply?
* **Q5.3** — Which artefacts must be explicitly excluded from evidential use?
* **Q5.4** — How should NeoMundi measurement outputs and ASRO witness outputs remain evidence of distinct facts?
* **Q5.5** — Is a meta-evidence category required for evidence about protocol execution itself, and who holds its custody?
* **Q5.6** — How can admissibility criteria remain independent of the eventual outcome of Round 2?
* **Q5.7** — What additional custody constraints are required to prevent circularity across the full evidence chain?

---

## Section 6 — Independent Comparison Procedure

### 6.1 Intended purpose

To define the post-hoc procedure by which the independent Reviewer compares the sealed evidence record and produces a Phase C review report.

The procedure should make it possible to assess whether the protocol was executed in a manner that remains independently reviewable under its stated constraints.

### 6.2 Scope boundary

Section 6 defines **how the Reviewer examines the evidence record**.

It does not authorise the Reviewer to:

* validate Law E;
* validate runtime behavior;
* certify NeoMundi or ASRO;
* infer regulatory compliance;
* transform an explicit non-conclusion into a conclusion;
* fuse measurement and witnessing into a single substantive judgement.

### 6.3 Open questions

* **Q6.1** — What exact sequence should the Reviewer follow when comparing sealed artefacts?
* **Q6.2** — What is the minimum evidence set required for an independent review?
* **Q6.3** — What Reviewer discretion is permitted, and what must remain outside Reviewer interpretation?
* **Q6.4** — How should the protocol respond when artefacts are incomplete, inconsistent or unavailable?
* **Q6.5** — How should the Reviewer report an inconsistency without treating attestation as an adjudication of runtime behavior, or measurement as an adjudication of governance state?
* **Q6.6** — Can the procedure be reproduced by an independent third party using only sealed artefacts and no operational role in Round 2?

---

## Section 7 — Formal Freeze and Signature

### 7.1 Intended purpose

To define the formal act through which the complete protocol becomes frozen before execution.

This section must specify:

* the pre-registration mechanism;
* the protocol version and commit reference;
* the signing parties;
* the scope and limits of signatures;
* the handling of defects or required amendments discovered after freeze;
* the conditions under which a subsequent version must be created and pre-registered.

### 7.2 Scope boundary

Section 7 defines **when and how the protocol becomes binding for a specific execution**.

It does not:

* retrospectively alter the role boundary;
* imply that either party validates the operational role of the other;
* certify the substantive content of any future artefact;
* permit undocumented amendment after freeze.

### 7.3 Open questions

* **Q7.1** — What must be frozen before Phase A can open?
* **Q7.2** — Is the Git tag and commit hash sufficient, or must an external timestamping mechanism also be used?
* **Q7.3** — What exactly does each signature acknowledge, and what does it explicitly not acknowledge?
* **Q7.4** — Does protocol signature require operational separation from Phase A custodians?
* **Q7.5** — What happens when a defect is discovered between formal freeze and execution?
* **Q7.6** — Does a defect require a full re-freeze under a new version, or can a narrowly defined corrective procedure exist without compromising pre-registration?

---

## Required Drafting Sequence

1. Resolve the evidence-boundary questions for Section 5.
2. Draft and review Section 5.
3. Seal Section 5 in a new protocol version.
4. Resolve the Reviewer-scope questions for Section 6.
5. Draft and review Section 6.
6. Seal Section 6 in a new protocol version.
7. Resolve the freeze and signature questions for Section 7.
8. Draft and review Section 7.
9. Name the mandatory third-party witness required by Section 4.3.4.
10. Freeze, tag and sign the complete protocol before Phase A begins.

---

**End of skeleton-0.2.** No procedural logic for Sections 5–7 is committed by this document.
