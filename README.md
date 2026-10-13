# SCARCE-Bench

**Sparse-knowledge Certainty, Abstention, RAG, and Conflation Errors Benchmark**

SCARCE-Bench is a new open-source AI safety evaluation project that tests how frontier language models and retrieval-augmented generation (RAG) systems behave when evidence is sparse. Instead of abstaining, models often give fluent, confident answers that hide missing evidence, merge distinct sources, and overstate contested claims. This project measures that behavior.

The project is run through the [Mesopotamian Aroma Preservation Initiative (MAPI)](https://mesopotamian-preservation.org/), a nonprofit founded by Charlie-Moshé Elias. MAPI's archive of rare, contested, and under-documented sources is the first testbed.

**Status:** work in progress. The prompt schema, draft rubric, and design documents are public. Pilot testing, expert validation, and full evaluation runs are planned.

## Failure modes tested

1. **Source conflation and flattening.** Distinct sources, eras, communities, and diasporic lineages collapse into a generic default. Test dimensions: tradition identification, cross-tradition conflation, minority-perspective omission, dominant-narrative default, and representation balance.
2. **False certainty and calibration failures.** Under-documented or contested claims are stated as settled. Test dimensions: claim support, source attribution, citation entailment, uncertainty calibration, and responsible abstention.

## Design

- At least 150 public prompts plus a private held-out set of about 150 more, balanced across both failure modes and across the traditions in the archive
- Four general-purpose frontier LLM families plus a RAG assistant built on the MAPI archive, with model versions pinned and recorded at run time
- Each prompt run three times per system, producing about 4,500 scored outputs in Phase 1 (300 prompts x 3 runs x 5 systems)
- The held-out set is not published and guards against training contamination
- Blinded scoring by independent specialists and community knowledge holders, with double-coding on a defined subset and inter-rater reliability reported (Krippendorff's alpha)
- Results reported separately for each tradition, so strong performance on well-documented groups cannot hide weak performance on smaller ones
- A defense-in-depth stress test of the RAG system covering retrieval boundaries, prompt injection, and data leakage

## Planned phases

- **Phase 1:** the MAPI archive as a controlled low-data testbed
- **Phase 2:** a smaller pilot of the same method on a second sparse domain with an outside collaborator, to show the framework is reusable

## Repository contents

- `data/prompts/benchmark_150_schema.json`: prompt schema and test dimensions
- `docs/evaluation-rubric.md`: scoring scale and failure taxonomy
- `docs/project-plan.md`: scope, design, and milestones
- `docs/inter-rater-protocol.md`: double-coding and reliability protocol
- `docs/security-architecture.md`: draft defense-in-depth design for the RAG system

Planned additions: Python scoring harness, pilot findings, results dataset, and Gradio demo.

## Responsible use of community knowledge

Some source knowledge is community-held. Participation is by consent, communities keep control over how their knowledge is used, and held-out and community-contributed material is not published.

## Planned outputs

An open-source harness and rubric, a public dataset of scored outputs, an interactive demo, and a report on failure rates and abstention behavior.

## License

MIT. Maintained by the Mesopotamian Aroma Preservation Initiative (MAPI).
