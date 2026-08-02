# Portfolio — Sumedh Nikalje

Personal portfolio site. Single page, no build step, no dependencies beyond Google Fonts.

## Structure

```
index.html          entire site — markup, styles, and scripts
assets/img/         favicon and touch icon
```

## Running locally

Open `index.html` in a browser, or serve it:

```bash
python3 -m http.server 8000
```

## Editing

All content lives in `index.html`.

- **Palette** — defined once in the `:root` block at the top of the `<style>` tag.
  `--cyan` is the primary accent, `--coral` the secondary. Change those two to retheme.
- **Hero diagram** — hand-written SVG inside `.diagram`. Boxes are `<rect class="node">`
  with two `<text>` labels each; connectors are `<path class="edge">`. The `.flow` paths
  are duplicates of the edges that carry the animated packets. Edit the coordinates to
  show a different system.

Update before sharing:

- `hello@example.com` in the contact section
- the LinkedIn and GitHub `href="#"` placeholders in the contact section

## Notes

- Responsive down to mobile, visible keyboard focus, `prefers-reduced-motion` respected.
- Scroll reveals use `IntersectionObserver`; the diagram draws itself in via the Web Animations API.
- No contact form. Static hosts can't run PHP — use [Formspree](https://formspree.io)
  or a `mailto:` link if you want one.
