# Chiron

An adaptive tutoring skill for Claude. Chiron diagnoses what a learner already
knows, teaches one concept at a time, checks understanding, classifies errors,
and adapts the path — all driven by a **learner model** it builds at the start
and updates after every exchange.

## What it does

- **Diagnose** — asks about the goal and prior knowledge, then probes for
  misconceptions before teaching anything.
- **Anchor** — learns what the learner already knows well, to build analogies
  that fit.
- **Core loop, per concept** — Instruct → Question → Practice → Retrieve →
  Analyze errors (slip / missing prerequisite / misconception / honest gap) →
  Decide.
- **Space and Reflect** — resurfaces earlier concepts on a spaced schedule and
  compares the learner's confidence to their actual results.
- **Quiz and Transfer** — a cumulative mixed-format quiz, then a novel,
  unscaffolded problem shaped like the learner's real task.
- **Persistence** — ends each session by outputting the learner model as a
  block the learner can paste back next time.

## Triggers

Chiron activates when someone wants to learn and retain a topic: "teach me X",
"help me understand Y", "quiz me on Z", "I want to get good at W", or when they
paste a learner model from an earlier session. It is not meant for one-off
factual questions.

## Install

### Claude Code

Copy the `chiron` folder into your skills directory:

```bash
git clone https://github.com/pdelsignore/Chiran.git
cp -R Chiran/chiron ~/.claude/skills/
```

For a single project, copy it into that project's `.claude/skills/` instead.

### Claude.ai

Zip the `chiron` folder and upload it under **Settings → Capabilities →
Skills**.

## Structure

```
chiron/
└── SKILL.md   # the skill: frontmatter (name, description) + instructions
```

## License

MIT — see [LICENSE](LICENSE).
