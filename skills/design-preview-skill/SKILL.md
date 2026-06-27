---
name: design-preview-skill
description: Generate multiple standalone HTML design-preview iterations, open them in the browser, and ask the user to choose the best direction before final implementation. Use when designing websites, landing pages, product UIs, components, or visual redesigns where the user wants options, alternatives, exploration, or surgical refinements like font swaps, color tweaks, spacing adjustments, or more iterations of a selected direction.
---

# Design Preview Skill

Use this skill to explore multiple visual directions before committing to a final design. The agent should create **N separate HTML previews**, open them for the user, then ask the user which direction suits them best.

## When to Use

Use this skill when the user asks for:

- Multiple design options or iterations.
- A website, landing page, app screen, dashboard, marketing page, portfolio, or component redesign.
- “Show me a few directions,” “make variants,” “try different styles,” or similar.
- Follow-up refinement requests like “modify the fonts,” “make option 2 warmer,” “generate 4 more iterations of design 1,” “try this layout with different colors,” or “keep this but adjust spacing.”
- A design decision where visual comparison is more useful than text description.

If the user gives a number, that is **N**. If no number is given, default to **3** previews. If the user asks for more than 6, confirm or create an index-only browser launch to avoid opening too many tabs.

## Core Workflow

1. **Lock the design context.** If the prompt or codebase does not reveal the product goal, audience, target screen/workflow, and key content/data, ask up to 3 targeted questions or inspect available files. Do not fill major gaps with generic defaults.
2. **Determine N.** Use the requested number, otherwise default to 3.
3. **Define the scenario and data fixture.** Pick the concrete user moment each option is proving, the domain objects on screen, and at least one realistic state beyond a perfect happy path when appropriate.
4. **Write a divergence contract before coding.** Each option must vary at least two high-level axes such as IA/flow, layout structure, interaction model, typography, density, color, motion, component anatomy, or content emphasis.
5. **Create a preview workspace:**
   - `design-previews/<project-or-feature-slug>-<timestamp>/`
   - `index.html` as a gallery/launcher for all options.
   - `option-01-<direction-name>.html`, `option-02-<direction-name>.html`, etc.
   - `manifest.md` with the brief, scenarios, divergence contract, and self-review notes.
6. **Generate N independently authored directions.** Do not make superficial color swaps and do not reuse one visual scaffold with different tokens. Vary concept, layout, typography, density, color, motion, component treatment, content emphasis, and interaction grammar.
7. **Run the self-review gate.** If options share the same skeleton, repeated fake numbers, formulaic copy, or generic app/dashboard patterns, rewrite the weak options before opening them.
8. **Open the previews.** Open the gallery and, when reasonable, each option HTML file in the browser.
9. **Ask the user to choose.** Present a concise numbered list and ask which option, blend, or revision they prefer.
10. **Wait for selection before final implementation.** Do not build the final design into the production app until the user chooses or requests a combination.

## If the User Rejects the Visual Quality

When the user says the previews look bad, generic, AI-generated, samey, or templated, treat that as a failed audit, not as a request for cosmetic polish.

1. **Stop patching.** Do not merely remove side notes, change colors, add shadows, tweak spacing, or rename options.
2. **State the scaffold failure internally.** Identify the repeated skeleton: phone frame, status bar, bottom nav, rounded cards, dashboard summary, rationale column, fake device/browser chrome, or identical class structure.
3. **Cut weak variants.** Prefer fewer stronger previews over keeping every previous option alive.
4. **Regenerate from product artifacts.** Pick domain-native structures before styling: receipt, rack timer, barcode review, contact sheet, weekly board, map, editor, lab label, inspection bench, route, ledger, dial, or flow strip.
5. **Change the viewport model.** For mobile products, at least one direction should avoid decorative phone chrome; show a full-viewport screen, native sheet, interaction close-up, or storyboard instead.
6. **Move rationale out of the preview.** The option HTML should read as product UI, not a slide explaining itself.
7. **Re-run the audit skill** and rewrite anything that still looks like a generic dashboard with different colors.
8. **Rebuild color and text.** If the user says colors/text are off, redo the pre-code contract: palette roles, contrast, type roles, headings, CTAs, helper text, warnings, and empty/error states. Do not keep the old tokens.

## Pre-Code Art Direction Contract

Before writing preview files, create this contract and include the compact version in `manifest.md`. Do not start HTML/CSS until it exists.

```text
Reference-to-decision map:
- Positive reference 1 -> visible type/color/layout/copy/interaction decision:
- Positive reference 2 -> visible type/color/layout/copy/interaction decision:
- Negative reference/pattern -> rule that prevents the failure:

Content model:
- Real nouns on screen:
- User action:
- Imperfect state / edge case:
- Exact CTA language:

Visual system:
- Typography roles: display / title / body / label / numeric:
- Colour tokens: background / surface / text / muted / border / primary / success / warning / danger / focus:
- Component grammar: radius / borders / shadows / density / icon style:
- Layout grammar: grid / flow / nav / hierarchy / spacing rhythm:
```

Quality rules for the contract:

- Every colour must have a role. Delete decorative colours that only “look nice.”
- Every heading must communicate a product fact, user state, or action. Delete vague mood lines.
- Every option must have a different structural noun, not just a different adjective: e.g. receipt, editor, board, sheet, map, inspection queue, timeline, dial.
- At least one reference decision must affect content or interaction, not only palette.

## Design Brief Gate

Before writing preview files, establish these fields internally and include the important ones in `manifest.md`:

```text
Product/context:
Target user:
Primary screen or workflow:
Existing product constraints:
Real content/data available:
Top user action:
Failure/edge state to represent:
Tone/art direction:
What must stay consistent across options:
What must intentionally diverge:
```

If too many fields are unknown and no code/content source is available, ask up to 3 focused clarifying questions instead of generating from vague assumptions. If the user wants speed, proceed with explicit assumptions in the manifest.

## Divergence Contract

A preview set fails if it looks like one template with theme swaps. For broad exploration:

- Each option must change at least **two** high-level axes: IA/flow, layout skeleton, primary interaction model, navigation model, component anatomy, density, typography system, color logic, motion language, or content model.
- At least one option should change the **workflow framing**, not just the mood: for example command-first vs timeline-first, editor-first vs dashboard-first, map-first vs list-first, receipt-first vs chart-first.
- Do not let every option share the same outer shell, phone/browser chrome, status bar, bottom nav, side rationale panel, card stack, and class structure. If a shared device frame is necessary, the product UI inside it must be materially different.
- Do not use fake mobile/browser chrome as a default presentation device. It is allowed only when the chrome itself is a real product constraint or when the UI inside has a clearly different interaction model.
- Give each option a different signature product move. A palette, background texture, badge shape, or new option name is not enough.
- Keep comparison fair by preserving the same product truths and goals, but do not copy-paste the same fake rows, numbers, and labels into every direction.

In `manifest.md`, include a compact table:

```text
Option | Scenario | Axes changed | Signature move | Shared constraints | Anti-template risk checked
```

## Scenario, Copy, and Mock Data Contract

Mock content should feel gathered from the product, not invented by a model at the last minute. Copy quality is part of visual quality; weak text makes even polished UI look AI-generated.

- Build a coherent fixture: names, timestamps, totals, units, statuses, item labels, and edge states should all belong to the same plausible story.
- Use domain vocabulary and objects from the actual product or codebase when available.
- Prefer concrete states over generic metrics: draft, overdue, edited, syncing, skipped, conflicted, expiring, low stock, PR blocked, rest timer, barcode failed, invite pending.
- Avoid repeating the same generic numbers across options (`2,000 target`, `1.2L`, `45 min`, `98%`, `10k users`) unless the user supplied them.
- Do not imply unsupported product capabilities. If a capability is speculative, label it as a concept in the manifest, not as shipped product behavior.
- Draft the real on-screen headings and CTAs before layout. Headings should be scannable and useful; CTAs should be verbs with consequences.
- Include at least one helper, warning, empty, loading, undo, or confirmation line when the workflow naturally needs it.
- Remove self-important or faux-profound copy. Ask: “why would anyone want to read this?” If the answer is not clear, rewrite.

## Surgical Refinement Workflow

When the user asks for a targeted alteration, do **not** restart the design process unless they explicitly request a fresh direction. Treat the selected option as the base design and make controlled, comparable variations.

Examples of surgical requests:

- “Modify the fonts.”
- “Generate N more iterations of design X.”
- “Keep option 2 but make it more premium.”
- “Try different button styles only.”
- “Make the hero less busy.”
- “Use the layout from 1 with the colors from 3.”

Rules for surgical refinement:

1. **Preserve the base.** Keep the chosen layout, content, hierarchy, and interaction model unless the user targets one of those areas.
2. **Change one design axis at a time** when possible: typography, palette, spacing, component treatment, hero composition, imagery, motion, density, or copy tone.
3. **Create N new derived previews** using lineage-aware names:
   - `option-02a-font-editorial.html`
   - `option-02b-font-technical.html`
   - `option-02c-font-luxury.html`
4. **Make differences visible but controlled.** A font iteration should materially change typeface, scale, weight, tracking, and heading/body pairing while leaving color/layout mostly intact.
5. **Keep comparisons fair.** Use the same content and approximately the same viewport assumptions across derived previews.
6. **Update the gallery/index** so the user can compare the original option against the new variants.
7. **Explain the delta, not the whole design.** Summaries should say what changed: “same layout, sharper condensed headings, calmer body text.”

### Common Surgical Axes

- **Typography:** Try 2-5 distinct font systems: editorial serif + humanist sans, condensed grotesk + neutral text, mono/technical + warm sans, luxury high-contrast serif, playful rounded display. Adjust scale, line height, tracking, and weights; do not merely change `font-family`.
- **Color:** Preserve layout and type while testing palette mood: warmer, cooler, higher contrast, monochrome plus accent, muted premium, energetic campaign, dark mode, light mode. Always define semantic roles and check contrast; never swap random hex values.
- **Spacing/density:** Keep visual identity while testing compact, balanced, and spacious rhythm. Adjust section padding, grid gaps, card padding, line length, and nav density.
- **Components:** Keep page composition while varying button shape, card treatment, borders, shadows, input states, nav style, badges, and iconography.
- **Hero:** Keep brand system while testing headline alignment, media placement, CTA grouping, proof placement, background treatment, or above-the-fold density.
- **Motion:** Keep static design while testing subtle, expressive, or reduced motion. Always include reduced-motion handling.

If the user asks for “N more iterations of design X,” generate N variants that orbit the selected design rather than unrelated concepts. Make each variant a different plausible evolution of that same direction.

## Preview File Requirements

Each option must be a standalone `.html` file with inline CSS and minimal inline JS when needed. The file should run directly from disk with no build step.

Each preview should include:

- A small visible label such as `Option 01 — Editorial Signal`; keep it unobtrusive so the page still feels like the product, not a presentation slide.
- Realistic content based on the user's product, not lorem ipsum unless no context exists.
- A concrete screen, flow slice, transaction, editor, review state, or decision moment; not only a static marketing/dashboard summary when the task involves product interaction.
- A distinctive structural idea inside the UI itself: layout, IA, navigation, editing model, data display, or control system.
- Responsive layout for mobile and desktop.
- Semantic HTML structure.
- Accessible contrast, visible focus states, and touch-friendly controls.
- `prefers-reduced-motion` handling if animations are used.
- Enough interaction states to judge the direction: hover, active, selected, form state, nav state, empty/loading/error/success state, or card state when relevant.

Avoid:

- Tiny tweaks masquerading as separate options for broad exploration.
- Wholesale redesigns when the user asked for a surgical alteration.
- Generic AI SaaS templates repeated with different gradients.
- Reusing the same HTML/CSS scaffold, class names, bottom nav, card stack, device chrome, or explanatory side panel for every option.
- Using a phone mockup/status bar/bottom nav as decorative preview furniture rather than a real product requirement.
- Repeating the same fake numbers, rows, labels, and section copy across options without a product reason.
- Letting side notes explain the concept while the actual screen remains generic.
- Remote assets that may break unless they are clearly optional.
- Heavy dependencies, build pipelines, or framework code for previews.
- Misleading mock data that implies unsupported product capabilities.

## Iteration Quality Bar

Good preview sets should feel like a design review with a strong creative director. Each option needs a distinct thesis.

Examples of useful divergence:

- **Option 01: Editorial / magazine** — oversized type, asymmetry, story-led sections.
- **Option 02: Technical / instrument panel** — dense but controlled data, grid lines, precise states.
- **Option 03: Warm premium** — calm color, tactile surfaces, generous space, refined motion.
- **Option 04: Playful / kinetic** — expressive shapes, bouncy interactions, memorable illustrations.
- **Option 05: Brutalist / raw** — stark contrast, exposed grid, blunt hierarchy, minimal decoration.

Use the same underlying product truth across options when possible so the user is comparing design direction, not unrelated concepts. This does **not** mean copy-pasting identical fake numbers and rows into every file; adapt the scenario details so each direction proves its own workflow.

Bad preview set smells:

- Every option has the same `phone > screen > status > option label > content > bottom nav` skeleton.
- Every option uses the same card grid/list rhythm with only color and border changes.
- Every option explains itself with the same “Best for / Design move / Avoids” side panel.
- The option would look identical in a design portfolio screenshot after replacing product nouns with CRM, finance, AI notes, or wellness labels.
- The colours feel unrelated to the product world or have no semantic roles.
- The copy sounds like an attractive caption instead of useful interface language.
- Mock data repeats across files without forming a plausible scenario.
- The UI could be renamed from a fitness app to a finance app or CRM with only label changes.
- References are cited in the manifest but not visible in decisions about type, structure, interaction, or content.

## Self-Review Gate

Before opening previews, review the files as if rejecting generic AI output:

1. **Scaffold check:** do the options share more than necessary? If yes, redesign at least one from a different IA or flow model.
2. **Product specificity check:** can the product name be swapped out? If yes, add domain artifacts, real controls, and scenario-specific copy.
3. **Data coherence check:** do numbers, rows, timestamps, and statuses tell one believable story? If not, rewrite the fixture.
4. **Interaction check:** is there a real action/state to judge, not just a pretty static panel? If not, add controls or a flow slice.
5. **Rationale check:** is the design thesis visible in the product UI itself, not only in an aside or manifest? If not, change the screen.
6. **Colour check:** can you name the role of every hue and verify readable contrast? If not, rebuild the palette.
7. **Copy check:** do headings, labels, CTAs, and warnings help the user act? If not, rewrite the copy before touching CSS.

Rewrite failing options before opening them.

## Opening Previews

After writing the files, use a shell command appropriate to the environment.

Preferred macOS command for **N ≤ 6**:

```bash
PREVIEW_DIR="design-previews/<slug>-<timestamp>"
open "$PREVIEW_DIR/index.html"
open "$PREVIEW_DIR"/option-*.html
```

For **N > 6** or when the user asked for index-only review:

```bash
PREVIEW_DIR="design-previews/<slug>-<timestamp>"
open "$PREVIEW_DIR/index.html"
```

Portable fallback opens the gallery only:

```bash
PREVIEW_DIR="design-previews/<slug>-<timestamp>"
if command -v open >/dev/null 2>&1; then
  open "$PREVIEW_DIR/index.html"
elif command -v xdg-open >/dev/null 2>&1; then
  xdg-open "$PREVIEW_DIR/index.html"
elif command -v python3 >/dev/null 2>&1; then
  python3 -m webbrowser "$PREVIEW_DIR/index.html"
else
  echo "Open $PREVIEW_DIR/index.html manually"
fi
```

For large N, open `index.html` only and let the user choose individual previews from the gallery.

## Response After Opening

After opening previews, respond with:

```text
Created and opened N design previews:
1. <Name> — <one-line thesis> — <path>
2. <Name> — <one-line thesis> — <path>
3. <Name> — <one-line thesis> — <path>

Pick one option, or tell me what to combine/refine, e.g. “2 with the hero from 1,” “3 but more premium,” “modify the fonts on 2,” or “generate 4 more iterations of option 1.”
```

Keep the response concise. The user should judge visually in the browser.

## After the User Selects

When the user selects an option:

1. Confirm the selected direction.
2. Ask any required implementation-specific question only if needed.
3. Convert the selected HTML direction into the target codebase or requested final artifact.
4. Preserve the chosen art direction: typography, spacing, layout grammar, color system, motion language, and component treatments.
5. If the user requests a blend, create one additional combined preview before final implementation unless the blend is trivial.
6. If the user requests surgical refinements, generate derived previews from the selected option and reopen the updated gallery instead of implementing immediately.
7. Only implement in the production codebase once the user has approved a final direction or explicitly asks to skip further previews.
