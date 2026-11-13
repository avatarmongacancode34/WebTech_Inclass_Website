# Prompt: Registration Page (`register.html`)

Copy everything below the line into Claude. Put `styles.css` and `CLAUDE.md` in the same folder or attach them first.

---

Read `CLAUDE.md` and `styles.css` first. Build `register.html`, the student registration page of the Ashesi University website, using only the existing classes in `styles.css`. Do not create new CSS files and do not use inline styles or `<style>` blocks. If a style is missing, tell me the exact CSS to add to `styles.css` and which numbered section it belongs in.

**Layout:**
- Navbar (markup from CLAUDE.md; no link is `is-active`, or highlight "Register" if you add one).
- `.auth` wrapper containing `.auth__card.auth__card--wide` with `.auth__title` ("Create your account") and `.auth__subtitle`.
- Footer is optional on this page; if you include it, copy it from the other pages.

**Form fields** (every field needs a `<label class="form-label">` linked by `for`/`id`, and a `.form-input`, `.form-select` or `.form-textarea`):
- First name and last name (side by side in `.form-row`)
- Email address and phone number (`.form-row`)
- Date of birth and gender (`.form-row`)
- Country (select) and intended major (select)
- Entry year (select)
- Password and confirm password (`.form-row`) with a `.form-hint` explaining the rules (at least 8 characters)
- A `.form-check` checkbox: "I agree to the terms and privacy policy"
- Submit button: `.btn.btn--primary.btn--block` labelled "Create account"
- `.auth__footer`: "Already have an account? Log in" linking to `login.html`

**Behaviour:** use native HTML validation (`required`, `type="email"`, `minlength`, `pattern`). Optionally add a small `<script>` at the bottom that checks the two passwords match, adds `.is-invalid` to the field, and shows a `.form-error` message. On success, redirect to `login.html`. No backend is needed; add an HTML comment where the form `action` will go later.

**Rules:** unique `<title>` ending in `| Ashesi`, meta description, responsive down to 375px, accessible labels and keyboard navigation. Never store or log passwords in the script.
