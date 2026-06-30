# Codex Project Instructions

- This is a Hugo Blox / Tailwind personal site.
- For content-only updates, edit the relevant files under `content/`, `content-zh/`, or `static/`.
- Before changing Hugo Blox blocks, home sections, CSS, icons, or collection behavior, read `CUSTOMIZATION_GUIDE.md`.
- Keep blocks focused on structure, styling, and rendering logic. Put text and data in `content/**/_index.md` or page front matter.
- Style priority: Tailwind utility classes first, block-local `<style>` for complex selectors or animations, and `assets/css/custom.css` only for shared global CSS.
- New custom blocks default to `layouts/partials/hbx/blocks/*-custom/block.html`.
- Verify site changes with `npm run build`; use `npm run dev` for local preview.
