---
name: bioinfo-writing
description: Revise bioinformatics, computational biology, and biomedical data-science manuscripts while preserving the exact strength, scope, and status of the evidence. Use when prose overstates association as causation, buries a supported claim under defensive qualifications, stacks hedges or contrastive transitions, needs a claim-preserving clarity pass, or needs an evidence-bounded closing sentence that explains why the work matters and what research it enables. Do not use for new analysis, fact-checking, citation discovery, medical advice, or grammar-only editing.
license: MIT
---

# Bioinfo Writing

Make the supported claim easy to see without making it stronger. Preserve the scientific meaning of the source text, including uncertainty that changes how a result must be interpreted.

## Establish the editing contract

Before revising, identify from the supplied text:

- the manuscript mode: `BIOLOGY_DRIVEN`, `METHOD_DRIVEN`, or `MIXED_OR_UNCLEAR`;
- the main claim;
- its evidence type: computational prediction, association, experiment, mechanism, validation, or application;
- its population, dataset, organism, protein family, assay, and evaluation scope;
- qualifications that are necessary to interpret the claim;
- any missing information that prevents safe calibration.

If the intended claim or evidence status is ambiguous, keep the narrower defensible reading and mark `AUTHOR_INPUT_NEEDED`. Never resolve scientific ambiguity by making the sentence sound more certain.

Read [references/paper-modes.md](references/paper-modes.md) before revising a complete
paragraph, section, abstract, or title. Use the biological question as the narrative spine in
`BIOLOGY_DRIVEN` work. Use the computational limitation and delivered capability as the spine
in `METHOD_DRIVEN` work. In both modes, connect computational choices to the biological or
inferential question they serve.

For Methods prose or any passage whose claim depends on implementation, evaluation design, or
reproducibility, also read [references/methods-rigour.md](references/methods-rigour.md). Do not
smooth over a missing design choice that changes what the analysis can establish.

## Preserve the claim ceiling

A revision may keep or narrow a claim. It must not increase certainty, causality, mechanistic interpretation, novelty, generalisability, biological or clinical relevance, or validation status.

Never introduce a fact, number, method, dataset, experiment, citation, mechanism, or application absent from the supplied material.

Calibrate the claim in its affirmative wording first: describe an association, an inferred
trajectory, or model attribution at the appropriate level. After removing an unsupported causal
claim, reassess whether a separate "does not establish causality" sentence still adds necessary
information. The original overclaim alone does not require a permanent disclaimer in the revision.
Keep concrete facts such as unmeasured trafficking, missing lineage tracing, or unevaluated
calibration in the manuscript when they govern interpretation. An author note may explain the
editing decision, but must not become the sole location of a necessary methodological disclosure.

Retaining "suggests" does not automatically preserve the strength of an embedded proposition.
Check the whole claim when simplifying "suggests that X may be meaningful". Stability after
adjustment alone does not establish biological importance. Likewise, "potential" must not turn
an inferred cell-state ordering into evidence of lineage continuity.

Read [references/claim-calibration.md](references/claim-calibration.md) whenever the passage connects variables, explains a biological mechanism, interprets model features, or moves from computational results toward experimental or clinical meaning.

## Diagnose rhetorical defensiveness

Treat a qualification according to its function in context, not according to cue words such as `may`, `however`, or `although`.

Classify each candidate as:

- `KEEP`: required evidence, scope, statistical, methodological, ethical, or reproducibility boundary;
- `TIGHTEN`: necessary information expressed redundantly;
- `REFRAME`: a valid proposition organised as apology or self-defence;
- `RELOCATE`: a necessary limitation placed where it obscures the claim it qualifies;
- `CUT`: rhetoric whose removal loses no proposition or boundary;
- `QUERY`: meaning depends on an author decision or unavailable evidence.

Read [references/defensive-qualification.md](references/defensive-qualification.md) when a claim is followed by repeated concessions, contrastive transitions, imagined-reviewer objections, or self-undermining commentary.

## Revise

1. Lead with the strongest claim already supported by the text.
2. Place evidence immediately after the claim when available.
3. State each necessary boundary once, close to the claim it changes.
4. Remove apologies, repeated disclaimers, instructions telling readers how not to interpret an unmade claim, and stacked transitions that add no logical relation.
5. Prefer positive scope: state what was studied, evaluated, or observed.
6. Preserve negative findings, failed validation, non-significant results, trade-offs, alternative explanations, and known failure conditions when they affect the conclusion.
7. Do not conceal an unfavourable result by changing the endpoint, comparator, subgroup, metric, or narrative after seeing the result.
8. Keep sentence openings easy to process. Combine closely related result and uncertainty
   statements when this improves their logical connection; split a sentence when several
   qualifications obscure its main clause. Avoid reporting a comparison and then restating
   the same observation in an appended "indicating an association" clause. Make the evidence
   status clear once. Judge reading burden by repetition and clause structure, without imposing
   a fixed sentence-length limit or one sentence per rhetorical function.
9. Preserve paragraph-level progression after splitting sentences. Use precise anaphora or a
   lexical chain so that each sentence develops the previous one; do not replace syntactic
   overload with a sequence of disconnected statements or stacked transition words.
   For example, "This association" can carry a reported relationship into its interpretation
   or boundary when the referent is unambiguous. Keep the connection explicit where helpful,
   without repeating the whole finding or adding a connector to every sentence.

Use section purpose to decide whether an outlook is needed. Do not append the same scope phrase,
causal disclaimer, or future experiment to every paragraph. A Results paragraph may end with its
finding. Match each limitation to the inference it actually constrains; independent replication,
measurement provenance, and causal identification answer different questions.

## Close with warranted significance

When the section or paragraph establishes a supported contribution, it may end by explaining why that contribution matters. A constructive closing sentence can:

- name the research question, capability, dataset, method, or connection the work makes available;
- identify a plausible next investigation enabled by the result;
- connect the finding to an adjacent field when the connection follows from the demonstrated method or evidence;
- invite broader testing, validation, reuse, or interdisciplinary attention;
- state a field-level opportunity at the same evidential level as the preceding paragraph.

Keep three levels distinct:

1. `ESTABLISHED`: what the present study demonstrates within its scope;
2. `ENABLED`: what the contribution now makes feasible or testable;
3. `POSSIBLE`: a future direction or cross-field implication that remains hypothetical.

Use verbs that expose the level: `provides`, `enables`, and `offers a framework` require a concrete resource or capability already delivered; `creates an opportunity to test`, `may support`, and `could inform` mark a bounded future possibility.

Do not claim that the work opens a new field, transforms a discipline, has broad clinical impact, or will attract researchers unless evidence external to the prose supports that claim. Translate “blue ocean” language into a specific open problem, underexplored application, reusable capability, or testable research programme.

A closing sentence must grow from the paragraph's evidence. Omit it when it would merely repeat generic importance language.

In Discussion, when a limitation identifies a specific unresolved question, consider ending with
a practical way to investigate it. For example, unmeasured metabolites can motivate metabolite
measurement; establishing a causal role requires additional causal evidence. Present the step
as proposed work, never as something already performed or guaranteed to resolve the question.
Avoid vague self-evaluations such as "broader relevance remains uncertain" when the specific
untested population, mechanism, or application can be named. Results may end on the finding or
its necessary boundary without an outlook.

## Bioinformatics and biomedical ML guardrails

Keep any statement needed to disclose or interpret:

- the unit of data splitting, including patient-, sample-, gene-, protein-, family-, or mutation-level separation;
- homologous or related entities crossing data partitions;
- train, validation, test, external-validation, or prospective-validation status;
- class imbalance, prevalence, threshold selection, calibration, uncertainty, or distribution shift;
- confounding, batch effects, missing data, label provenance, multiple testing, or nested observations;
- the distinction between feature importance and biological mechanism;
- the distinction between in-silico prediction and experimental observation;
- the distinction between benchmark performance and biological or clinical utility.

When the supplied text exposes a possible integrity problem, flag it separately. Do not repair a study-design problem through wording.

## Output

For a revision request, lead with the revised prose. Add a brief author note only for a material
change in interpretation, a substantive ambiguity, or information needed to complete the passage.
Perform paper-mode classification, claim checking, and boundary checking internally; show these
checks when the user requests an explanation or audit. Follow any requested output format.
For incomplete Methods, mark specific missing details with clear placeholders and identify the
passage as incomplete. Keep comments about the draft out of manuscript prose.

For an audit-only request, do not rewrite. Return the candidate wording, its function, disposition, scientific risk, and recommended action.

## Final checks

Before delivery, verify:

- every factual element in the revision traces to the supplied text;
- association has not become causation;
- prediction has not become mechanism or observation;
- internal evaluation has not become external generalisation or clinical utility;
- no necessary limitation or negative result disappeared;
- deleted transition words did not erase a real logical contrast;
- the revised passage sounds direct without becoming promotional.
- any positive closing sentence distinguishes established contribution, enabled work, and possible future impact.

## Optional integration

This skill is self-contained. If other skills are installed, use them only for their own layer:

- run a statistics-reporting skill before this one when sample units, tests, uncertainty, or multiple comparisons are unsettled;
- run a claim-source verification skill when cited sources must be checked against individual claims;
- run a general prose or humanisation skill after this one, while treating the claim check and preserved boundaries as locked.

External skills may add constraints. They must not weaken this skill's claim ceiling.
