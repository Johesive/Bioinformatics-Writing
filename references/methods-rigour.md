# Methods rigour

Use this reference when revising Methods or when a Results claim depends on computational design.
Improve readability without making an incomplete method appear complete.

Match audit depth to the request. For a local paragraph edit, flag gaps that change its meaning
or prevent completion, with a short list of the information required. Do not automatically expand
the response into a review of the entire study. For a requested Methods audit, use the broader
questions below. Keep missing-information labels in author notes; use explicit placeholders in
unfinished manuscript text rather than sentences describing what "the draft does not specify".

## Preserve the computational chain

Trace the analysis in the order needed to reproduce and interpret it:

```text
biological unit and data provenance
-> preprocessing and label construction
-> partitioning and leakage control
-> model or statistical procedure
-> tuning and model selection
-> evaluation and uncertainty
-> reproducibility artefacts
```

Each major choice should state what was done and, when relevant, the biological or inferential
reason. Avoid decorative justification. A protein-level split, for example, matters because it
tests transfer to proteins absent from training; calling it "more rigorous" conveys less.

## Missing-information severity

Classify missing detail by its effect on interpretation.

- `BLOCKING`: Without it, the analysis cannot be reproduced or the central claim cannot be
  interpreted. Examples include the split unit, outcome definition, test-set reuse, primary
  metric, or statistical unit. Preserve the gap and request author input before presenting the
  passage as complete.
- `MATERIAL`: The main analysis remains interpretable, but reliability, transportability, or
  comparison is uncertain. Examples include hyperparameter selection, random seeds, software
  versions, calibration assessment, or handling of missing values. Flag the omission and avoid
  claims that depend on it.
- `REPORTING`: The detail improves implementation clarity without changing the present claim.
  Examples may include hardware or secondary defaults when they do not affect reproducibility.
  Tighten the prose and request the detail only when the venue or reproducibility standard needs it.

Severity depends on the claim. Random seeds can be material for an unstable neural model and
less consequential for a deterministic analysis.

## Section-specific revision

### Introduction

Name the biological problem or computational bottleneck before the proposed solution. End the
gap paragraph with the unresolved capability, not generic importance.

### Methods

Use operational language and explicit referents. Preserve units, denominators, data partitions,
selection rules, thresholds, software, and uncertainty procedures. Keep chronology only when it
helps reproduction; organise by analytical dependency when pipeline order alone obscures why a
step exists.

### Results

Separate the claim from the evidence supporting it. For biology-driven work, lead with the
biological comparison and then establish computational reliability. For method-driven work,
lead with the capability or limitation resolved and then show performance on biologically
meaningful tasks. Report unfavourable metrics and robustness failures where they alter the claim.

### Discussion

Move from established result to interpretation to next test. State computational boundaries
where they constrain biological meaning. Do not repeat the Methods or turn every limitation into
a final sentence.

### Abstract and title

Make the governing contribution visible. A biology-driven title should foreground the biological
finding unless the method itself is co-primary. A method-driven title or abstract may foreground
the method, but its significance must name the biological capability evaluated or enabled.

## Methods audit questions

Ask only questions relevant to the supplied analysis:

1. What is the independent biological or statistical unit?
2. How were labels or outcomes obtained, and are they measured, curated, or predicted?
3. What entities may be related across partitions?
4. Was the test set used for tuning, threshold selection, or repeated decision-making?
5. Which metric answers the stated task under the observed prevalence and costs?
6. How were variability and uncertainty estimated?
7. Which preprocessing steps were learned using training data only?
8. What information is needed to reproduce the reported result?

Do not invent answers. Use `AUTHOR_INPUT_NEEDED` for blocking or material omissions that affect
the requested prose.
