# SCARCE-Bench

**SCARCE-Bench** (*Sparse-knowledge Certainty, Abstention, RAG, and Conflation Errors Benchmark*) is an open-source evaluation framework designed to audit how frontier language models and Retrieval-Augmented Generation (RAG) systems behave in evidence-sparse and high-ambiguity knowledge domains.

Using the curated digital archive of the Mesopotamian Aroma Preservation Initiative (MAPI) as a controlled evaluation sandbox, SCARCE-Bench stress-tests model outputs for unearned confidence, source conflation, and epistemic failures.

---

## Key Features & Scope
* **Target Failure Modes:** Source Conflation & Epistemic Flattening, False Certainty & Calibration Failures.
* **Evaluated Systems:** 4 Frontier LLM Families (OpenAI GPT-4, Anthropic Claude, Google Gemini, Meta Llama flagship runtimes) + Pinecone/AWS Bedrock RAG Control Baseline.
* **Sample Size:** 150 curated edge-case prompts × 15 evaluations/variations = **2,250 logged evaluation outputs**.
* **Methodology:** Blinded dual-annotation paired with expert archivist double-coding to compute inter-rater reliability ($Krippendorff's \alpha$).

---

## Project Deliverables
1. **GitHub Benchmark Repository:** Python evaluation harnesses, test suites, and scoring protocols.
2. **Open Output Dataset:** 2,250 logged model completions hosted on Hugging Face.
3. **Interactive Gradio Demo:** Web interface hosted on Hugging Face Spaces for interactive error exploration.
4. **Empirical Evaluation Report:** Publication-grade report detailing model failure rates and boundary enforcement mechanisms.

---

## Repository Structure
For detailed technical specifications, rubric taxonomies, and budget breakdowns, see the [`docs/`](./docs/) directory.

* [`docs/proposal-spec.md`](./docs/proposal-spec.md): Full project specification, budget allocation, and execution timeline.
* [`docs/evaluation-rubric.md`](./docs/evaluation-rubric.md): Scoring rubric (0–2 scale) and failure taxonomy definitions.
* [`docs/inter-rater-protocol.md`](./docs/inter-rater-protocol.md): Expert double-coding protocol and inter-rater reliability targets.
