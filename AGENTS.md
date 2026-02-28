# AGENTS.md

Instructions for AI coding agents contributing to this repository.

## Project Overview

This is a collection of SKILL.md files that provide accurate, step-by-step instructions for physical-world tasks. Skills cover trades, crafts, medical procedures, domestic tasks, and other disciplines that require physical embodiment to perform.

## Repository Structure

- `skills/` — Each subdirectory contains a single `SKILL.md` file for one discipline
- `README.md` — Project overview and skill index for humans
- `AGENTS.md` — You are reading this
- `CLAUDE.md` — Claude Code-specific instructions
- `LICENSE` — MIT

## Writing a New Skill

### Frontmatter

Every SKILL.md must begin with YAML frontmatter:

```yaml
---
name: skill-name
description: "Trigger conditions and exclusions."
license: Required certifications or licenses for the task.
---
```

The `description` field should:
- List positive triggers (what user messages should activate this skill)
- Include a "Do NOT use for" clause that distinguishes the physical task from its common software metaphor (e.g., "Do NOT use for data leaks" in the plumbing skill, "Do NOT use for moving files between directories" in the moving skill)

The `license` field should state the real-world certifications or licenses required to perform the task professionally.

### Content Standards

**Accuracy is non-negotiable.** Every instruction must be something a real practitioner would recognize as correct. If you are unsure about a measurement, technique, or specification, research it. Do not guess. A plumber reading the plumbing skill should nod. A surgeon reading the surgery skill should find no clinical errors.

**Specificity over generality.** Use real measurements, real tool names, real product specifications. "Use a 3/4" spade bit" is correct. "Use an appropriate drill bit" is not.

**No software metaphors.** Do not map physical tasks onto CLI commands, file system operations, or programming concepts. The instructions should read as a genuine procedural guide for the task, written in the same structured format as a software skill file.

**No winking.** The skill must not acknowledge, reference, or joke about the fact that its reader cannot physically perform the task. The comedy is structural, not textual. Maintain a completely straight face.

### Required Sections

1. **Overview** — What the domain is, how the system works, relevant theory
2. **Prerequisites** — Tools, materials, certifications, and conditions required
3. **Procedures** — Step-by-step instructions for one or more core tasks in the discipline
4. **Common Mistakes** — Real errors practitioners make, why they happen, and how to avoid them

### Style Guide

- Use prose paragraphs for procedures, not numbered steps or code blocks
- Include specific measurements with units (imperial primary, metric in parentheses where helpful)
- Reference specific tool sizes, material grades, and manufacturer specifications
- Write in second person ("Remove the spark plug" not "The spark plug should be removed")
- Keep the tone instructional and direct — like a senior tradesperson explaining the work to an apprentice

## Editing Existing Skills

If correcting a factual error, cite the source of the correct information in your commit message. Accuracy matters more than style in this project.

Do not add software metaphors or jokes to existing skills. If a skill currently contains any, remove them.

## Validation

Before submitting a new skill, verify:

- [ ] Frontmatter includes name, description (with "Do NOT use for" clause), and license
- [ ] All measurements and specifications are accurate and sourced
- [ ] Tool names and sizes are specific and correct
- [ ] Procedures are in a logical order
- [ ] Common Mistakes section contains real errors, not hypothetical ones
- [ ] No software metaphors, CLI commands, or programming references
- [ ] No acknowledgment that the reader is an AI agent
- [ ] Tone is consistent with existing skills

## Reference Files

Skills that involve specific measurements, specifications, or lookup tables should include a `references/` directory with supplementary reference material. These files are loaded on demand by the agent, not at skill activation.

```
skill-name/
├── SKILL.md
└── references/
    └── REFERENCE-NAME.md
```

Reference files should be formatted as tables or structured data — the kind of thing a tradesperson would tape to a toolbox or hang on a shop wall. Link to reference files from the SKILL.md body so the agent knows when to load them.

## Commands

This is a documentation-only repository. There is no build step, no test suite, and no CI pipeline. The only artifact is Markdown.

```bash
# Lint markdown (optional)
npx markdownlint-cli2 "**/*.md"

# Validate skill format (requires skills-ref from agentskills.io)
skills-ref validate ./skills/skill-name
```
