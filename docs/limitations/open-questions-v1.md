# NeoMundi / ASRO — Round 2 Open Questions

**Version:** v1
**Status:** Draft for ASRO review
**Scope:** Questions to resolve before formal protocol freeze

---

## 1. Purpose

This document records the unresolved questions that must be examined before the NeoMundi / ASRO Round 2 protocol is formally frozen.

These questions are intentionally separated from known limitations.

A known limitation is an accepted boundary of the current protocol.

An open question is a point that still requires clarification, review or decision.

---

## 2. Witnessing questions

* What conditions make a witnessing event admissible?
* Who may act as witness for each artefact class?
* What operational separation is required between NeoMundi, ASRO and the Reviewer?
* Which witnessing outputs must be timestamped?
* Which witnessing outputs must be signed?
* Does any witnessing constraint risk implying that ASRO validates NeoMundi runtime content?
* Does any witnessing constraint risk implying that NeoMundi certifies ASRO infrastructure?

---

## 3. Evidence questions

* Which artefact classes are required for Phase C review?
* Which artefacts are mandatory?
* Which artefacts are optional?
* Which artefacts may remain internal?
* Which artefacts may be shared with the Reviewer?
* Which artefacts may later become public?
* Should the evidence record include meta-evidence about the protocol execution itself?
* Who holds custody of each artefact class?
* How should missing or incomplete artefacts be reported?

---

## 4. Comparison-procedure questions

* What comparison steps must the Reviewer follow?
* Which comparisons are mandatory?
* Which comparisons remain discretionary?
* How should inconsistencies between NeoMundi outputs and ASRO outputs be reported?
* How can the protocol preserve the distinction between runtime measurement and governance-state witnessing?
* Can an independent third party reproduce the post-hoc comparison using sealed artefacts only?
* What conclusions may the Reviewer state?
* What conclusions must remain explicitly excluded?

---

## 5. Freeze and signature questions

* What constitutes the formal freeze event?
* Is a Git tag sufficient?
* Is a commit hash sufficient?
* Is an external timestamp required?
* Is a co-signed external timestamp required?
* Which parties must sign the frozen protocol?
* Does signature imply acceptance of the other party's outputs?
* What happens if a defect is discovered after freeze but before execution?
* Does any substantive correction require a full new version?
* Must the previous frozen version remain preserved?

---

## 6. Metric questions

* What is the final stabilized implementation of information density?
* What latency threshold is acceptable for the self-hosted judge?
* Which judge-layer version will be used during Round 2?
* Is a single judge sufficient for Round 2?
* Should double-judge comparison be deferred to a later version?
* How should judge-layer limitations be documented?
* Which metric implementation details must be versioned?
* Which metrics are included in the evidence record?
* Which metrics remain internal?

---

## 7. Artefact-format questions

* What is the minimum artefact schema?
* Which identifiers are required?
* Which timestamps are required?
* Which hashes are required?
* Which version identifiers are required?
* Which fields are required for post-hoc review?
* Which fields must remain private?
* What constitutes a sealed artefact?
* What constitutes a reviewer package?

---

## 8. Communication questions

* Which Round 2 conclusions may be communicated publicly?
* Which statements must remain internal?
* Which wording avoids any implication of certification?
* Which wording avoids any implication of universal scientific validation?
* Which wording avoids any implication of regulatory compliance?
* How should the future contribution paper distinguish specification, reviewability and validation?

---

## 9. Questions for ASRO review

ASRO review should specifically examine:

1. Whether the role boundary remains stable across the draft protocol.
2. Whether any proposed witnessing mechanism implies mutual validation.
3. Whether the evidence categories remain distinct.
4. Whether the Reviewer scope is sufficiently bounded.
5. Whether the freeze mechanism is sufficiently explicit.
6. Whether the known limitations are visible and correctly framed.
7. Which questions must be resolved before procedural drafting is finalized.
