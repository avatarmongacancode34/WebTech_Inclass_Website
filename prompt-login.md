# Prompt: Login Page (`login.html`)

Copy everything below the line into Claude. Put `styles.css` and `CLAUDE.md` in the same folder or attach them first.

---

Read `CLAUDE.md` and `styles.css` first. Build `login.html`, the sign-in page of the Ashesi University website, using only the existing classes in `styles.css`. Do not create new CSS files and do not use inline styles or `<style>` blocks. If a style is missing, tell me the exact CSS to add to `styles.css` and which numbered section it belongs in.

**Layout:**
- Navbar (markup from CLAUDE.md; `is-active` is not needed on any link).
- `.auth` wrapper containing `.auth__card` with `.auth__title` ("Welcome back") and `.auth__subtitle` ("Log in to access your dashboard").

**Form fields** (each with a `<label class="form-label">` linked by `for`/`id`):
- Email or student ID (`.form-input`, `autocomplete="username"`)
- Password (`.form-input`, `type="password"`, `autocomplete="current-password"`)
- Row with a `.form-check` "Remember me" checkbox on the left and a "Forgot password?" link on the right (use `.cluster.cluster--between`)
- Submit button: `.btn.btn--primary.btn--block` labelled "Log in"
- An `.alert.alert--danger.hidden` block above the form for error messages (remove `.hidden` to show it)
- `.auth__footer`: "New to Ashesi? Create an account" linking to `register.html`

**Behaviour:** use `required` on both fields. There is no backend yet, so add an HTML comment where the form `action` will go. For demo purposes only, a small `<script>` may send the user to `dashboard.html` on submit; clearly label that script as a temporary placeholder to be replaced by real authentication. Never hard-code real credentials.

**Rules:** unique `<title>` ending in `| Ashesi`, meta description, responsive down to 375px, accessible labels and keyboard navigation.
