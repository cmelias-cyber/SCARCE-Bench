# SCARCE-Bench Project Plan

## Scope

A 9-month project with two phases. Phase 1 uses the MAPI archive as a controlled low-data testbed. Phase 2 repeats the method on a second sparse domain with an outside collaborator.

## Design

- At least 150 prompts, balanced across two failure modes and across traditions
- Four general-purpose frontier LLM families plus a MAPI RAG assistant, versions pinned at run time
- Three runs per prompt per system (2,250 scored outputs per domain)
- A private held-out set to guard against training contamination
- Blinded scoring, double-coding on a defined subset, inter-rater reliability reported (Krippendorff's alpha)
- Results reported separately for each tradition
- The same RAG pipeline is also deployed as MAPI's public assistant, so scripted benchmark behavior can be compared with behavior on real user questions

## Milestones

- Month 2: rubric validated (target Krippendorff's alpha of 0.7 or higher on a pilot set), advisors and first raters confirmed, corpus sources and permissions documented
- Month 4: assistant deployed to a small pilot group, Phase 1 runs complete, held-out set locked
- Month 6: in-person sessions complete, second-domain pilot running
- Month 8: public release of harness, dataset, and demo
- Month 9: empirical report

## Status

Work in progress. See the README for what is currently public.
