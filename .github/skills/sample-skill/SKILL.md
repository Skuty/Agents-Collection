---
name: sample-skill
description: >
  A concise, trigger-oriented description of what this skill does and when the
  agent should invoke it. Use action verbs and name the domain clearly.
  Example: "Explain, refactor, or document Python code. Use when the user asks
  to clean up, simplify, or add docstrings to Python functions."
argument-hint: 'the thing to operate on — e.g., a file path, function name, or short description'
---

<!--
  SKILL TEMPLATE — replace every section marked [TODO] with your own content.

  File layout:
    SKILL.md            ← you are here (required)
    assets/             ← reusable templates / boilerplate the skill may copy (optional)
    references/         ← deep-dive reference docs the skill may read (optional)

  How skills are invoked:
    The agent reads this file at runtime to know what to do.
    Keep instructions concrete and imperative ("do X", "check Y").
    Avoid vague guidance ("consider doing X") — the agent should not have to guess.
-->

# [TODO: Skill Display Name]

> **One-sentence summary.** [TODO: What does this skill produce and for whom?]

---

## When to Use

Use this skill when the user says something like:

- "[TODO: trigger phrase 1]"
- "[TODO: trigger phrase 2]"
- "[TODO: trigger phrase 3 — include synonyms and intent variants]"

Do **not** use this skill when:

- "[TODO: out-of-scope scenario 1]"
- "[TODO: out-of-scope scenario 2]"

---

## Inputs

| Input | Source | Notes |
|-------|--------|-------|
| [TODO: input 1] | [argument / file read / user message] | [TODO: description] |
| [TODO: input 2] | [argument / file read / user message] | [TODO: description] |

---

## Procedure

Follow these steps in order. Do not skip steps unless the condition in the step itself says it is optional.

### Step 1 — [TODO: Gather context]

- [TODO: specific action — read a file, run a command, parse a config, etc.]
- [TODO: what to look for]
- If [TODO: condition], skip to Step 3.

### Step 2 — [TODO: Plan / analyse]

- [TODO: what analysis or design decisions to make before writing output]
- Consider: [TODO: list of factors that should influence the output]

### Step 3 — [TODO: Produce output]

- [TODO: concrete instruction for generating the primary deliverable]
- Follow the conventions in [assets/template.md](./assets/template.md) if it exists.
- [TODO: any naming, formatting, or placement rules]

### Step 4 — [TODO: Validate]

- [TODO: how to verify the output is correct — run a command, re-read the file, etc.]
- If validation fails: [TODO: remediation action]

---

## Output Specification

[TODO: describe exactly what the skill produces]

```
[TODO: example output — code block, table, markdown snippet, etc.]
```

- **Location:** [TODO: where the output goes — file path pattern, stdout, inline edit]
- **Format:** [TODO: language, schema, or structure the output must follow]

---

## Conventions and Rules

- [TODO: rule 1 — e.g., "never overwrite existing files without user confirmation"]
- [TODO: rule 2 — e.g., "always preserve existing code style"]
- [TODO: rule 3 — e.g., "add a TODO comment wherever a value must be filled in by the user"]

---

## Supporting Files (optional)

| File | Purpose |
|------|---------|
| [assets/template.md](./assets/template.md) | Boilerplate to copy when creating output from scratch |
| [references/deep-dive.md](./references/deep-dive.md) | Extended reference material the agent may read for edge cases |

> Remove this section if the skill has no supporting files.

---

## Quick Example

[TODO: a short, self-contained example showing a representative input and the expected output]

**Input:**

```
[TODO: example user request or input value]
```

**Output:**

```
[TODO: example output the skill produces]
```
