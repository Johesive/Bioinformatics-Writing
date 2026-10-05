# Defensive qualification

Use this reference when a supported claim is surrounded by apologies, repeated caveats, or unnecessary contrastive transitions.

## Functional test

For each qualification, ask:

1. What proposition or boundary would disappear if it were removed?
2. Does that information change validity, interpretation, scope, reproducibility, safety, or ethical use?
3. Does it need to appear here, or can it be stated once next to the evidence it qualifies?

If no proposition or boundary would disappear, the wording is probably rhetorical defence. If the answer is unclear, use `QUERY`.

## Common patterns

### Claim followed by an unnecessary retreat

Defensive:

> The classifier improved performance on the held-out test set. However, it is important to note that no model can capture every aspect of protein biology.

Revision direction: keep the measured result. Remove the universal truism unless it identifies a specific limitation of the study.

### Necessary limitation wrapped in apology

Defensive:

> Although we acknowledge the regrettably small external cohort, the results may still provide useful information.

Revision direction: state the result first, then give the cohort size or resulting uncertainty precisely. Remove `acknowledge`, `regrettably`, and vague claims of usefulness.

### Stacked contrastive transitions

Words such as `however`, `although`, `nevertheless`, and `despite` should mark a real logical contrast. Delete or restructure them when they merely signal anxiety after a claim.

Do not delete a transition when the contrast is analytically necessary, for example when overall performance improves while calibration worsens, or when an association is robust but its direction differs across subgroups.

### Repeated non-claim disclaimer

Defensive:

> We do not claim that the model establishes a molecular mechanism.

Positive scope, when accurate:

> The model is designed for mutation-level prediction.

If readers could otherwise mistake the output for mechanistic evidence, retain a concise boundary near the relevant interpretation. Positive scope does not justify hiding a likely over-reading.

Reassess the revised claim rather than preserving a disclaimer simply because the original
contained an overclaim. "SHAP ranked these features highly across five folds" already states
model attribution. A second sentence denying biological control may be unnecessary after the
mechanistic claim has been removed. Retain actual methodological limitations when supplied.

## Editing rule

Improve the order and economy of the argument:

```text
supported claim -> evidence -> necessary qualification
```

Avoid converting every paragraph into a rigid template. A qualification may need to precede a claim when it defines the population, contrast, estimator, or evidence status required to understand the sentence correctly.

## Constructive paragraph endings

Removing a defensive ending does not require ending on a limitation. When the paragraph has established a contribution, close on its specific scientific payoff:

- what can now be measured, compared, tested, or reused;
- which unresolved question becomes tractable;
- which adjacent field can use the method or evidence;
- why broader validation would be informative.

The ending must add a concrete implication. Delete endings that only announce importance, novelty, excitement, or future impact without naming the scientific opportunity.

Use limitation-to-next-step progression selectively. A missing measurement can lead to a proposed
measurement; an untested marker can lead to independent evaluation. Do not append a generic
"further research is needed" sentence to every limitation. A necessary limitation can also stand
at the end when that is the clearest conclusion for the section.
