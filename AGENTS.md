# Codex Project Instructions

- This is a Hugo Blox / Tailwind personal site.
- Before changing Hugo Blox blocks, home sections, CSS, icons, or collection behavior, read `CUSTOMIZATION_GUIDE.md`.
- Keep blocks focused on structure, styling, and rendering logic. Put text and data in `content/**/_index.md` or page front matter.
- Style priority: Tailwind utility classes first, block-local `<style>` for complex selectors or animations, and `assets/css/custom.css` only for shared global CSS.
- New custom blocks default to `layouts/partials/hbx/blocks/*-custom/block.html`.
- Verify site changes with `npm run build`; use `npm run dev` for local preview.
- Do not create or modify files solely to save assistant working notes. Provide working notes in chat unless the user explicitly asks for a file.
