# ASRO Review Tracker

## Purpose

This tracker records the status of methodological review, boundary decisions, open questions and next actions for NeoMundi × ASRO Round 2.

It is a working coordination record. It does not amend the sealed protocol unless a protocol version is explicitly updated and tagged.

---

## Current Protocol Status

| Protocol area                                                  | Status | Notes                                                        |
| -------------------------------------------------------------- | ------ | ------------------------------------------------------------ |
| Sections 1–3 — claim limits, custody structure, observer roles | Sealed | Carried forward from v0.2, unchanged in v0.3                 |
| Section 4 — witness constraints                                | Sealed | Integrated and sealed in v0.3 following ASRO boundary review |
| Section 5 — admissible evidence categories                     | Open   | Procedural drafting pending                                  |
| Section 6 — independent comparison procedure                   | Open   | Depends on Section 5                                         |
| Section 7 — formal freeze and signature procedure              | Open   | Depends on Sections 5–6                                      |

---

## Confirmed Boundary Decisions

| ID | Decision                                                                                                | Status    |
| -- | ------------------------------------------------------------------------------------------------------- | --------- |
| B1 | NeoMundi measures runtime behavior.                                                                     | Confirmed |
| B2 | ASRO witnesses reviewability conditions around the measurement process.                                 | Confirmed |
| B3 | ASRO does not validate runtime behavior or Law E.                                                       | Confirmed |
| B4 | NeoMundi does not witness, attest or co-attest.                                                         | Confirmed |
| B5 | Witness output and measurement output remain distinct evidence classes.                                 | Confirmed |
| B6 | ASRO cannot independently witness custody continuity of its own attestation output.                     | Confirmed |
| B7 | A third-party witness is required for ASRO attestation output custody continuity.                       | Confirmed |
| B8 | Git timestamping is admissible only when the repository infrastructure is outside the witnessed system. | Confirmed |

---

## Open Questions

| ID  | Question                                                                                                                             | Owner           | Needed before  |
| --- | ------------------------------------------------------------------------------------------------------------------------------------ | --------------- | -------------- |
| Q3  | Beyond timestamping, what custody conditions are required to avoid circularity across the full evidence chain?                       | ASRO + NeoMundi | Section 5      |
| Q4  | Are the non-claims strong enough to prevent over-generalisation after execution, including in public communication?                  | ASRO + NeoMundi | Section 5      |
| Q5  | What minimum evidence set would allow a genuinely independent third party to review the execution without operational participation? | ASRO            | Section 5      |
| Q6  | Which evidence classes are admissible, excluded or only conditionally admissible in Phase C?                                         | ASRO + NeoMundi | Section 5      |
| Q7  | What Reviewer discretion is permitted, and what must remain outside Reviewer interpretation?                                         | ASRO            | Section 6      |
| Q8  | What exact comparison procedure should the Reviewer follow across sealed artefacts?                                                  | ASRO + NeoMundi | Section 6      |
| Q9  | What formal act, signatures and version references make the protocol frozen before Phase B?                                          | ASRO + NeoMundi | Section 7      |
| Q10 | Who can act as the third-party witness required by Section 4.3.4?                                                                    | NeoMundi        | Before Phase B |

---

## Next Drafting Sequence

1. Draft Section 5 — admissible evidence categories.
2. Review and resolve Q3–Q6.
3. Draft Section 6 — independent comparison procedure.
4. Review and resolve Q7–Q8.
5. Draft Section 7 — formal freeze and signature procedure.
6. Name the third-party witness for ASRO attestation output.
7. Freeze and tag the complete protocol.
8. Prepare Phase A artefacts and protocol log.

---

## Requested ASRO Review

For the next review cycle, ASRO is invited to comment on:

1. the minimum admissible evidence set for Phase C;
2. evidence that must be excluded or treated as conditional;
3. residual risks of circularity or self-attestation;
4. the scope and limits of Reviewer interpretation;
5. the conditions required for formal protocol freeze;
6. whether any remaining wording risks implying mutual validation or certification.

---

## Change Log

| Date        | Change                                                        | Status   |
| ----------- | ------------------------------------------------------------- | -------- |
| June 2026   | Sections 1–3 sealed at role-boundary level.                   | Complete |
| June 2026   | Section 4 boundary review completed and integrated into v0.3. | Complete |
| Next cycle  | Section 5 drafting and evidence-boundary review.              | Pending  |
| Later cycle | Sections 6–7 drafting, freeze and execution preparation.      | Pending  |
