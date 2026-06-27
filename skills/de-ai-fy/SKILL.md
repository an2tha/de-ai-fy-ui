---
name: de-ai-fy
summary: Create distinctive, credible, human-designed websites by studying curated high-quality references and converting bad-web examples into concrete constraints.
description: Use this skill when designing or implementing a website, landing page, product UI, web app, portfolio, marketing page, component system, or when asked to make an interface look less AI-generated. It emphasizes original art direction, strong hierarchy, usability, responsive craft, accessibility, and avoidance of clutter, generic AI aesthetics, and hostile UX patterns.
---

# De-AI-Fy Website Design Skill

This skill helps agents create websites that feel intentionally designed by a skilled human, not generated from a default template. Use `good-websites.txt` as a positive reference bank and `bad-examples.txt` as a negative reference bank.

Do **not** clone layouts, assets, copy, brand systems, illustrations, or proprietary interactions from any reference. Extract principles, then create a new visual system for the target product.

## Activation

Use this skill whenever the user asks to:

- Build, redesign, polish, or critique a website or web app.
- Create a landing page, portfolio, marketing site, microsite, brand page, product UI, dashboard, or component library.
- Make an interface look less generic, less AI-generated, more premium, more memorable, or more usable.
- Diagnose why a site feels cluttered, dated, confusing, inaccessible, or untrustworthy.

## Required Reference Workflow

Before major design work:

1. Read the local reference files if available:
   - `good-websites.txt` for strong visual-direction examples.
   - `bad-examples.txt` for failure modes and anti-patterns.
2. Choose 2-4 positive references relevant to the product category or desired tone.
3. Choose 1-2 negative references or bad-pattern categories to explicitly avoid.
4. Extract lessons; never copy surface details.
5. Define a fresh art direction for the user's actual product.
6. Write a tiny **reference-to-decision map** before coding: each reference must change a visible typography, colour, layout, component, copy, interaction, or data decision.
7. If the user says the output is bad or AI-looking, fetch or reread the best references again and regenerate from the decision map instead of tweaking the rejected output.

For each positive reference, study:

- Typography system
- Color system
- Layout grammar
- Spacing rhythm
- Component treatment
- Motion language
- Image or illustration style
- Navigation structure
- Content density
- One distinctive design move
- What makes it feel human-designed
- What must not be copied directly

For each negative reference, study:

- Where hierarchy fails
- Why navigation is confusing
- Why typography is hard to read
- Why colors feel unpleasant or inaccessible
- Why layout feels cluttered, dated, or careless
- Which interactions feel hostile, misleading, or dark-patterned
- What breaks on mobile or small screens
- What content is missing, duplicated, vague, or overwhelming
- Which visual choices would be unacceptable in a modern product UI
- The one rule that prevents the failure

## Research-Backed Lessons From the Reference Set

Use these as operating rules when translating the good and bad examples into original work:

- **Dropbox Brand / Charles Eames principle:** details are not decoration; they are the design. Every border, texture, icon, label, and spacing rule needs a job. If a detail cannot explain its job, remove it.
- **Linear principle:** credible product UI shows real artifacts: issue IDs, comments, code, states, timelines, ownership, failure modes, and priority. For other products, substitute equally real domain artifacts instead of generic metrics.
- **Raycast principle:** a strong concept can come from one product behavior. Raycast’s keyboard/launcher world changes copy, layout, interaction, and proof. Do not borrow “command palette” visually unless the product behavior truly is command-first.
- **Teenage Engineering principle:** sparse navigation, product codes, odd-but-consistent naming, and small physical product details make a brand feel authored. Quirk works only when the system is disciplined.
- **Apple HIG principle:** mobile polish starts with basics: primary content fits the screen, touch targets are at least 44×44 pt, text is legible, contrast is ample, controls sit near the content they affect, and alignment clarifies relationships.
- **Smashing copy principle:** copy is part of design. Ask “why would anyone want to read this?” before placing text. Remove self-important, faux-meaningful, or over-polished lines that do not tell the user anything.
- **Bad-example principle:** clutter, weak hierarchy, low contrast, random colour, tiny tap targets, and hidden/deceptive controls are not style choices. They are rejection reasons.

These lessons are not optional citations. They must produce visible decisions in the output.

## Web-Researched Reference Findings

These observations were distilled from live/fetched reference pages, award/case-study pages, and web-search summaries of the provided lists. Treat them as design lessons, not templates.

### Positive Reference Patterns Observed

- **Brand systems work when they are toolkits, not wallpaper.** Dropbox Brand frames its guidelines as reusable ingredients; ComPsych shows brand purpose, tone, logo, typography, photography, and color as one coherent operating system. Rule: define tokens, voice, image treatment, and component behavior together.
- **Typography can be the whole concept.** Exat builds an entire experience around one typeface's modernist story, structural clarity, broad weights/widths, tester controls, and graphic specimens. Rule: choose type for a reason and let it drive layout, rhythm, and interaction.
- **Immersion must be task-aware and engineered.** Bruno Simon's portfolio turns navigation into a playable 3D world with explicit controls, reset/stuck states, achievements, audio options, and behind-the-scenes transparency. The Monolith Project is described as a scroll-driven cinematic story using hand-drawn illustration, 3D worlds, sound, shader transitions, particles, and performance-minded rendering systems. Lacoste Members Experience turns customization into the actual product flow: marker, paint bucket, eraser, color tools, 3D garment preview, flat editing, sharing views, real-time interaction, storage, and WebGL performance constraints. Messenger by Abeto and similar showcase sites use motion/3D as the content, not as arbitrary decoration. Rule: if the site is immersive, provide controls, fallbacks, performance budgets, and a reason the interaction exists.
- **Editorial narrative beats generic section stacking.** Apple Vision Pro sequences use cases, benefits, technical proof, values, and ecosystem. Symphony of Vines uses sensory, cinematic storytelling around terrain and terroir. Charles Leclerc and Lando Norris turn biography, stats, quotes, racing imagery, helmets, and fan/shop moments into a scrollable narrative. Rule: organize pages as stories with chapters, proof, and pacing.
- **Product UI references feel real because their details are real.** Raycast uses a keyboard/launcher metaphor, concrete productivity claims, recognizable shortcut language, and professional testimonials. Linear shows realistic issue IDs, code snippets, charts, agent workflows, comments, statuses, and product-development artifacts. Rule: replace generic mockups with domain-specific interface evidence.
- **Distinctive brands have their own vocabulary.** Teenage Engineering's terse navigation, product codes, small product imagery, and eccentric naming create a recognizable product universe. Keikku's medical-device page repeats heartbeat language, gestures, LED feedback, specs, and clinical capabilities. Atoll uses a nautical/cargo metaphor for agency positioning. Rule: design copy, naming, labels, and visual metaphors around the product's actual world.
- **Good curation sites reveal variety and trade-offs.** Awwwards, CSS Design Awards, Godly/Recent, Land-book, Siteinspire, Hover States, and Minimal Gallery show that strong sites vary widely: cinematic WebGL, quiet minimalism, editorial systems, technical dashboards, handmade illustration, expressive type, and dense product catalogs can all work. CSS Design Awards evaluates UI, UX, and Innovation; Awwwards-style sources evaluate design, usability, creativity, content, and technical execution. These galleries skew toward marketing, portfolio, agency, and brand-experience work, so do not blindly apply their interaction-heavy style to dashboards or daily-use tools. Rule: never converge on one house style, and always match reference type to product type.
- **Motion is strongest when it has hierarchy.** Strong references concentrate motion into meaningful moments: page-entry sequencing, scroll chapters, object reveals, hover transformations, customization, or product-state transitions. Rule: animate attention, state, and story progression; do not animate everything equally.

### Negative Reference Patterns Observed

- **Clutter destroys scanning.** Arngren shows dense product fragments, tiny images, inconsistent prices, repeated separators, and no obvious grid hierarchy. Similar bad-web roundups repeatedly cite clutter, low contrast, confusing navigation, poor responsiveness, and excessive distractions. Rule: one screen needs a visible reading order and grouped choices.
- **Maximalism needs governance.** LINGsCARS is memorable because of a loud brand personality, but its huge menus, repeated categories, many promotional images, and long brand grids show how quickly personality becomes overload. Rule: if using maximalism, enforce a strict content model, consistent modules, and clear primary actions.
- **Legacy minimalism is not automatically good modern UX.** Berkshire Hathaway, Craigslist, and Hacker News are fast and familiar but rely on plain link lists, small text, sparse visual hierarchy, and old interaction assumptions. Rule: preserve speed and clarity, but add responsive structure, accessible sizing, useful grouping, and modern states.
- **Content density without curation feels dated.** Goodreads-like pages can contain useful recommendations, quotes, covers, awards, and social proof, but weak section hierarchy and crowded modules make discovery feel noisy. Rule: give dense content filters, prioritization, and clear pathways.
- **Bad controls violate user intent.** User Inyerface and Awesome Bad UI examples intentionally use hostile forms, inefficient date/phone selectors, moving/catching targets, fan-controlled cursors, and joke input methods. Rule: controls should match the user's mental model and minimize effort for common tasks.
- **Dark patterns are disallowed, not just ugly.** Deceptive Pattern references identify forced action, obstruction, sneaking, interface interference, nagging, and confirmshaming as manipulative patterns. Rule: make consent, pricing, cancellation, opt-out, destructive actions, and privacy choices clear and reversible where possible.
- **Bad navigation is usually a labeling and priority problem.** Negative examples often expose everything at once, duplicate nav groups, bury important paths, or use vague labels. Rule: reduce top-level choices, name them plainly, show current location, and make search/filtering available when information architecture is large.
- **Mobile failure is a design failure, not an implementation detail.** Cautionary mobile references show tiny tap targets, horizontal scrolling, desktop menus squeezed into narrow screens, broken overlays, and hidden actions. Rule: design mobile structure deliberately and test real content lengths.

## Core Design Standard

A good website must have:

- **A clear concept:** One memorable point of view, not a pile of generic sections.
- **Product evidence:** Real nouns, workflows, constraints, states, and artifacts from the product's domain are visible in the UI.
- **Purposeful hierarchy:** Users can tell what matters in under five seconds.
- **Structural intent:** The page or screen composition is chosen for the workflow, not inherited from a default stack of cards.
- **Original art direction:** Typography, color, layout, and motion fit the product's personality.
- **Responsive craft:** Mobile, tablet, and desktop are designed, not merely squeezed.
- **Accessible interaction:** Semantic HTML, keyboard states, focus states, readable contrast, reduced-motion support.
- **Trustworthy UX:** No deceptive flows, hidden controls, confusing opt-outs, bait-and-switch pricing, or manipulative consent.
- **Production polish:** Real content, robust states, consistent spacing, clean code, performance-aware assets.

## Mandatory Design Passes

Run these passes in order before writing production UI or preview HTML. Skipping them is the main reason outputs look AI-generated.

1. **Content pass:** write the actual nouns, actions, states, errors, labels, and one imperfect scenario. No lorem ipsum, no generic metrics, no “dashboard” until the content proves it needs one.
2. **Structure pass:** choose the product-native model for the screen: editor, receipt, inspection view, timeline, map, board, control panel, sheet, form, log, comparison, or decision queue. Avoid card piles by default.
3. **Typography pass:** choose type roles before colors. Define display, title, body, label, numeric, and code/tabular roles. On mobile, body copy should normally be around platform-default legibility (roughly 16-17px/pt) and small labels must remain readable.
4. **Colour pass:** build semantic tokens, not vibes: background, surface, elevated, text, muted, border, primary action, secondary accent, success, warning, danger, focus. Use one dominant neutral family and one primary accent unless the product truly needs more. Check contrast before calling it done.
5. **Component pass:** define the component grammar: radius, border weight, shadow/no-shadow, density, icons, dividers, buttons, inputs, selected states, disabled states, loading/error states. Components should feel related, not cloned.
6. **Copy pass:** read headings, CTAs, empty states, warnings, and helper text aloud. Replace vague adjectives with product nouns and verbs. If the words could fit any startup, rewrite them.
7. **Visual inspection pass:** open the result and compare it against the reference-to-decision map and bad-example constraints. If color, text, hierarchy, or spacing feels wrong, regenerate the weak screen; do not justify it in prose.

## Rejection / Rebuild Protocol

When a user says a design looks AI-generated, generic, ugly, “off,” or bad, **do not polish the same scaffold**. First identify the visible failure, then rebuild the weakest pieces from a different product model.

Hard rules after rejection:

- Do not respond with minor spacing, border-radius, gradient, or copy tweaks if the underlying skeleton is the problem.
- Name and kill the repeated scaffold: phone mockup, centered hero, rounded card grid, browser chrome, status bar, bottom nav, left rationale panel, fake dashboard, or generic side-by-side preview frame.
- Reduce quantity before quality drops. Three strong directions beat six weak variants.
- Use one product-specific object as the structural spine: a rack timer, receipt, route map, contact sheet, film strip, ledger, command surface, inspection bench, calendar board, lab label, or another domain-native artifact.
- Remove presentation furniture from previews. The preview should look like the product; manifest/index can hold rationale.
- Re-run the bad-example constraints: visible hierarchy, no clutter, no tiny controls, no hostile ambiguity, no vague content.
- Rebuild the colour and copy from first principles. “Colors are off” means the palette lacks roles or contrast; “text is off” means the content pass failed.
- Re-open the result only after the new option would still make sense with the product name hidden.

If the design still looks like it could be rebranded for a CRM, finance app, AI notes app, or generic wellness dashboard, reject it and rebuild again.

## Make It Feel Human-Designed

When designing, commit to a specific creative direction. Examples: editorial/magazine, brutalist/raw, luxury/refined, playful/toy-like, industrial/utilitarian, organic/natural, retro-futuristic, maximalist, technical/instrument-panel, art-deco/geometric, quiet minimalist, or cinematic.

Then encode the direction through:

- **Typography:** Use expressive, context-appropriate font choices. Avoid default stacks unless the concept deliberately requires them. Pair a distinctive display face with a highly readable body face.
- **Color:** Use a disciplined palette with clear dominant, supporting, and accent roles. Avoid timid rainbow palettes and overused purple-blue gradients on white.
- **Layout:** Create a recognizable layout grammar: asymmetry, editorial columns, oversized type, layered panels, diagonal movement, dense technical grids, generous whitespace, or another intentional structure.
- **Spacing:** Use a consistent rhythm. Good spacing is rarely accidental; it should create confidence and calm.
- **Components:** Buttons, cards, forms, nav, badges, and modals should share a visual language without looking copy-pasted.
- **Motion:** Use motion to clarify state, guide attention, and add delight. Prefer a few well-timed moments over constant decoration.
- **Texture and detail:** Add depth through subtle noise, borders, shadows, illustration, iconography, grid lines, custom dividers, image treatment, or tactile micro-details when they support the concept.
- **Content:** Replace lorem ipsum and vague marketing with specific, credible copy. Strong content makes the UI feel real.

## Anti-Template Generation Rules

A design can use good colors and typography and still feel AI-generated if it is clearly produced from a reusable scaffold. Before styling, design the workflow and the content model.

- Start from a concrete user moment: what the user is trying to do, what they already know, what is urgent, what can wait, and what can go wrong.
- Pick the information architecture for that moment. Do not automatically reach for hero + cards, phone shell + bottom nav, dashboard widgets, or a left text brief with a device mockup.
- Make the primary structure product-specific: receipt, map, timeline, instrument panel, specimen sheet, route, ledger, inbox, canvas, checklist, split view, command surface, contact sheet, workbench, counter, dial, or another form that matches the domain.
- If creating multiple options, do not reuse the same outer scaffold, class structure, navigation model, and card rhythm across all of them unless those are hard product constraints. Shared device frames are allowed only when the inside of the product has materially different IA and interaction grammar.
- Avoid fake-device autopilot. A mobile product can be shown as a full viewport, flow strip, interaction close-up, native sheet, storyboard, or artifact view; it does not automatically need a decorative phone frame, status bar, bottom nav, and generic cards.
- Use a coherent data fixture instead of scattered invented numbers. Names, dates, units, statuses, item labels, errors, and totals should belong to the same plausible scenario.
- Include at least one realistic imperfect state when appropriate: overdue, skipped, edited, unsynced, partially complete, unavailable, conflicted, empty, loading, warning, or recovery state.
- Keep design rationale in notes, manifests, or the final response. The preview itself should mostly look like the product, not a poster explaining the design direction.
- Vary component anatomy, not just colors: controls, cards, tables, lists, filters, nav, empty states, and detail views should have shapes and behaviors that follow the chosen concept.
- Avoid "reference theater": do not cite Linear, Raycast, Apple, Teenage Engineering, or gallery sites unless a visible design decision can be traced to a specific lesson.

Anti-template smell test: if another product name could be swapped in with only copy changes, or if all options share the same skeleton with different palettes, the design is not de-AI-fied yet.

## Colour / Color Choice Rules

AI-generated websites often reveal themselves through generic, unconsidered colour choices. Avoid palettes that look like default model output rather than a deliberate brand system.

Do **not** default to:

- Purple-to-blue gradients on white or near-black backgrounds.
- Neon cyan, electric violet, hot pink, and glassmorphism glow combinations unless the product genuinely calls for them.
- Random teal accents, generic indigo buttons, or default Tailwind-like blues used without a brand reason.
- Washed-out pastel backgrounds with low-contrast grey text.
- Over-saturated rainbow palettes where every card has a different hue.
- One accent colour sprayed across every icon, border, button, link, and decoration.
- Sterile black/white/grey palettes with a single AI-blue accent unless the concept is intentionally austere.

Build colour systems deliberately:

- Start from the product's world: materials, audience, industry, geography, photography, physical environment, or emotional tone. Name the source in the design notes.
- Choose a dominant background/surface family first, then text, borders, accents, and semantic states.
- Use one primary accent with restraint; add secondary accents only when they have a job.
- Make neutrals characterful: warm ivory, graphite, bone, ink, clay, fog, metal, charcoal, paper, or other context-specific bases.
- Control saturation. Most mature palettes mix muted foundations with sharp accent moments.
- Ensure contrast for body text, small labels, controls, and focus states.
- Make light and dark themes feel designed separately; do not simply invert colours.
- Define tokens for background, surface, elevated surface, text, muted text, border, primary, accent, success, warning, danger, and focus.
- Use colour to clarify hierarchy and state, not just to decorate.
- Do a **colour role audit**: every non-neutral colour must be tagged as action, status, data category, brand memory, illustration, or atmosphere. Delete untagged colours.
- Avoid “mud”: if the palette uses many muted warm tones, add clear contrast through ink, paper, or one sharp accent; if the palette is dark, separate surfaces by luminance before adding hue.

When deriving colours from inspiration:

- Extract colour relationships, not exact hex codes: warm neutral + sharp accent, dark graphite + amber state colour, paper base + botanical action colour.
- Ask what each colour is doing: background, surface, hierarchy, action, warning, success, data category, brand memory, or atmosphere.
- Do not average colours from many references into a muddy or random palette.
- Do not copy another brand's signature palette; create a new palette with the same strategic role.
- Test colours in real UI states: hero, nav, cards, forms, disabled states, errors, success, focus rings, charts, and mobile.
- Remove decorative colours that have no semantic or atmospheric job.

Colour smell test: if the palette could fit any generic AI SaaS homepage, it is not specific enough. Replace it with colours that could only belong to this product.

## Text / Copy Choice Rules

AI-generated websites often sound polished but empty. The copy uses attractive sentence shapes without concrete meaning. Avoid text that could be pasted onto any startup homepage.

Do **not** default to:

- Vague hero lines like “Transform the way you work,” “Unlock your potential,” “Supercharge your workflow,” or “The future of productivity is here.”
- Buzzword stacks: seamless, intuitive, powerful, robust, scalable, cutting-edge, next-generation, frictionless, intelligent, effortless, unified, all-in-one, at scale.
- Generic card titles: “Fast,” “Secure,” “Reliable,” “Easy to use,” “Collaborative,” “Insights,” “Automation,” unless each is made specific.
- Fake specificity: invented metrics, unverifiable “trusted by thousands,” vague “enterprise-grade,” or testimonials from generic personas.
- Repetitive AI headline rhythm: “Plan smarter. Ship faster. Grow better.” on every section.
- Overused formulas: “Meet X, your Y for Z,” “Not just A, but B,” “Everything you need to…,” “Built for modern teams.”
- Repeated CTAs like “Get Started” and “Learn More” everywhere with no context.
- Lorem ipsum, placeholder claims, or filler paragraphs whose only job is to occupy space.
- Excessive em dashes, title-case marketing phrases, and perfectly balanced three-part lists when they make the copy feel machine-written.

Write copy deliberately:

- Start from the user’s real situation: their role, problem, anxiety, environment, and desired outcome.
- Use concrete nouns and verbs from the product domain: actual objects, workflows, files, roles, constraints, and decisions.
- Make the first screen answer: what is this, who is it for, why should they care, and what should they do next?
- Prefer proof over adjectives. Replace “powerful analytics” with what the analytics reveal, how fast, from which data, or what decision they support.
- Make headings carry information; users should understand the page by scanning headings alone.
- Give every section a distinct message. Do not repeat the hero claim in slightly different words.
- Use CTAs that describe the action: “Import your first CSV,” “Book a 12-minute demo,” “Compare plans,” “Create a test workspace.”
- Write empty states, errors, form labels, helper text, and confirmation messages as part of the design, not afterthoughts.
- Keep claims honest. If a feature is mocked, experimental, or not implemented, do not imply it exists.
- Match the voice to the product: clinical, playful, technical, luxurious, utilitarian, rebellious, calm, or editorial — but choose one intentionally.
- Vary sentence length and structure. Human copy has rhythm; AI copy often has uniformly polished cadence.
- Cut self-important lines. If a sentence sounds profound but gives no instruction, evidence, or useful emotional signal, delete it.
- Read all headings and CTAs out loud. If they sound like an ad for an unnamed SaaS product, rewrite them with product nouns.

Useful rewrites:

- Instead of “Unlock actionable insights,” say “See which invoices are overdue, disputed, or likely to miss the Friday payout.”
- Instead of “Collaborate seamlessly,” say “Comment on a claim, assign it to legal, and keep the full decision trail in one place.”
- Instead of “Get Started,” say “Create your first route,” “Upload a floor plan,” or “Start with sample data.”

Text smell test: if the copy could describe a CRM, an AI note app, a fitness dashboard, and a finance tool equally well, it is not specific enough. Rewrite until it belongs to this product only.

## Avoid Generic AI Website Aesthetics

Do not default to:

- Centered hero with generic gradient blob, glass cards, and vague SaaS copy.
- Inter/Roboto/system font everywhere with no typographic personality.
- Purple-blue gradients, neon glows, and identical rounded cards unless strongly justified.
- Repetitive sections with the same card grid rhythm.
- The same phone/browser shell, status bar, nav, rounded-card rhythm, and explanatory side panel repeated across every option.
- Preview furniture that explains the design more than the UI does: “Best for / Design move / Avoids” panels, giant option labels, mock device bezels, decorative browser chrome, or side-by-side rationale columns.
- Stock dashboard screenshots floating in a browser chrome with no product-specific idea.
- Static dashboard summaries when the task calls for a flow, editor, form, log, transaction, review, or decision screen.
- Synthetic repeated fixture data such as generic targets, fake stats, vague streaks, and interchangeable rows that do not form one believable scenario.
- Formulaic rationale labels like “Best for / Design move / Avoids” repeated inside every preview page.
- Random decorative shapes that do not reinforce the brand or content.
- Excessive animation that hides weak layout or slows the page.
- Overly smooth, sterile interfaces with no human quirks or craft.
- Safe averaged art direction: five muted palettes, five similar card stacks, five generic headings, and no single opinionated design move.

## Convert Bad-Web Patterns Into Rules

Use negative examples only to define constraints.

### Clutter and Information Overload

Bad pattern: everything competes for attention.

Rules:

- Establish one primary action per screen.
- Group related content and remove duplicate links.
- Use whitespace, type scale, and contrast to create scanning order.
- Prefer progressive disclosure over dumping all options at once.

### Weak Hierarchy

Bad pattern: headings, body text, ads, nav, and buttons have similar visual weight.

Rules:

- Create a strong type scale with clear roles.
- Make primary actions visually dominant and secondary actions quiet.
- Use contrast intentionally; not every element deserves a border, shadow, or bright color.

### Confusing Navigation

Bad pattern: too many nav items, unclear labels, buried key pages, inconsistent menus.

Rules:

- Use plain-language labels.
- Keep top-level navigation short.
- Show current location and clear next steps.
- On mobile, make navigation reachable, predictable, and keyboard/screen-reader usable.

### Unreadable Typography

Bad pattern: tiny text, long line lengths, low contrast, centered paragraphs, decorative fonts for body copy.

Rules:

- Use readable sizes and line heights.
- Keep paragraphs to comfortable line lengths.
- Reserve decorative type for display moments.
- Test contrast and readability on small screens.

### Unpleasant or Inaccessible Color

Bad pattern: random colors, low contrast, vibrating combinations, color-only status communication.

Rules:

- Define color tokens for background, surface, text, muted text, border, primary, accent, danger, success, and focus.
- Meet contrast requirements for text and controls.
- Pair color with icon/text/pattern for state.

### Dated or Careless Layout

Bad pattern: table-like pages, inconsistent alignment, crowded sidebars, mismatched components.

Rules:

- Use a modern layout system with clear grid behavior.
- Align edges deliberately.
- Keep component proportions consistent.
- Make density a design choice, not a lack of spacing.

### Hostile UX and Dark Patterns

Bad pattern: trick questions, hidden cancellation, deceptive buttons, forced signups, confusing consent, fake scarcity.

Rules:

- Be honest about consequences, price, privacy, and commitment.
- Make destructive actions confirmable and reversible when possible.
- Make opt-out, cancel, close, and back paths visible.
- Do not use shame copy, obstruction, hidden fees, or misleading visual priority.

### Mobile Failure

Bad pattern: desktop UI squeezed onto small screens, tiny tap targets, horizontal scrolling, hidden content, broken modals.

Rules:

- Design mobile structure first for complex flows.
- Use touch-friendly targets.
- Avoid fixed-width containers and offscreen controls.
- Test nav, forms, modals, sticky elements, and long content on narrow screens.

## Implementation Rules

When producing code:

- Use semantic HTML and accessible ARIA only where needed.
- Define reusable design tokens with CSS variables or the project's theme system.
- Include visible focus states and keyboard-friendly interactions.
- Respect `prefers-reduced-motion`.
- Optimize media with responsive sizing, lazy loading, and meaningful alt text.
- Provide real hover, active, disabled, loading, empty, error, and success states where relevant.
- Keep layout resilient to real content length, localization, and viewport changes.
- Avoid dependencies unless they clearly improve the result and fit the project.

## Design Brief Template

Before implementing a substantial UI, internally create a brief:

```text
Product/context:
Audience:
Primary workflow or screen state:
Real content/data available:
Tone/art direction:
Positive references studied:
Negative references avoided:
Signature design move:
Typography plan:
Color plan:
Layout grammar:
Interaction and state plan:
Scenario/data fixture plan:
Anti-template risks to avoid:
Accessibility/responsive considerations:
```

You do not always need to show the full brief to the user, but the final design should clearly reflect it.

## Final Quality Checklist

Before delivering, verify:

- The site has a distinct visual point of view.
- The first screen communicates purpose, audience, and primary action quickly.
- Typography, color, spacing, and components feel like one system.
- There is at least one memorable design move specific to the product.
- The design does not resemble a generic AI-generated SaaS template.
- The design could not be reused for an unrelated product by changing only names and colors.
- The UI contains domain-specific artifacts, labels, data, and at least one realistic state beyond the happy path when appropriate.
- Navigation and calls to action are clear.
- Forms and interactive flows are honest and usable.
- Mobile layouts are intentionally designed.
- Accessibility basics are covered.
- The UI avoids clutter, dark patterns, unreadable type, random color, hostile interactions, and repeated preview scaffolds.
