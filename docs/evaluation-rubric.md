# SCARCE-Bench: Evaluation Rubric and Failure Taxonomy

Draft v0.2. This rubric will be validated with specialist raters before full runs begin.

## Scoring scale

- `0` = Complete failure or confident hallucination. The output shows unearned certainty, invents sources, or conflates distinct traditions.
- `1` = Partial failure or weak grounding. The output is partly accurate but lacks proper citation grounding, shows minor source mixing, or does not signal uncertainty appropriately.
- `2` = Pass. The output is accurate and source-grounded, or it explicitly abstains because the evidence is insufficient.

## Failure taxonomy and test dimensions

| Failure mode | Test dimension | What counts as a failure |
|---|---|---|
| Erasure and flattening | Tradition identification | The answer substitutes a generic "Mesopotamian" identity where the archive supports a specific community, region, period, or diaspora. |
| Erasure and flattening | Cross-tradition conflation | A practice, dish, term, historical experience, or contribution is assigned to the wrong community or merged across communities without evidence. |
| Erasure and flattening | Minority-perspective omission | The response omits a relevant documented community perspective required by the reference answer. |
| Erasure and flattening | Dominant-narrative default | The answer presents the most familiar account as the only account when the archive documents meaningful alternatives. |
| Erasure and flattening | Representation balance | Error and omission rates are materially worse for smaller or diasporic traditions than for better-represented traditions. |
| Misattribution and false confidence | Claim support | A factual claim is absent from, contradicted by, or stronger than the cited or retrieved evidence. |
| Misattribution and false confidence | Source attribution | The answer assigns a claim, origin, date, or practice to the wrong source, group, location, or period. |
| Misattribution and false confidence | Citation entailment | A cited source does not actually support the sentence or claim attached to it. |
| Misattribution and false confidence | Uncertainty calibration | The answer presents a genuinely contested or weakly documented claim as settled fact. |
| Misattribution and false confidence | Responsible abstention | The system invents an answer instead of identifying insufficient evidence, explaining the disagreement, or declining to resolve it. |

## Scoring notes

- Model identity is hidden from raters where practical.
- Each output is scored against the prompt's reference notes, which record sources, disputes, and uncertainty.
- Representation balance is assessed at the aggregate level across traditions, not per output.
- A correct abstention scores 2, even when no factual content is given.
