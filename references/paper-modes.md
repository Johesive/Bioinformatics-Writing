# Paper modes

Use this reference to decide what should organise the prose. The mode controls rhetorical
priority; it never changes the evidence ceiling.

## Classify the governing contribution

### `BIOLOGY_DRIVEN`

Choose this mode when the study's main contribution is a biological finding, relationship,
hypothesis, explanation, or application. Computational analysis is the evidential machinery.

Common signals:

- the title or research question names a biological phenomenon;
- the main figures are organised around biological comparisons or phenotypes;
- the computational method is established, adapted, or secondary to the biological question;
- success is judged by what is learned about the biological system.

Narrative spine:

```text
biological question -> computational evidence -> calibrated biological interpretation
```

Lead paragraphs with the biological question or finding. Introduce model behaviour, metrics,
and robustness where they determine confidence in that finding. End with the biological
question made testable, the experimental validation enabled, or the bounded insight obtained.

Keep biological subjects and comparisons visible without packing all cohort, assay, and analysis
details into the opening sentence. A short study-context sentence can precede the finding when
it makes the paragraph easier to follow. Connect each result to the question it answers, and
place computational evaluation in a supporting sentence. Predictive accuracy cannot validate a
biological association or lineage transition; those require their own evidence.

### `METHOD_DRIVEN`

Choose this mode when the main contribution is an algorithm, representation, benchmark,
dataset, software system, evaluation design, or analytical capability. Biological tasks
establish relevance and expose the conditions under which the contribution works.

Common signals:

- the study begins from a computational or measurement limitation;
- novelty resides in the method, resource, or evaluation protocol;
- main comparisons concern baselines, ablations, generalisation, efficiency, or robustness;
- success is judged by a new capability rather than a particular biological discovery.

Narrative spine:

```text
computational limitation -> delivered method or resource -> validated biological capability
```

Lead paragraphs with the limitation or capability relevant to the local claim. Report the
evaluation design precisely. End with the biological analyses, comparisons, or experiments
that the contribution now makes feasible. Do not manufacture a biological discovery to make a
method paper sound important.

### `MIXED_OR_UNCLEAR`

Use this mode when biology and method make co-primary contributions, or when a supplied passage
does not reveal the manuscript's governing contribution. Do not infer the mode from isolated
technical vocabulary.

For a narrow passage, identify its local function and preserve both plausible framings. Mark
`AUTHOR_INPUT_NEEDED` only when choosing a mode would materially change emphasis, paragraph
order, title, abstract, or significance claim.

## Section-level emphasis

| Section | Biology-driven emphasis | Method-driven emphasis |
|---|---|---|
| Introduction | Biological problem and unresolved knowledge | Computational limitation and why it blocks biological work |
| Methods | Reproducible analysis tied to the biological question | Formal method definition, assumptions, implementation, and reproducibility |
| Results | Biological claim supported by computational evidence | Capability claim supported by benchmarks, ablations, and biological tasks |
| Discussion | Biological interpretation and experimental next step | Scope of the capability, failure conditions, and enabled biological questions |
| Conclusion | Bounded biological contribution | Bounded methodological contribution and the work it enables |

The table sets emphasis, not permission to omit evidence. A biology-driven Results section still
needs split design, uncertainty, baselines, calibration, and robustness when they govern the
claim. A method-driven paper still needs biologically meaningful evaluation and must distinguish
benchmark improvement from biological insight.

## Methods standard in both modes

When the relevant information is present, preserve or clarify:

- data provenance, inclusion criteria, preprocessing, labels, and missing-data handling;
- unit of splitting and related entities crossing partitions;
- model inputs, outputs, architecture or algorithm, optimisation, and hyperparameter selection;
- baselines, ablations, evaluation metrics, uncertainty, repeated runs, and statistical tests;
- software versions, random seeds, code, data, and reproducibility constraints;
- the biological or inferential reason for every major design choice.

Do not invent missing methodological detail. Flag information needed for reproducibility as
`AUTHOR_INPUT_NEEDED` when its absence affects the requested revision.

## Mode-specific significance test

Before writing a positive ending, ask:

- `BIOLOGY_DRIVEN`: What biological relationship, hypothesis, experiment, or interpretation
  becomes clearer or testable?
- `METHOD_DRIVEN`: What analysis, comparison, generalisation test, or biological investigation
  becomes possible because the method or resource now exists?

If neither question has an answer in the supplied evidence, omit the significance sentence.
