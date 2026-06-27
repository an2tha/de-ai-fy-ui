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
- **Purposeful hierarchy:** Users can tell what matters in under five seconds.
- **Original art direction:** Typography, color, layout, and motion fit the product's personality.
- **Responsive craft:** Mobile, tablet, and desktop are designed, not merely squeezed.
- **Accessible interaction:** Semantic HTML, keyboard states, focus states, readable contrast, reduced-motion support.
- **Trustworthy UX:** No deceptive flows, hidden controls, confusing opt-outs, bait-and-switch pricing, or manipulative consent.
- **Production polish:** Real content, robust states, consistent spacing, clean code, performance-aware assets.

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

- Start from the product's world: materials, audience, industry, geography, photography, physical environment, or emotional tone.
- Choose a dominant background/surface family first, then text, borders, accents, and semantic states.
- Use one primary accent with restraint; add secondary accents only when they have a job.
- Make neutrals characterful: warm ivory, graphite, bone, ink, clay, fog, metal, charcoal, paper, or other context-specific bases.
- Control saturation. Most mature palettes mix muted foundations with sharp accent moments.
- Ensure contrast for body text, small labels, controls, and focus states.
- Make light and dark themes feel designed separately; do not simply invert colours.
- Define tokens for background, surface, elevated surface, text, muted text, border, primary, accent, success, warning, danger, and focus.
- Use colour to clarify hierarchy and state, not just to decorate.

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
- Stock dashboard screenshots floating in a browser chrome with no product-specific idea.
- Random decorative shapes that do not reinforce the brand or content.
- Excessive animation that hides weak layout or slows the page.
- Overly smooth, sterile interfaces with no human quirks or craft.

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
Tone/art direction:
Positive references studied:
Negative references avoided:
Signature design move:
Typography plan:
Color plan:
Layout grammar:
Motion plan:
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
- Navigation and calls to action are clear.
- Forms and interactive flows are honest and usable.
- Mobile layouts are intentionally designed.
- Accessibility basics are covered.
- The UI avoids clutter, dark patterns, unreadable type, random color, and hostile interactions.
