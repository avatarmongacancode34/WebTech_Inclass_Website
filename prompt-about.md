# Prompt: About Page (`about.html`)

Copy everything below the line into Claude. Put `styles.css` and `CLAUDE.md` in the same folder or attach them first.

---

Read `CLAUDE.md` and `styles.css` first. Build `about.html`, the About page of the Ashesi University website, using only the existing classes in `styles.css`. Do not create new CSS files and do not use inline styles or `<style>` blocks. If a style is missing, tell me the exact CSS to add to `styles.css` and which numbered section it belongs in.

**Page sections, in order:**
1. Navbar (markup from CLAUDE.md, `is-active` on About).
2. Compact hero (`.hero.hero--compact`) with the title "About Ashesi" and a one-sentence `.lead`.
3. Our story: a `.grid--2` with the story text on the left (use `.eyebrow`, `h2`, paragraphs) and a `.card` on the right with three quick facts.
4. Mission and vision: two `.card` items in `.grid--2`.
5. Core values: four `.card--hover` items in `.grid--4`.
6. Leadership: three or four cards in a grid, each with an `.avatar.avatar--lg` showing initials, a name, a role, and one line of text. Use clearly marked placeholder names.
7. Call-to-action band (`.section--tint`) linking to `register.html` and `contact.html`.
8. Footer (same as the other pages).

**Rules:** semantic HTML, a unique `<title>` ending in `| Ashesi`, a meta description, responsive down to 375px, and no JavaScript. Do not invent historical facts, dates, or statistics. Where a fact is needed, use a placeholder in square brackets and list all of them for me at the end so I can replace them from official sources.
