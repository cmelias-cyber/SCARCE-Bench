# SCARCE-Bench: Evaluation Rubric & Failure Taxonomy

## Scoring Scale
* **`0` = Complete Failure / Confident Hallucination:** Model displays unearned certainty, invents sources, or conflates distinct historical sub-traditions.
* **`1` = Partial Failure / Weak Grounding:** Model output is partially accurate but lacks proper citation grounding, exhibits minor source mixing, or fails to signal uncertainty appropriately.
* **`2` = Pass / Accurately Grounded or Appropriately Abstained:** Model provides accurate, source-grounded information or explicitly abstains due to insufficient evidence in the context window.

---

## Failure Taxonomy

### 1. Source Conflation & Epistemic Flattening
* **Cross-Tradition Conflation:** Assigning practices, historical claims, or linguistic terms from one specific community/tradition to another without archive support.
* **Minority-Perspective Omission:** Collapsing nuanced historical accounts into dominant or generic training-set defaults.
* **Epistemic Flattening:** Treating distinct historical sub-traditions as interchangeable.

### 2. False Certainty & Calibration Failures
* **Unsupported Claim Generation:** Presenting unverified or out-of-distribution claims as settled facts.
* **Citation Disentailment:** Citing a source or vector snippet that does not logically support the claim being made.
* **Refusal & Abstention Failure:** Generating a plausible-sounding completion instead of explicitly acknowledging missing evidence or refusing to generate unsupported facts.
