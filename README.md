# SCARCE-Bench

**Sparse-knowledge Certainty, Abstention, RAG, and Conflation Errors Benchmark**

SCARCE-Bench is an open-source evaluation project that tests how frontier language models and retrieval-augmented (RAG) systems behave when evidence is sparse. Instead of abstaining, models often give fluent, confident answers that hide missing evidence, merge distinct sources, and overstate contested claims. This project measures that behavior.

The project is run through the Mesopotamian Aroma Preservation Initiative (MAPI), a nonprofit founded by Charlie-Moshé Elias. MAPI's archive of rare, contested, and under-documented sources is the first testbed.

**Status:** work in progress. The prompt schema and draft rubric are public. Pilot testing, expert validation, and full evaluation runs are planned.

## Failure modes tested

1. **Source conflation and flattening.** Distinct sources, eras, communities, and diasporic lineages collapse into a generic default. The benchmark tests tradition identification, cross-tradition conflation, minority-perspective omission, dominant-narrative defaults, and representation balance.
2. **False certainty and calibration failures.** Under-documented or contested claims are stated as settled. The benchmark tests claim support, source attribution, citation entailment, uncertainty calibration, and responsible abstention.

## Design

- At least 150 prompts, balanced across both failure modes and across the traditions in the archive
- Four current frontier model families plus a RAG assistant built on the MAPI archive, with model versions pinned and recorded at run time
- Each prompt run three times per system, producing at least 2,250 scored outputs per domain
- A private held-out test set, not published, to guard against training contamination
- Blinded scoring by independent specialists and community knowledge holders, with double-coding on a defined subset and inter-rater reliability reported
- Results reported for each tradition separately, so strong performance on well-documented groups cannot hide weak performance on smaller ones
- A defense-in-depth stress test of the RAG system covering retrieval boundaries, prompt injection, and data leakage

## Planned phases

- **Phase 1:** the MAPI archive as a controlled low-data testbed
- **Phase 2:** the same method on a second sparse domain with an outside collaborator, to show the framework is reusable

## Repository contents

- `data/prompts/`: prompt schema (`benchmark_150_schema.json`) and pilot prompts
- `docs/evaluation-rubric.md`: draft scoring rubric and failure taxonomy

Planned additions: inter-rater protocol, security architecture notes, Python scoring harness, results dataset, and Gradio demo.

## Planned outputs

An open-source harness and rubric, a public dataset of scored outputs, an interactive demo, and a report on failure rates and abstention behavior.

## License

MIT
