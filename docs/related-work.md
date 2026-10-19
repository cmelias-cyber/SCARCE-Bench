# Related Work and Background Reading

Draft notes. These are reading notes, not claims. SCARCE-Bench does not depend on any forecast about future AI.

## Benchmarks on factual accuracy and abstention

- SimpleQA and AbstentionBench test factual accuracy and abstention on general-knowledge questions. SCARCE-Bench differs by focusing on sparse, expert-curated domains, using reference notes written with specialists, and reporting results for each tradition separately.

## Why scale changes failure modes

- Steinhardt, "Future ML Systems Will Be Qualitatively Different" (2022). New behaviors and failure modes can appear as systems scale, and are not simple extensions of past trends. For this project, calibration and abstention behavior may change between model versions, so SCARCE-Bench pins versions and keeps the harness rerunnable to track change over time.

## Why verification matters as AI does more AI work

- Anthropic Institute essay on recursive self-improvement (2026). As AI systems write and review more work, human verification becomes a bottleneck and oversight grows more important. For this project, automated judging is tempting, but in sparse domains an AI judge may share the blind spots of the system it grades. SCARCE-Bench uses human specialist scoring with double-coding. Testing where automated judges and specialists disagree is a possible later extension.
