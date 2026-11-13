# Prompt: Contact Page (`contact.html`)

Copy everything below the line into Claude. Put `styles.css` and `CLAUDE.md` in the same folder or attach them first.

---

Read `CLAUDE.md` and `styles.css` first. Build `contact.html`, the Contact page of the Ashesi University website, using only the existing classes in `styles.css`. Do not create new CSS files and do not use inline styles or `<style>` blocks. If a style is missing, tell me the exact CSS to add to `styles.css` and which numbered section it belongs in.

**Page sections, in order:**
1. Navbar (markup from CLAUDE.md, `is-active` on Contact).
2. Compact hero (`.hero.hero--compact`): "Contact us" with a one-sentence `.lead`.
3. Main section with a `.grid--2`:
   - **Left:** a `.card` containing the contact form. Fields (each with a linked `<label class="form-label">`): full name and email (`.form-row`), subject (`.form-select` with options such as Admissions, Academics, Careers, Other), message (`.form-textarea`), and a submit button `.btn.btn--primary` labelled "Send message". Add an `.alert.alert--success.hidden` block for the confirmation message.
   - **Right:** a `.stack` of `.card` items for contact details (address, phone, email, office hours). Use clearly marked placeholders in square brackets; do not invent real contact details.
4. Map placeholder: a `.card` with a text note and an HTML comment showing where an embedded map `<iframe>` would go.
5. FAQ strip (`.section--alt`): three short Q&A `.card` items in `.grid--3`.
6. Footer (same as the other pages).

**Behaviour:** native validation (`required`, `type="email"`). No backend yet; add an HTML comment where the form `action` will go. An optional small `<script>` may remove `.hidden` from the success alert and reset the form on submit.

**Rules:** unique `<title>` ending in `| Ashesi`, meta description, responsive down to 375px, accessible labels. List every placeholder I need to replace at the end.
