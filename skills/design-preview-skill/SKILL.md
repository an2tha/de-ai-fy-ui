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

1. **Clarify only if blocked.** If requirements are clear enough, do not ask a preliminary question; proceed with previews.
2. **Determine N.** Use the requested number, otherwise default to 3.
3. **Create a preview workspace:**
   - `design-previews/<project-or-feature-slug>-<timestamp>/`
   - `index.html` as a gallery/launcher for all options.
   - `option-01-<direction-name>.html`, `option-02-<direction-name>.html`, etc.
   - Optional `manifest.md` summarizing the concepts.
4. **Generate N meaningfully different directions.** Do not make superficial color swaps. Vary concept, layout, typography, density, color, motion, component treatment, and content emphasis.
5. **Open the previews.** Open the gallery and, when reasonable, each option HTML file in the browser.
6. **Ask the user to choose.** Present a concise numbered list and ask which option, blend, or revision they prefer.
7. **Wait for selection before final implementation.** Do not build the final design into the production app until the user chooses or requests a combination.

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
- **Color:** Preserve layout and type while testing palette mood: warmer, cooler, higher contrast, monochrome plus accent, muted premium, energetic campaign, dark mode, light mode.
- **Spacing/density:** Keep visual identity while testing compact, balanced, and spacious rhythm. Adjust section padding, grid gaps, card padding, line length, and nav density.
- **Components:** Keep page composition while varying button shape, card treatment, borders, shadows, input states, nav style, badges, and iconography.
- **Hero:** Keep brand system while testing headline alignment, media placement, CTA grouping, proof placement, background treatment, or above-the-fold density.
- **Motion:** Keep static design while testing subtle, expressive, or reduced motion. Always include reduced-motion handling.

If the user asks for “N more iterations of design X,” generate N variants that orbit the selected design rather than unrelated concepts. Make each variant a different plausible evolution of that same direction.

## Preview File Requirements

Each option must be a standalone `.html` file with inline CSS and minimal inline JS when needed. The file should run directly from disk with no build step.

Each preview should include:

- A small visible label such as `Option 01 — Editorial Signal`.
- Realistic content based on the user's product, not lorem ipsum unless no context exists.
- Responsive layout for mobile and desktop.
- Semantic HTML structure.
- Accessible contrast, visible focus states, and touch-friendly controls.
- `prefers-reduced-motion` handling if animations are used.
- Enough interaction states to judge the direction: hover, active, selected, form state, nav state, or card state when relevant.

Avoid:

- Tiny tweaks masquerading as separate options for broad exploration.
- Wholesale redesigns when the user asked for a surgical alteration.
- Generic AI SaaS templates repeated with different gradients.
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

Use the same underlying content across options when possible so the user is comparing design direction, not copy differences.

## Opening Previews

After writing the files, use a shell command appropriate to the environment.

Preferred macOS command:

```bash
PREVIEW_DIR="design-previews/<slug>-<timestamp>"
open "$PREVIEW_DIR/index.html"
open "$PREVIEW_DIR"/option-*.html
```

Portable fallback:

```bash
PREVIEW_DIR="design-previews/<slug>-<timestamp>"
if command -v open >/dev/null 2>&1; then
  open "$PREVIEW_DIR/index.html"
  open "$PREVIEW_DIR"/option-*.html
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
