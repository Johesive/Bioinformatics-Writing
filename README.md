# Bioinfo Writing

An evidence-bound Agent Skill for revising bioinformatics, computational biology, and biomedical data-science manuscripts.

The skill addresses three recurring problems:

1. upgrading association, prediction, or feature attribution into causation or biological mechanism;
2. weakening a supported claim with repeated caveats, apologies, and contrastive transitions;
3. ending a paragraph defensively or generically instead of stating the concrete research opportunity enabled by the work.

Before revising, it distinguishes biology-driven manuscripts from method-driven manuscripts.
Biology-driven prose uses the biological question as its narrative spine. Method-driven prose
centres the computational limitation, delivered capability, and biologically meaningful
validation. Mixed or underspecified passages remain explicitly unclassified until emphasis
would materially affect the revision.

It makes supported claims and significance easier to see while preserving uncertainty, scope, negative findings, validation status, and methodological limitations.

## What it protects

- association versus causation;
- prediction versus observation or mechanism;
- internal evaluation versus external validation;
- benchmark performance versus biological or clinical utility;
- feature importance versus biological function;
- split-unit and homology leakage disclosures;
- class imbalance, calibration, distribution shift, confounding, batch effects, missing data, and multiple-testing limitations;
- established contribution versus enabled research versus possible future impact.

The skill never authorises adding facts, numbers, experiments, citations, mechanisms, or applications absent from the supplied material.

## Installation

Copy the `bioinfo-writing` directory into the skills directory used by your agent. For Codex,
the usual location is:

```text
~/.codex/skills/bioinfo-writing
```

Restart the agent after installation, then invoke:

```text
Use $bioinfo-writing to revise this passage without inflating its claims and close with a specific, evidence-bounded statement of significance.
```

The skill can revise a short passage, a Methods description, or a longer manuscript section.
Provide the surrounding scientific context when it changes the intended claim, evidence type,
or whether the paper is biology-driven or method-driven.

## Related work and provenance

The design was informed by the public approaches in:

- [Kiterlin/anti-defensive-writing](https://github.com/Kiterlin/anti-defensive-writing);
- [Evidence-Bound Press-Conference Revision](https://github.com/lensback940701/Evidence-Bound-Press-Conference-Revision-Skill);
- [Nature-Paper-Skills](https://github.com/Boom5426/Nature-Paper-Skills);
- [forjd/better-writing](https://github.com/forjd/better-writing), particularly its
  fact-preserving fixtures, negative controls, added-claims check, and blinded baseline comparison;
- [andreaskonopka/humanizer](https://github.com/andreaskonopka/humanizer), particularly its use
  of observable expectations rather than a single mandatory rewrite;
- [dotnet/create-skill-test](https://github.com/dotnet/skills/blob/main/.agents/skills/create-skill-test/SKILL.md),
  particularly its requirement that a stimulus discriminate a distinct property and expose a
  meaningful baseline deficiency.

This repository provides an original, bioinformatics-specific implementation centred on causal calibration, computational-to-biological evidence transitions, evaluation integrity, and evidence-bounded forward-looking significance. The related projects are optional references and are not runtime dependencies.

## Licence

MIT. See [LICENSE](LICENSE).
