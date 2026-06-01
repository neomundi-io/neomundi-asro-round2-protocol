# NeoMundi / ASRO — Round 2 Known Limitations

**Version:** v1
**Status:** Draft for ASRO review
**Scope:** Known limitations applicable to the current Round 2 protocol draft

---

## 1. Purpose

This document records the known limitations of the NeoMundi / ASRO Round 2 protocol.

These limitations must remain visible throughout:

* protocol drafting;
* execution planning;
* artefact generation;
* post-hoc review;
* public communication;
* client-facing interpretation.

The purpose of this file is not to weaken the protocol. It is to preserve a clear boundary between what Round 2 can document and what remains outside its current scope.

---

## 2. Limited scope of Round 2

Round 2 is a bounded specification and reviewability exercise.

It is not intended to establish:

* universal scientific validity;
* full industrial validation;
* regulatory compliance;
* certification;
* complete model evaluation;
* complete infrastructure evaluation;
* exhaustive detection of AI failure modes.

Round 2 documents a defined execution context and a defined evidence record.

---

## 3. Runtime-signal limitation

NeoMundi runtime signals are measured signals produced during AI system execution.

The current protocol does not establish that:

* every runtime variation has a unique causal interpretation;
* every runtime variation corresponds to a semantic failure;
* every runtime variation corresponds to a governance failure;
* every relevant model behavior is fully captured by the current metric set;
* the runtime signal alone is sufficient to adjudicate model quality or model truth.

---

## 4. Information-density limitation

The information-density metric is still undergoing technical stabilization.

Current known constraints include:

* runtime performance remains dependent on judge-layer latency;
* the self-hosted judge is currently too slow for the intended execution scale;
* the information-density value must not be treated as final until the implementation has been stabilized;
* no definitive interpretation should be attached to information-density outputs generated before technical validation.

The final specification of the information-density metric will be documented after stabilization.

---

## 5. Judge-layer limitation

The current judge layer remains a bounded interpretive component.

Known limitations include:

* judge latency may affect execution time;
* judge outputs must not be interpreted as ground truth;
* judge outputs may remain sensitive to implementation choices;
* single-judge dependency limits robustness;
* inter-judge disagreement is not yet integrated into the current protocol;
* double-judge validation may be introduced in a subsequent version.

The judge layer supports interpretation and evidence generation. It does not adjudicate universal semantic truth.

---

## 6. Evidence-record limitation

The Round 2 evidence record is bounded by the artefacts actually generated and preserved during execution.

The protocol does not guarantee that:

* every relevant event is captured;
* every implementation defect is detectable;
* every infrastructure defect is detectable;
* every custody-chain defect is detectable;
* every ambiguity can be resolved post hoc;
* incomplete artefacts can always be reconstructed.

A missing, inconsistent or incomplete artefact must remain reportable as such.

---

## 7. Review limitation

The Reviewer examines sealed artefacts after execution.

The Reviewer does not:

* participate in runtime execution;
* certify NeoMundi;
* certify ASRO;
* certify infrastructure;
* replace legal review;
* replace regulatory review;
* replace scientific peer review;
* extend conclusions beyond the frozen protocol.

The Reviewer report is bounded by the available evidence record.

---

## 8. Reproducibility limitation

Round 2 may support reproducible post-hoc examination of sealed artefacts.

This does not mean that:

* every external runtime condition can be reproduced identically;
* every model behavior will recur identically;
* every provider environment is fully controllable;
* every infrastructure dependency is fully reproducible;
* every result generalizes beyond the documented execution context.

Reproducibility must be interpreted within the bounded scope of the protocol.

---

## 9. Versioning limitation

Any conclusion produced during Round 2 applies only to:

* the frozen protocol version;
* the documented metric implementation;
* the documented judge-layer version;
* the documented execution context;
* the preserved artefacts;
* the known limitations recorded at the time of execution.

A later implementation change requires a new documented protocol version.

---

## 10. Future enrichment

The following improvements may be considered in future protocol versions:

* stabilized information-density implementation;
* reduced judge-layer latency;
* double-judge comparison;
* inter-judge disagreement analysis;
* expanded artefact schemas;
* stronger custody-chain documentation;
* additional execution cases;
* client-specific deployment profiles;
* external technical review.
