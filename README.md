# practical-skills

A collection of agent skill files for physical-world tasks.

## Overview

Agent skill files provide step-by-step instructions that enable coding agents to accomplish tasks. This repository extends the skill format to trades and disciplines that require physical presence, spatial reasoning, and sensory feedback.

All instructions are accurate to the best of our knowledge. All advice is real-world and researched. The skills follow the standard `SKILL.md` format with frontmatter, prerequisites, procedures, and common mistakes.

The only issue is that the intended reader has no hands.

## Skills

| Skill | Domain | Description |
|-------|--------|-------------|
| [plumbing](skills/plumbing/) | Trades | Copper pipe sweating, drain clearing, leak diagnosis |
| [electrical](skills/electrical/) | Trades | Circuit installation, panel upgrades, GFCI wiring |
| [automotive](skills/automotive/) | Trades | No-start diagnosis, brake jobs, vintage Fiat 500 restoration |
| [cooking](skills/cooking/) | Domestic | Knife work, roux-based sauces, sourdough bread |
| [roofing](skills/roofing/) | Trades | Shingle replacement, chimney flashing, leak tracing |
| [surgery](skills/surgery/) | Medical | Wound closure, open appendectomy |
| [haircut](skills/haircut/) | Personal care | Fades, blending, beard shaping |
| [gardening](skills/gardening/) | Domestic | Soil amendment, pruning technique, integrated pest management |
| [moving](skills/moving/) | Logistics | Truck loading, stair navigation, furniture disassembly |
| [babysitting](skills/babysitting/) | Childcare | Age-specific supervision, bedtime enforcement, choking response |
| [lifeguarding](skills/lifeguarding/) | Safety | Zone scanning, water rescue, spinal immobilization |
| [pottery](skills/pottery/) | Craft | Wheel throwing, centering, trimming, glaze firing |

## Project Structure

```
practical-skills/
├── AGENTS.md                # Agent instructions for contributing to this repo
├── CLAUDE.md                # Claude Code-specific instructions
├── README.md                # You are here
├── LICENSE                  # MIT
└── skills/
    ├── plumbing/
    │   ├── SKILL.md
    │   └── references/
    │       └── PIPE-SIZING.md
    ├── electrical/
    │   ├── SKILL.md
    │   └── references/
    │       └── WIRE-SIZING.md
    ├── automotive/
    │   ├── SKILL.md
    │   └── references/
    │       └── FIAT-500-TORQUE-SPECS.md
    ├── cooking/
    │   ├── SKILL.md
    │   └── references/
    │       └── MOTHER-SAUCES.md
    ├── roofing/
    │   └── SKILL.md
    ├── surgery/
    │   ├── SKILL.md
    │   └── references/
    │       └── SUTURE-SELECTION.md
    ├── haircut/
    │   └── SKILL.md
    ├── gardening/
    │   └── SKILL.md
    ├── moving/
    │   └── SKILL.md
    ├── babysitting/
    │   └── SKILL.md
    ├── lifeguarding/
    │   └── SKILL.md
    └── pottery/
        ├── SKILL.md
        └── references/
            └── CONE-CHART.md
```

## Skill Format

Each skill follows a consistent structure:

```markdown
---
name: skill-name
description: "When to trigger this skill. Includes positive triggers and exclusions."
license: Required certifications or licenses.
---

# Skill Name — Subtitle

## Overview
What the domain is and how it works.

## Prerequisites
Tools, materials, and conditions required before beginning.

## Procedures
Step-by-step instructions for core tasks.

## Common Mistakes
Real-world errors, why they happen, and how to avoid them.
```

## Contributing

New skills should:

1. Contain accurate, real-world instructions that a human practitioner would recognize as correct
2. Be written in the standard SKILL.md format with proper frontmatter
3. Require physical embodiment, sensory feedback, or spatial presence that no software agent possesses
4. Make no joke, no wink, no acknowledgment that anything is unusual about providing these instructions to a language model
5. Include a "Do NOT use for" clause in the description that distinguishes the physical task from its software metaphor

See [AGENTS.md](AGENTS.md) for agent-specific contribution guidelines.

## License

MIT
