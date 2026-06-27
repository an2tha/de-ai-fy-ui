# de-ai-fy

A small set of agent skills for making web interfaces feel less AI-generated and more intentionally designed.

This repo helps coding agents create websites with stronger art direction, better colour and copy choices, more useful inspiration research, and browser-based design previews before implementation. It also adds hard anti-template gates so generated options do not collapse into the same scaffold with different palettes.

## What This Is

`de-ai-fy` is a skill bundle for frontend/design agents. It teaches agents to avoid the common signs of generic AI UI:

- Purple-blue gradient SaaS templates
- Vague “supercharge your workflow” copy
- Random glass cards and glow effects
- Weak hierarchy and repetitive card grids
- Generic fonts, colours, and CTAs
- Inspiration copying instead of original art direction
- The same phone/browser shell, card stack, fake data, and rationale copy repeated across every option
- Dark patterns, clutter, and inaccessible UI

## Included Skills

### `skills/de-ai-fy/SKILL.md` — de-ai-fy

Main website-design skill. Covers:

- Human-designed art direction
- Colour choice rules
- Text/copy choice rules
- Typography, layout, spacing, motion, and component guidance
- Positive lessons from good web references
- Negative constraints from bad website examples
- Accessibility, responsiveness, and UX quality checks

Use when building or improving a website, landing page, dashboard, product UI, or component system.

### `skills/design-preview-skill/SKILL.md`

Preview workflow skill. Instructs the agent to:

- Lock the product context before generating previews
- Create `N` standalone HTML design previews
- Define a divergence contract so options differ in IA, flow, structure, interaction, and visual system — not just color
- Use coherent, product-specific mock data and realistic states
- Open them in the browser
- Let the user choose a preferred direction
- Generate surgical refinements like “modify the fonts” or “make 4 more iterations of option 2”
- Avoid implementing final production UI until a direction is approved

### `skills/inspirations-skill/SKILL.md`

Research and reference-selection skill. Instructs the agent to:

- Find good inspiration from direct, adjacent, product, brand, editorial, artifact, and negative references
- Distinguish useful inspiration from bad/generic inspiration
- Extract principles without copying assets, layouts, or brand systems
- Tie each reference to a visible design decision instead of citing references decoratively
- Align references with the main `de-ai-fy` standards
- Translate inspiration into original design directions

### `skills/design-output-audit-skill/SKILL.md`

Audit skill for generated previews or implemented UI. Instructs the agent to:

- Detect repeated scaffolds, fake data, formulaic copy, and decorative reference citations
- Compare options as a set, not just one-by-one
- Score product specificity, structural originality, data realism, interaction depth, and accessibility
- Reject or revise previews before showing them when they still look AI-generated

## Reference Files

### `good-websites.txt`

Curated positive references: award-winning sites, product UIs, brand systems, and inspiration directories.

Agents should study these for:

- Typography systems
- Colour systems
- Layout grammar
- Motion language
- Navigation structure
- Content density
- Distinctive human-designed moves

### `bad-examples.txt`

Negative references and anti-patterns: cluttered websites, dark patterns, legacy UI, bad mobile UX, intentionally bad UI examples, and deceptive design databases.

Agents should use these only to extract constraints — never to copy.

## Recommended Agent Workflow

1. Load `inspirations-skill` when research or references are needed.
2. Use `good-websites.txt` and `bad-examples.txt` to identify lessons and constraints.
3. Use the main `de-ai-fy` skill to define a distinct art direction.
4. Use `design-preview-skill` to generate browser previews when visual comparison would help.
5. Use `design-output-audit-skill` to reject repeated scaffolds, generic mock data, and AI-looking preview sets before showing them.
6. Let the user select or refine a direction.
7. Implement the approved design into the real codebase.

## Installation / Usage with Pi

Add this repo as a skills directory in Pi settings, or copy/symlink the skill files into a Pi skill location.

Typical Pi skill locations include:

```text
~/.pi/agent/skills/
.pi/skills/
.agents/skills/
```

You can also add this repo path to Pi settings:

```json
{
  "skills": ["/absolute/path/to/de-ai-fy"]
}
```

Pi will discover:

- `skills/de-ai-fy/SKILL.md`
- `skills/design-preview-skill/SKILL.md`
- `skills/inspirations-skill/SKILL.md`
- `skills/design-output-audit-skill/SKILL.md`

## Philosophy

Do not make websites that look like default AI output.

Good design should feel specific to the product, audience, and context. References are used to extract principles, not to clone. Colour, copy, layout, motion, data, states, IA, and components should all serve a deliberate design thesis.
