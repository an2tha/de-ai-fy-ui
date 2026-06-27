---
name: design-output-audit-skill
description: Audit generated design previews or implemented UI for AI-generated/template-like fingerprints, then produce concrete revision instructions or rewrite failing previews before they are shown. Use when the user says a design still looks AI-generated, when reviewing design-preview outputs, or before delivering multiple UI options.
---

# Design Output Audit Skill

Use this skill after generating previews or implementing UI, and whenever the user says the work still feels AI-generated. The goal is not to praise or lightly critique; the goal is to find template fingerprints and force concrete fixes.

This skill complements `de-ai-fy`, `design-preview-skill`, and `inspirations-skill`.

## When to Use

Use this skill when:

- Reviewing `design-previews/...` HTML files before opening them.
- The user says outputs look AI-generated, generic, templated, sterile, or samey.
- Comparing multiple generated design directions.
- Auditing a landing page, dashboard, product screen, or component set for specificity and craft.
- Deciding whether to revise generated previews before final implementation.

## Audit Workflow

1. **Collect the artifacts.** Read the preview directory, `manifest.md`, `index.html`, and option files. For implemented UI, inspect the relevant source components, routes, styles, and sample data.
2. **Compare options against each other.** AI-generated sets often look acceptable one-by-one but fail as a set because every option shares the same shell, nav, card rhythm, mock data, and rationale structure.
3. **Check product specificity.** Verify that labels, data, controls, states, and copy could only belong to this product and user scenario.
4. **Check structural divergence.** Confirm that each broad option changes at least two high-level axes: IA/flow, layout skeleton, interaction model, navigation model, component anatomy, density, typography, color logic, motion, or content model.
5. **Check data coherence.** Numbers, timestamps, names, statuses, units, and rows should tell a plausible story. Repeated generic metrics are a failure.
6. **Check reference usefulness.** References cited in the manifest must map to visible decisions. Drop references that are merely decorative citations.
7. **Prescribe fixes.** For each failing option, say exactly what to change: structure, flow, content fixture, component anatomy, copy, type, color, motion, states, or accessibility.
8. **Revise before delivery when possible.** If you own the preview files and the failure is clear, rewrite the weakest options rather than asking the user to choose from flawed work.
9. **Escalate to regeneration when needed.** If the same scaffold appears in most options, do not prescribe tweaks. Reject the set and rebuild fewer, stronger directions from different product artifacts.

## Hard Regeneration Triggers

Reject and regenerate rather than revise when any of these are true:

- The options are all arranged as a decorative phone/browser mockup with the same status bar, nav, card stack, and option badge.
- Removing the side rationale makes the product UI feel ordinary or empty.
- The most memorable thing about the set is the presentation frame, not a product-specific interaction.
- The previews rely on safe muted palettes, rounded rectangles, and generic card lists without a domain-native structure.
- The UI can be renamed to a CRM, finance tool, AI notes app, or generic wellness dashboard with only copy changes.
- The user explicitly says it still looks AI-generated or bad after a revision pass.

Regeneration means: cut weak variants, choose new structural metaphors from the product domain, vary viewport models, and rewrite files before showing them again.

## Visual Craft Audit

Run this when the user says colours, text, or everything feels off. These are not subjective polish notes; they are pass/fail gates.

### Colour gate

Fail if:

- The palette has more than one or two accent hues without semantic jobs.
- Muted colours are so close in luminance that hierarchy collapses.
- The palette looks like a generic AI theme: purple/blue glow, random teal, muddy beige/charcoal, washed pastels, or neon-on-black without product reason.
- Text, labels, disabled states, or focus states have poor contrast.
- Light/dark modes are simple inversions rather than separately designed systems.

Fix by defining semantic tokens: background, surface, elevated, text, muted, border, primary action, success, warning, danger, focus, and optional data colors.

### Typography gate

Fail if:

- The design uses default/system fonts everywhere without a deliberate reason.
- There is no clear role separation between display, title, body, label, numeric, and code text.
- Small labels are too thin, too tight, too low contrast, or overused in all caps.
- Headings are oversized but uninformative.

Fix by choosing type roles first, then scale, tracking, line height, and weight. Mobile body text should remain comfortably legible and controls should be touch-sized.

### Copy gate

Fail if:

- Headings sound like marketing captions rather than interface language.
- CTAs are generic (`Get started`, `Learn more`, `Continue`) when a specific action is available.
- The copy contains faux-profound lines, over-polished rhythms, or buzzwords.
- Warnings, empty states, helper text, and confirmations are missing from workflows that need them.

Fix by writing from the user's immediate situation: what happened, what it means, what action is safe, and what changes after the action.

### Composition gate

Fail if:

- Everything is a card, all cards have similar weight, or the primary action does not dominate.
- Layout is centered by default with no product-specific reading order.
- Spacing is decorative rather than functional: cramped controls, random gaps, or no grouping logic.
- The strongest visual idea is a frame/mockup rather than the product workflow.

Fix by rebuilding hierarchy from the content model before changing colors.

## Static Smell Checks for Preview Directories

Use these quick inspections when auditing standalone HTML previews. They do not replace judgment, but they reveal repeated scaffolds quickly.

```bash
PREVIEW_DIR="design-previews/<slug>-<timestamp>"

# Shared class-name fingerprints.
grep -Rho 'class="[^"]*"' "$PREVIEW_DIR"/option-*.html | sort | uniq -c | sort -nr | head -40

# Repeated explanatory/rationale labels.
grep -RInE 'Best for|Design move|Avoids|This direction|Option [0-9]' "$PREVIEW_DIR"/*.html "$PREVIEW_DIR"/*.md

# Repeated mock metrics and units.
grep -RhoE '[0-9][0-9,.]*( ?(kcal|cal|g|kg|lb|L|ml|min|hrs|%|users|tasks|tickets|items))?' "$PREVIEW_DIR"/option-*.html | sort | uniq -c | sort -nr | head -40

# Shared navigation/status shells.
grep -RInE '<nav|status|bottom nav|tab bar|phone|screen|dashboard|card' "$PREVIEW_DIR"/option-*.html
```

Flag suspicious repetition, then inspect the actual files before deciding.

## Rejection Criteria

Reject or revise a preview set if any of these are true:

- Every option uses the same device/browser frame, status bar, bottom nav, card stack, and side explanation panel.
- Options differ mainly by palette, gradient, border radius, surface texture, or option naming.
- The primary screen is a generic dashboard summary when the requested product needs a flow, editor, form, log, decision, review, or transaction state.
- Mock data repeats across options or feels like model defaults rather than one coherent scenario.
- Copy uses polished but interchangeable phrases, repeated three-part rhythms, faux-profound captions, or generic CTAs.
- Colors are chosen as mood decoration rather than a semantic system with readable contrast.
- Typography has no role system or relies on default fonts without a deliberate concept.
- References are cited but cannot be traced to visible type, structure, interaction, content, or state decisions.
- The design thesis is clearer in the side notes than in the product UI itself.
- No realistic imperfect state appears where the product would naturally have loading, empty, warning, edit, conflict, undo, error, offline, privacy, or partial-completion states.
- The UI could be renamed for an unrelated product with only text/color changes.
- A screenshot crop of the main UI would look like a generic template once the option label is hidden.

## Scoring Rubric

Score each option from 0-2:

- **Product specificity:** domain artifacts, vocabulary, controls, and states.
- **Structural originality:** layout and IA are chosen, not defaulted.
- **Divergence from siblings:** option is meaningfully different from the others.
- **Data realism:** fixture is coherent and plausible.
- **Copy quality:** concrete, varied, and useful rather than generic.
- **Colour quality:** palette has semantic roles, product fit, restraint, and contrast.
- **Typography quality:** type roles, scale, line height, and weight create hierarchy and legibility.
- **Visual system:** typography, color, spacing, components, and motion form one concept.
- **Interaction/state depth:** there is a real action or state to judge.
- **Accessibility/responsiveness:** contrast, focus, touch targets, reduced motion, and small-screen behavior are considered.

Any option scoring 0 in product specificity, structural originality, data realism, colour quality, typography quality, or copy quality should be revised before presentation. If more than half the options score 0 in structural originality or divergence from siblings, reject the set and regenerate from different product artifacts.

## Audit Output Format

When reporting an audit, be direct:

```text
Verdict: pass / revise before showing / reject and regenerate

Top issues:
1. <issue> — evidence: <file/path:line or pattern> — fix: <specific change>
2. <issue> — evidence: <file/path:line or pattern> — fix: <specific change>
3. <issue> — evidence: <file/path:line or pattern> — fix: <specific change>

Option decisions:
- Option 01: keep / revise / reject — <reason>
- Option 02: keep / revise / reject — <reason>

Required revisions:
- <concrete edit or regeneration instruction>
```

Keep the audit actionable. Do not hide behind subjective language like “make it better” or “more premium.”
