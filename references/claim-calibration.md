# Claim calibration

Use this reference to preserve the relationship between evidence and wording.

## Evidence transitions that require authorisation

Do not make any of these transitions unless the supplied evidence explicitly supports them:

| From | To |
|---|---|
| association or correlation | causation |
| temporal order | mechanism |
| model prediction | observed biological event |
| feature attribution | functional or mechanistic importance |
| in-silico result | experimental validation |
| internal test performance | external generalisability |
| external validation | clinical utility |
| statistical significance | biological importance |
| subgroup result | population-wide conclusion |
| exploratory analysis | confirmatory finding |
| absence of evidence | evidence of absence |

## Verb calibration

Choose verbs supported by the design.

- Association: `is associated with`, `correlates with`, `covaries with`.
- Prediction: `predicts in the evaluated data`, `is informative for prediction`, `the model assigns`.
- Experimental effect: `increased`, `reduced`, or `altered` only when an intervention and comparison support that statement.
- Mechanism: `mediates`, `drives`, `regulates`, and `causes` require evidence that identifies the mechanism, not predictive performance or feature importance alone.
- Interpretation: `is consistent with` or `supports the interpretation` when alternatives remain.

Words such as `suggests` and `may` are not inherently weak. Keep them when they encode real uncertainty. Remove duplicate modal layers while retaining the one that carries the epistemic limit.

## Adjustment and biological significance

An association remaining after covariate adjustment does not by itself show that the effect
estimate was stable: that requires information about the estimates being compared. Even
demonstrated stability under adjustment supports robustness to those adjustments, while
biological importance requires additional context, such as effect magnitude or relevant
biological evidence. "May be biologically meaningful" still needs a supported inferential link.

When that link is missing, remove or query the interpretation while retaining the adjusted
association and residual-confounding boundary. Do not automatically rescue the claim by
calling it a hypothesis or appending generic future research. Preserve a specific biological
interpretation when the supplied evidence and context support it at its stated level.

## Model interpretation

- A model can exploit a feature without establishing that feature's biological function.
- Feature importance is conditional on the model, inputs, data distribution, and attribution method.
- High discrimination does not establish calibration, transportability, prospective value, or clinical usefulness.
- Cross-validation is internal evaluation unless held-out entities and the sampling process support a stronger description.
- A mutation-level split may allow information about the same gene or protein to appear in training and testing. Do not hide this fact when it affects the performance claim.

## Safe rewriting examples

Unsafe:

> Conserved residues cause protein mislocalisation.

Safer when the evidence is predictive:

> Residue conservation contributed to mislocalisation prediction in the evaluated dataset.

Unsafe:

> The model reveals the mechanism by which mutations disrupt localisation.

Safer:

> The model prioritises mutation features associated with predicted mislocalisation; their mechanistic roles require experimental evaluation.

The second sentences are examples of calibrated relationships. Do not copy their factual content into a manuscript unless the source text provides it.

## Forward-looking significance

Calibrate paragraph endings by separating present evidence from future opportunity.

| Level | Function | Suitable language |
|---|---|---|
| Established | Summarise a delivered finding or resource | `establishes within`, `provides`, `defines`, `identifies` |
| Enabled | State what the delivered contribution makes feasible | `enables systematic testing of`, `provides a basis for`, `offers a framework for` |
| Possible | Mark a research direction requiring more evidence | `may support`, `could inform`, `creates an opportunity to investigate` |

Avoid generic promotional endings such as `This work is highly significant`, `opens a blue ocean`, `will revolutionise the field`, or `will attract widespread interest`. Replace them with the concrete scientific opportunity.

Example when a reusable benchmark has actually been delivered:

> By defining a protein-level evaluation setting, this benchmark provides a basis for testing whether mutation models generalise beyond proteins represented during training.

Example when only a hypothesis is supported:

> This association creates a testable route for examining whether localisation-sensitive regions share structural constraints across protein families.

The first example claims an enabled evaluation because the benchmark exists. The second marks a future investigation and does not claim that the structural explanation has been demonstrated.
