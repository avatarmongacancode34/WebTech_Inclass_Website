# Prompt: Home Page (`index.html`)

Copy everything below the line into Claude. Put `styles.css` and `CLAUDE.md` in the same folder or attach them first.

---

Read `CLAUDE.md` and `styles.css` first. Build `index.html`, the home page of the Ashesi University website, using only the existing classes in `styles.css`. Do not create new CSS files and do not use inline styles or `<style>` blocks. If a style is missing, tell me the exact CSS to add to `styles.css` and which numbered section it belongs in.

**Page sections, in order:**
1. Navbar (copy the markup from CLAUDE.md, `is-active` on Home).
2. Hero (`.hero`): headline about shaping ethical, entrepreneurial leaders in Africa, a short `.lead` paragraph, and two buttons in `.hero__actions`: "Register now" (`.btn--accent`, links to `register.html`) and "Learn more" (`.btn--outline`, links to `about.html`).
3. Key figures: four `.card` items in `.grid--4` (e.g. students, countries represented, majors, years since founding). Use placeholder numbers and mark them clearly as placeholders in an HTML comment.
4. "Why Ashesi" section (`.section--alt`): `.section__header` plus three `.card--hover` cards in `.grid--3` (Liberal arts education, Ethics and leadership, Entrepreneurship).
5. Programmes section: a `.grid--2` of cards, each with a `.badge`, a title, short text, and a `.btn--ghost` link.
6. Call-to-action band (`.section--tint`): heading, one sentence, `.btn--primary` to `register.html`.
7. Footer (copy from CLAUDE.md pattern: brand, quick links, contact links, copyright).

**Rules:** semantic HTML, a unique `<title>` ending in `| Ashesi`, a meta description, responsive down to 375px, and no JavaScript. Use realistic but generic copy; do not invent statistics and do not use the official logo or photos.

When finished, list any placeholder content I need to replace.
