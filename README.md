# NeoMundi × ASRO — Round 2 Methodology Protocol

## Purpose

This private repository documents Round 2 of the NeoMundi × ASRO methodological collaboration.

Round 2 is a specification and independent reviewability exercise.

Its purpose is to document the conditions under which a third-party Reviewer can examine a NeoMundi runtime AI measurement process using sealed artefacts, while preserving a strict separation between:

* NeoMundi runtime behavioral measurement;
* ASRO governance-state witnessing;
* independent post-hoc review.

## Core Question

Can a runtime measurement process remain reviewable after execution through versioned, sealed and role-bounded artefacts, without overstating what the measurement itself proves?

## Why This Matters

A runtime signal may reveal behavioral variability, factual-risk indicators, measurement limits or changes in observed conditions.

However, a signal is not automatically:

* a truth claim;
* a safety certification;
* an attestation;
* an authorization;
* a governance decision;
* an execution instruction.

Round 2 therefore focuses on the discipline required to preserve the evidence, limits and reconstructibility of a measurement process for later review.

## Scope

Round 2 is a methodological and non-production exercise.

It does not involve:

* customer data;
* proprietary prompts or outputs;
* live production decisions;
* delegated governance authority;
* automatic execution control;
* legal certification;
* public performance claims.

Round 2 does not certify NeoMundi, ASRO, a model, a provider or a measurement result.

## Role Boundary

The protocol is governed by the following role boundary:

* **NeoMundi** measures runtime behavior and produces the relevant measurement artefacts.
* **ASRO** witnesses the reviewability conditions surrounding the measurement process.
* **The independent Reviewer** compares sealed artefacts after execution.
* **No layer absorbs, certifies or replaces the role of another layer.**

NeoMundi does not claim that a measurement record alone determines truth, safety, admissibility, authority or execution permission.

ASRO does not validate NeoMundi’s operational role or certify the runtime behavioral signal.

## Round 2 Objectives

Round 2 aims to:

1. freeze and version a reviewable protocol;
2. document a clear model of role boundaries;
3. define witness constraints for each artefact class;
4. identify admissible evidence categories;
5. define a bounded independent comparison procedure;
6. establish freeze and signature procedures;
7. produce a sealed evidence record;
8. support a Phase C independent review;
9. document conclusions, exclusions and unresolved questions.

## Expected Deliverables

Round 2 is expected to produce:

1. a frozen and versioned protocol;
2. a documented role-boundary model;
3. witness constraints for each artefact class;
4. a list of admissible evidence categories;
5. a bounded comparison procedure for the independent Reviewer;
6. a formal freeze and signature procedure;
7. a sealed evidence record;
8. a Phase C independent review report;
9. a reusable documentation package for future due diligence;
10. a contribution paper authored by James after completion of Round 2.

## Reuse Value

The Round 2 package may become a reusable trust and due-diligence asset for future NeoMundi discussions.

It can help future clients, partners, reviewers or investors understand:

* what NeoMundi measures;
* what NeoMundi does not claim to measure;
* how measurement artefacts are generated and sealed;
* how responsibilities remain separated;
* how a third party can review the process;
* how protocol versions and amendments are handled;
* which conclusions are admissible and which remain excluded.

Its value is methodological discipline and reviewability, not certification.

## Repository Map

* `protocol.md` — Round 2 protocol, scope and methodological assumptions
* `round2-value-and-deliverables.md` — strategic value, deliverables and reuse conditions
* `asro-review-tracker.md` — review points, responses, decisions and unresolved questions
* `sections-4-7-skeleton.md` — draft structure for remaining protocol sections
* `docs/` — supporting material, sealed artefacts, manifests and methodological references

## Relation to the Wider Governance Research Program

This Round 2 protocol forms one methodological track within NeoMundi’s broader research on runtime observation, governance and reviewability.

Other NeoMundi research exercises may explore complementary questions, including:

* how runtime observations can inform admissibility;
* how uncertainty or discontinuity may affect execution boundaries;
* how decisions can remain reconstructible;
* how measurement, interpretation, authority and consequence can remain separated.

Those exercises are separate from this ASRO protocol.

ASRO’s specific role in Round 2 is limited to proof discipline, artefact reliability, witnessing conditions, reviewability and authority separation.

## Working Principles

* **Measurement is not authority.**
* **A score is not a decision.**
* **A sealed artefact is not a certification.**
* **Observation, interpretation, witnessing and authority must remain distinguishable.**
* **A record must retain its limitations, not only its signals.**
* **No contributor is represented beyond their explicit scope.**
* **Methodological findings remain traceable to artefacts, versions and assumptions.**

## Status

**Status:** Active
**Version:** v0.1
**Visibility:** Private
**Nature:** Methodological protocol and independent reviewability exercise
