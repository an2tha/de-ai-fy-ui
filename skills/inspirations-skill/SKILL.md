---
name: inspirations-skill
description: Find, evaluate, and translate design inspiration into original website directions aligned with de-ai-fy standards. Use when researching visual references, building moodboards, choosing between references, or deciding whether an inspiration source is useful or too generic, derivative, inaccessible, or AI-looking.
---

# Inspirations Skill

Use this skill to find **good design inspiration** and convert it into original design rules. Inspiration is not a template to copy. It is raw material for understanding art direction, hierarchy, typography, colour, motion, interaction, and content strategy.

This skill must align with the main `de-ai-fy` standards: avoid generic AI aesthetics, bad colour defaults, vague AI copy, template layouts, dark patterns, and trend-chasing without product fit.

## When to Use

Use this skill when the user asks to:

- Find inspiration, references, examples, moodboards, or design directions.
- Decide whether a website is good inspiration.
- Make a UI feel less AI-generated or less template-like.
- Compare references before creating a website, landing page, app screen, dashboard, or component system.
- Create multiple design directions from references.

## Inspiration Goal

Good inspiration should help answer:

- What should this product feel like?
- What visual language fits its audience and context?
- What hierarchy, layout, typography, colour, and motion patterns are useful?
- What should be avoided because it is generic, hostile, inaccessible, dated, or irrelevant?
- What original design thesis can be created from these lessons?

## Where to Look

Use a mix of reference types. Do not rely only on award galleries.

1. **Direct category references** — competitors or products with similar user goals.
2. **Adjacent category references** — different industries with similar complexity, trust needs, emotion, or workflow.
3. **High-art-direction references** — award-winning or experimental sites for layout, typography, motion, and storytelling.
4. **Product UI references** — real apps, dashboards, onboarding flows, pricing pages, docs, forms, search, settings, and empty states.
5. **Brand-system references** — typography, colour, logo, photography, iconography, tone of voice, and component rules.
6. **Offline or physical-world references** — magazines, signage, packaging, industrial controls, maps, books, film titles, museum labels, fashion, architecture, scientific instruments, sports graphics.
7. **Negative references** — cluttered, dated, deceptive, or inaccessible examples that define what not to do.

If local files exist, start with:

- `good-websites.txt` for positive web references.
- `bad-examples.txt` for anti-patterns.
- The main `SKILL.md` de-ai-fy rules for standards.

For current inspiration, use web search with varied queries, then fetch promising pages. Search by category, tone, and interaction type rather than only “best website design.”

## Good Inspiration vs Bad Inspiration

### Good Inspiration

A good inspiration source is:

- **Relevant:** It shares the target product's audience, task complexity, emotional tone, trust requirement, or content type.
- **Specific:** It has a clear visual thesis, not a generic SaaS template.
- **Systemic:** Typography, colour, layout, components, motion, and copy feel like one system.
- **Usable:** Navigation, hierarchy, readability, responsiveness, and interaction states are understandable.
- **Shipped or testable:** Prefer live experiences over static mockups when interaction matters.
- **Extractable:** You can name the underlying principle without copying the exact layout, assets, copy, or brand.
- **Distinctive:** It has at least one memorable design move tied to the product's story or function.
- **Accessible enough to learn from:** Contrast, type sizing, focus states, motion restraint, and mobile behaviour are not fundamentally broken.
- **Content-aware:** It demonstrates how real content, data, labels, and proof should be organized.

### Bad Inspiration

A bad inspiration source is:

- **Only pretty at screenshot size** but unusable in a real flow.
- **Trend-first:** glassmorphism, purple gradients, neon glows, generic blobs, or overused 3D objects with no product reason.
- **Irrelevant:** A cinematic WebGL portfolio used as inspiration for a daily-use admin panel without restraint.
- **Derivative:** Looks like every other AI-generated landing page.
- **Empty:** Uses vague copy, fake metrics, placeholder dashboards, and generic claims.
- **Inaccessible:** Low contrast, tiny text, motion overload, hidden controls, or mobile breakage.
- **Hostile:** Dark patterns, deceptive CTAs, confusing forms, forced signups, or obstruction.
- **Unadaptable:** Depends on proprietary assets, brand equity, celebrity imagery, or a technical budget the project does not have.
- **Too broad:** A giant moodboard with no selection criteria, causing bland averaging.

Rule: if the only thing you can say is “it looks cool,” it is weak inspiration. Good inspiration teaches a transferable design principle.

## Evaluation Rubric

Score each candidate from 0-3:

- **Product fit:** Does it match the user's audience, task, and tone?
- **Art direction:** Is there a clear point of view?
- **System depth:** Are type, colour, layout, motion, and components coherent?
- **Hierarchy:** Can users scan and understand what matters?
- **Usability:** Are nav, forms, states, and responsive behaviour sane?
- **Originality:** Does it avoid generic AI/template aesthetics?
- **Colour quality:** Are colours ownable, disciplined, and accessible rather than generic purple/blue/teal defaults?
- **Copy quality:** Is the text concrete and domain-specific rather than buzzword filler?
- **Extractability:** Can you borrow principles without copying assets or layout?

Keep references that score highly on fit + extractability, not just visual novelty.

## Extraction Workflow

For each selected inspiration, extract:

1. Typography system
2. Colour system and colour roles
3. Layout grammar
4. Spacing rhythm
5. Component treatment
6. Motion language
7. Image, illustration, icon, or 3D style
8. Navigation and information architecture
9. Content density
10. Copy tone and specificity
11. One distinctive design move
12. What makes it feel human-designed
13. What should not be copied directly
14. One principle to apply to the target product

Never copy:

- Proprietary layout structure exactly
- Brand colours or logos
- Original copy
- Illustrations, photos, icons, 3D assets, videos, or sounds
- Signature interactions that would be recognizable as another brand's experience

## Colour Inspiration Rules

When using colour inspiration, extract relationships, not hex codes.

Prefer notes like:

- “Muted mineral neutrals with one sharp safety-orange accent.”
- “Warm paper background, ink text, restrained botanical green for action.”
- “Dark graphite interface with amber instrument-panel state colours.”

Avoid:

- Copying exact brand palettes.
- Reusing generic AI palettes: purple-blue gradients, teal-on-white SaaS, neon cyan/pink on black, washed pastel cards.
- Letting every reference contribute a colour until the palette becomes random.

A good colour reference explains hierarchy, mood, and state. A bad colour reference is merely decorative.

## Copy Inspiration Rules

Study how good references make copy specific:

- Real product objects
- Real roles and workflows
- Concrete proof
- Clear CTAs
- Useful section headings
- Honest constraints

Reject inspiration whose copy is interchangeable buzzword filler. If the words could describe any startup, do not imitate that voice.

## Building an Inspiration Set

For most design tasks, collect:

- 2 direct references
- 2 adjacent references
- 1 high-art-direction reference
- 1 product/UI reference
- 1 negative reference

Then reduce to **2-4 primary influences**. Too many references create averaged, generic output.

For each primary influence, define:

```text
Reference:
Why it is relevant:
What to learn:
What not to copy:
Design principle to apply:
Risk if overused:
```

## Translating Inspiration Into Original Direction

After research, create a new design thesis:

```text
Target product:
Audience:
Desired feeling:
Primary inspiration lessons:
Negative references avoided:
Original art direction:
Typography direction:
Colour direction:
Layout grammar:
Motion language:
Content/copy voice:
Signature design move:
```

The final direction must feel inevitable for the user's product, not like a collage of references.

## Output Format

When presenting inspiration findings to the user, be concise:

```text
I found 6 references and would use 3:

1. <Reference> — useful for <principle>, avoid copying <risk>.
2. <Reference> — useful for <principle>, avoid copying <risk>.
3. <Reference> — useful for <principle>, avoid copying <risk>.

Negative constraint:
- Avoid <bad reference/pattern> because <reason>.

Recommended direction:
- <one clear design thesis>
```

If the user wants visual exploration, hand off to `design-preview-skill`: create multiple standalone HTML previews based on the selected inspiration principles and let the user choose.
