# NeoMundi / ASRO — Round 2 Protocol
## Sections 4–7 — Structural Skeleton

**Version:** skeleton-0.1
**Status:** Pre-draft. Structural skeleton only — headings, intended purpose, and unresolved boundary questions. No procedural logic at this stage, per ASRO review guidance.
**Reads against:** `protocol.md` v0.2 (sections 1–3, sealed at role-boundary level).

---

## Purpose of this file

This file is **not** part of v0.2's sealed scope. It exists to make the downstream architecture of the protocol legible to ASRO before any procedural commitments are made.

Per ASRO review guidance, sections 4–7 must **flow from** the role boundary sealed in v0.2 rather than reopen it. The boundary crystallization (Annex A of `protocol.md`) governs every section below:

> — NeoMundi measures runtime behavior.
> — ASRO witnesses the reviewability conditions around the measurement process.
> — Neither layer absorbs the other.

The sections are ordered in the sequence required by ASRO: witness constraints → admissible evidence categories → comparison procedure → formal freeze and signature. Each later section depends on the prior one being sealed.

---

## Section 4 — Witness constraints

### 4.1 Intended purpose
To specify, for each artefact class enumerated in Section 2.3, the conditions under which a witnessing event is admissible: who may witness, under what separation guarantees, with what timestamping and signing requirements, and what constitutes a valid witness output.

### 4.2 Scope boundary
Section 4 defines **how** witnessing occurs. It does not define what counts as admissible evidence (Section 5), nor how artefacts are compared (Section 6), nor how the protocol is finally frozen (Section 7).

### 4.3 Unresolved boundary questions
- **Q4.1** — Does any witness constraint implicitly require ASRO to attest to runtime behavioral content rather than to governance-state conditions around the measurement process?
- **Q4.2** — Does any witness constraint implicitly require NeoMundi to act as a custody-chain verifier or infrastructure certifier?
- **Q4.3** — Are witness constraints stated symmetrically across artefact classes, or do they create an asymmetric burden that could be misread as one party validating the other?
- **Q4.4** — Is the timestamping mechanism specified at the protocol level, or delegated to infrastructure ASRO already attests to? (Risk of circularity if the latter is unbounded.)

---

## Section 5 — Admissible evidence categories

### 5.1 Intended purpose
To enumerate the categories of evidence that the protocol recognises as admissible for Phase C review, and to define the relationship between each category and the artefact classes of Section 2.3 / the witness constraints of Section 4.

### 5.2 Scope boundary
Section 5 defines **what** counts as evidence. It does not define the comparison procedure applied to that evidence (Section 6).

### 5.3 Unresolved boundary questions
- **Q5.1** — Does any evidence category collapse runtime behavioral measurement and governance attestation into a single admissibility test?
- **Q5.2** — Are NeoMundi measurement outputs and ASRO attestation outputs treated as evidence of distinct facts, or risk being read as mutually validating?
- **Q5.3** — Is there a meta-evidence category (evidence about the protocol's own execution) and, if so, who holds custody of it?
- **Q5.4** — Are the admissibility criteria independent of the eventual outcome of Round 2, or do they implicitly assume what a positive outcome looks like?

---

## Section 6 — Comparison procedure

### 6.1 Intended purpose
To define the post-hoc procedure by which the Reviewer (Section 3.2) compares sealed artefacts, evaluates the protocol's independent reviewability, and produces a Phase C report.

### 6.2 Scope boundary
Section 6 defines **how** the Reviewer reads the evidence record. It does not authorise the Reviewer to extend conclusions beyond the explicit non-conclusions of Section 1.2.

### 6.3 Unresolved boundary questions
- **Q6.1** — Does the comparison procedure preserve the asymmetry of Annex A, or does it implicitly fuse NeoMundi measurement outputs and ASRO attestation outputs into a single judgement?
- **Q6.2** — Is the Reviewer's discretion bounded enough that a Phase C report cannot, in practice, restate a non-conclusion (Section 1.2) as a conclusion?
- **Q6.3** — What is the protocol response when comparison reveals inconsistency between NeoMundi outputs and ASRO outputs? (Specifically: the protocol must not adjudicate runtime behavior via attestation, nor adjudicate governance state via measurement.)
- **Q6.4** — Is the comparison procedure reproducible by an independent third party using only sealed artefacts, with no operational role in Round 2?

---

## Section 7 — Formal freeze and signature

### 7.1 Intended purpose
To define the act by which the protocol is frozen at the point of pre-registration (Git tag), the signing parties, the binding scope of their signature, and the conditions under which the protocol may be amended post-freeze (in principle: none, except via a v-next that is itself pre-registered before any subsequent execution).

### 7.2 Scope boundary
Section 7 defines **when** and **how** the protocol becomes binding. It does not retroactively modify the role boundary sealed in v0.2.

### 7.3 Unresolved boundary questions
- **Q7.1** — Does a signature by NeoMundi or ASRO on the frozen protocol imply attestation of the other party's role beyond the explicit non-conclusions? (It must not.)
- **Q7.2** — What is the protocol's response to a discovered defect between freeze and execution? (Specifically: is a single corrective amendment admissible, or is a full re-freeze required?)
- **Q7.3** — Is the pre-registration trace (Git commit hash + timestamp) sufficient on its own, or is a co-signed external timestamp required?
- **Q7.4** — Does the signature event require operational separation from the Phase A custodians, to avoid a single party producing, sealing, and signing the protocol?

---

**End of structural skeleton.** No procedural logic is committed at this stage. Procedural drafting for Section 4 begins only after ASRO has reviewed this skeleton and the v0.2 role boundary has been confirmed as stable in light of it.
