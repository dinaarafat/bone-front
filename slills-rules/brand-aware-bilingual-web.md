# Brand-aware bilingual web UI rules

Use these rules when creating or updating a website or web app. Adapt to the project's existing framework, components, conventions, and design system; do not replace or scaffold an existing app unnecessarily.

## Arabic and English

- Provide complete Arabic and English UI translations. Use the project's localization system; if none exists, use a small, clear translation dictionary instead of scattering language conditionals.
- Set the document language and direction whenever the language changes: English uses `en`/`ltr`, Arabic uses `ar`/`rtl`.
- Make the language control keyboard accessible, clearly labeled, and usable in both languages. Persist the selection when appropriate.
- Use RTL-aware layout and CSS logical properties. Check navigation order, icons, punctuation, forms, and mixed-direction text; do not implement RTL by merely right-aligning the page.

## Fully responsive

- Make every page and interaction usable from narrow mobile screens through tablets and large desktop displays.
- Reflow content, navigation, controls, and grids at suitable breakpoints. Avoid horizontal overflow, clipped content, and hover-only interactions.
- Test at narrow mobile, tablet, and desktop viewport sizes in both LTR and RTL.

## Supplied logo and brand identity

- Inspect the project and user-provided assets for the official logo and brand guidance before choosing colors, typography, shapes, or imagery.
- Use the supplied logo and derive a consistent palette and visual style from its actual brand colors. Define reusable design tokens and use them consistently across pages and components.
- Preserve the official logo asset and proportions. Do not invent a replacement logo or claim an unprovided color is an official brand color.
- If no logo or brand guidance can be found, ask the user before asserting exact branding. Continue only with an explicitly approved temporary treatment when appropriate.
- Check readable contrast in every theme; use brand accents without sacrificing legibility.

## Light and dark themes

- Provide an accessible light/dark theme toggle unless the project or user explicitly rules it out.
- Apply theme tokens consistently across the complete interface, label the control for assistive technology, and persist the user's choice when appropriate.

## Accessibility and validation

- Use semantic structure, visible keyboard focus, accessible names, and reduced-motion support where motion is used.
- Follow existing project patterns and make the smallest coherent change. Avoid adding dependencies when the existing stack can meet the requirements.
- Verify language switching updates translated content and `lang`/`dir`; verify theme switching, contrast, and persistence; inspect responsive layouts in both directions. Run the smallest relevant existing checks and report anything that could not be run.

## Completion checklist

- [ ] English and Arabic content is complete, and switching updates language and direction.
- [ ] Layout and controls work without overflow on mobile, tablet, and desktop in LTR and RTL.
- [ ] The actual supplied logo and its brand palette guide the visual design consistently.
- [ ] Light and dark themes are usable and the toggle is accessible.
- [ ] Relevant tests or browser checks cover the behaviors above.
