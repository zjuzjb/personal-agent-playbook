# UI Acceptance Template

Use this for UI and interaction acceptance. Adapt product-specific language in a
project adapter.

## Required Inputs

- Exact URL, page, state, and viewport.
- Desktop viewport around the target product width.
- Narrow viewport when layout may change.
- Affected flows or tabs, not only one screenshot.
- Before/after screenshots when visual quality is the target.

## Visual Gate

Check:

- Typography: clear hierarchy, no unnecessary bolding or oversized text.
- Spacing: no accidental large gaps, clipped sections, or crowded controls.
- Layout: columns, cards, navigation, and sticky elements align predictably.
- Color: palette supports content rather than overwhelming it.
- Borders and shadows: restrained and consistent.
- Icons: purposeful, aligned, and balanced with labels.
- Density: concise and scannable for the task.
- Responsiveness: no overlap, horizontal clipping, or hidden primary actions.

## Interaction Gate

Check:

- Loading, empty, error, hover, focus, and active states.
- Sticky elements do not cover content.
- Buttons and controls have clear purpose.
- Feedback appears near the content it concerns.
- Navigation and scroll behavior remain usable on long content.

## Failure Patterns

- Text overlaps, clips, or sits under sticky headers.
- Large empty spaces appear accidentally.
- A visual fix works only for one screenshot.
- Controls resize or shift unexpectedly.
- Important evidence or context disappears.

