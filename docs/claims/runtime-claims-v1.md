# NeoMundi / ASRO — Round 2 Runtime Claims

**Version:** v1
**Status:** Draft for ASRO review
**Scope:** Admissible runtime claims only

---

## 1. Purpose

This document defines the claims that may be made within the scope of NeoMundi / ASRO Round 2.

These claims are intentionally narrow.

They describe what the Round 2 protocol may document regarding runtime AI measurement, evidence generation, witnessing conditions and post-hoc reviewability.

They must not be interpreted as certification claims, universal validity claims or regulatory compliance claims.

---

## 2. Runtime measurement claim

NeoMundi measures runtime behavioral signals generated during AI system execution.

The protocol may document that:

* runtime behavioral signals were generated during execution;
* those signals were recorded according to a defined protocol version;
* the measurement process produced timestamped artefacts;
* the resulting artefacts were preserved for post-hoc review;
* the measurement process can be examined through a bounded evidence record.

---

## 3. Reviewability claim

Round 2 may document the conditions under which a third-party Reviewer can examine sealed artefacts after execution.

The protocol may document that:

* artefacts were generated under a defined execution protocol;
* artefacts were sealed and preserved;
* artefacts can be compared post hoc;
* the comparison procedure is bounded by the protocol;
* the Reviewer can examine the evidence record without participating in the runtime execution;
* the Reviewer can identify whether the expected artefacts are present, missing, inconsistent or incomplete.

---

## 4. Role-separation claim

Round 2 may document that the protocol preserves a strict separation of roles:

* NeoMundi measures runtime behavioral signals;
* ASRO witnesses reviewability conditions around the measurement process;
* the Reviewer examines sealed artefacts after execution;
* no layer absorbs, certifies or substitutes for another layer.

---

## 5. Evidence-record claim

Round 2 may document the existence of an evidence record containing distinct artefact classes.

The protocol may document that:

* NeoMundi measurement outputs and ASRO witnessing outputs are preserved as distinct artefacts;
* each artefact class refers to a distinct fact category;
* the evidence record does not collapse runtime measurement and governance-state witnessing into a single output;
* artefacts can be traced to a protocol version;
* missing or inconsistent artefacts can be identified during review.

---

## 6. Protocol-freeze claim

Round 2 may document that:

* the protocol was versioned before execution;
* the applicable protocol version was frozen before execution;
* the execution was associated with a traceable version identifier;
* substantive amendments require a new documented version;
* previous versions remain preserved as part of the audit trail.

---

## 7. Reproducibility claim

Round 2 may document whether an independent third party can re-examine the sealed evidence record using the documented comparison procedure.

Within this scope, reproducibility means:

* the evidence record is accessible to the Reviewer;
* the comparison steps are documented;
* the expected artefact classes are defined;
* the protocol version is identifiable;
* the Reviewer can reproduce the post-hoc examination process.

Reproducibility does not mean that every runtime event, infrastructure condition or model behavior is universally reproducible under all external conditions.

---

## 8. Bounded interpretation

Any conclusion produced under Round 2 must remain bounded by:

* the defined protocol version;
* the documented execution context;
* the available sealed artefacts;
* the explicit role boundary;
* the explicit non-claims;
* the known limitations.

No conclusion may extend beyond the evidence actually generated and preserved during Round 2.

---

## 9. Intended future use

The claims documented in this file may support:

* independent review;
* technical due diligence;
* governance discussions;
* procurement review;
* partner onboarding;
* client-specific deployment documentation;
* future specification work.

They must always be presented as bounded protocol claims, not as certification claims.
