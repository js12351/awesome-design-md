# Zernio Inspired Design System

Use this design direction for developer-first SaaS, API platforms, automation tools, and AI-agent products that should feel fast, practical, warm, and technically credible.

This is a Zernio-inspired system, not a clone. Do not copy Zernio logos, proprietary illustrations, screenshots, badges, partner marks, exact page composition, or marketing copy unless the user supplies those assets. Translate the visual language into reusable product UI decisions.

## Visual Character

- Lead with utility and momentum: compact navigation, direct headlines, visible API/code examples, proof metrics, and dense but readable product sections.
- Favor a warm off-white canvas with charcoal text and a sharp coral primary accent.
- Make the interface feel slightly editorial but still tool-like: large confident type, monospace/code surfaces, crisp borders, and understated cards.
- Keep surfaces mostly flat. Use borders, subtle translucency, and small glows instead of heavy shadows.
- Use social/API product cues such as endpoint rows, platform chips, OAuth steps, stat sparklines, and code panels.

## Palette

Core tokens:

```css
:root {
  --zernio-coral: #eb3514;
  --zernio-coral-muted: #e09282;
  --zernio-burgundy: #660202;
  --zernio-burgundy-muted: #a57070;
  --zernio-charcoal: #2d2d2d;
  --zernio-charcoal-muted: #6b6b6b;
  --zernio-cream: #f0efeb;
  --zernio-cream-muted: #d9d8d3;
  --zernio-success: #22c55e;
  --zernio-purple: #8b5cf6;
}
```

Usage:

- Page background: `--zernio-cream`.
- Primary text: `--zernio-charcoal`.
- Secondary text: `--zernio-charcoal-muted`.
- Primary buttons, banners, active states, progress indicators, link accents: `--zernio-coral`.
- Borders and separators: `--zernio-cream-muted`, usually at 1px.
- Use success green and purple only for metrics, sparklines, platform/account indicators, and small data accents.
- Avoid large gradients. If glow is needed, use a restrained coral glow such as `0 0 20px rgba(235, 53, 20, 0.3)`.

## Typography

- Primary font: Geist Sans.
- Fallback stack: `Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif`.
- Code and technical UI: `Menlo, Consolas, Monaco, "Liberation Mono", "Courier New", monospace`.
- Body pages may use a monospace-forward feel for product/API credibility, but keep long-form paragraphs in the sans stack when readability matters.
- Headlines should be bold, compact, and direct. Use tight line-height without negative letter spacing.
- Labels, nav items, chips, badges, file names, API routes, and code blocks should lean monospace.

Suggested scale:

```css
.hero-title {
  font-size: clamp(3rem, 7vw, 6.5rem);
  line-height: 0.94;
  font-weight: 800;
}

.section-title {
  font-size: clamp(2rem, 4vw, 4.5rem);
  line-height: 1;
  font-weight: 800;
}

.body {
  font-size: 1rem;
  line-height: 1.625;
}
```

## Layout

- Use a max content width around `80rem`.
- Page padding: `1.5rem` on mobile, `4rem` on large screens.
- Section gaps: `5rem` mobile, `7rem` desktop.
- Favor two-column hero layouts where the product promise sits beside a realistic code/API panel.
- Keep hero content immediately useful: headline, short supporting copy, primary CTA, no-credit-card or setup-time note, and a code example or product proof.
- Use sticky, translucent cream navigation with subtle backdrop blur.
- Let platform/product grids be dense, icon-led, and scannable.
- Include proof sections as compact logos, metrics, testimonials, or endpoint cards rather than oversized decorative cards.

## Components

### Announcement Bar

- Full-width coral strip.
- White text, small type, compact vertical padding.
- Optional white badge with coral text for status labels like `NEW`.
- Keep the entire bar clickable when it announces a product update.

### Navigation

- Sticky top navigation over cream.
- Use `backdrop-filter: blur(12px)` with `background: rgba(240, 239, 235, 0.85)`.
- Logo area at left, grouped nav links in the middle, CTA at right.
- Nav text should be small, practical, and calm. Avoid oversized marketing navigation.

### Buttons

- Primary: coral background, white text, 8px radius, medium-bold label.
- Secondary: cream or transparent background, charcoal text, 1px muted cream border.
- Keep buttons compact but comfortable: `0.75rem 1rem` for standard controls, `0.875rem 1.25rem` for hero CTAs.
- Use hover states that darken coral slightly or add a coral-tinted border/glow.

### Cards and Panels

- Radius: 8px to 12px.
- Border: 1px solid muted cream or low-opacity charcoal.
- Background: cream, white with low opacity, or charcoal for code.
- Avoid nested cards. Use dividers and rows inside panels.
- Code panels should have a filename/tab header, language label, dark or charcoal-tinted body, monospace text, and coral highlights for important tokens.

### Chips and Endpoint Rows

- Use small pill or rounded-rectangle chips for platforms, API methods, and statuses.
- Endpoint rows should combine method, path, one-line description, and optional link arrow.
- Method labels can use coral, green, purple, or charcoal depending on semantic role.

### Metrics

- Use compact statistic rows with tiny status dots and optional sparklines.
- Prefer real product proof numbers, weekly activity, connected accounts, or API uptime.
- Keep metric labels understated and text-muted.

## Motion

- Keep motion brief and functional: 150ms to 300ms transitions.
- Use subtle opacity, translate, and border-color transitions.
- Sparklines may animate line drawing and moving dots.
- Avoid bouncy, playful, or overly cinematic animation.

## Implementation Notes

- Use the Zernio palette as tokens first, then map into the target app's theme system.
- Preserve the target app's UX and information architecture; apply this style to the presentation layer.
- Do not overuse coral. It should punctuate the page, not flood it.
- Do not make the design monochrome cream/coral. Use charcoal structure, muted borders, and small green/purple data accents to keep the page dimensional.
- For dashboards, invert the emphasis: cream shell, charcoal/white panels, coral actions, and compact monospace metadata.

