# Ashesi Website — Project Guide (CLAUDE.md)

Read this before writing or editing any page. It explains the shared stylesheet so every page looks like one website.

## Project rules

- **One stylesheet only: `styles.css`.** Every page links it with `<link rel="stylesheet" href="styles.css">`.
- **No page-specific CSS files, no `<style>` blocks, no inline styles** (the dashboard has one small exception on the logout button).
- Plain **HTML + CSS only**. No frameworks. No JavaScript unless your page truly needs it (form validation is the usual case; keep it in a `<script>` at the bottom of your page).
- If you need a style that does not exist, **add it to `styles.css` in the matching numbered section**, follow the naming rules below, and add a line to the component list in this file.
- Always use the CSS variables (`var(--color-primary)`) instead of hard-coded colours or spacing.

## File map

| File | Owner | Purpose |
|------|-------|---------|
| `styles.css` | Everyone | The single shared stylesheet |
| `index.html` | Home page owner | Landing page |
| `about.html` | About page owner | About Ashesi |
| `register.html` | Registration owner | Sign-up form |
| `login.html` | Login owner | Sign-in form |
| `contact.html` | Contact owner | Contact form and details |
| `dashboard.html` | Dashboard owner | Logged-in student dashboard |
| `prompts/` or `prompt-*.md` | — | Prompts to give Claude for each page |

Page links between files are relative: `index.html`, `about.html`, `register.html`, `login.html`, `contact.html`, `dashboard.html`.

## Naming convention (BEM-lite)

- Block: `.card`, `.navbar`, `.auth`
- Element: `.card__title`, `.navbar__link` (double underscore)
- Modifier: `.btn--primary`, `.badge--success` (double dash)
- State: `.is-active`, `.is-invalid`

## Design tokens (`:root` variables)

| Group | Variables |
|-------|-----------|
| Brand | `--color-primary` (maroon), `--color-primary-dark`, `--color-primary-light`, `--color-accent` (gold), `--color-accent-light` |
| Neutrals | `--color-ink`, `--color-muted`, `--color-border`, `--color-bg`, `--color-surface` |
| Status | `--color-success`, `--color-warning`, `--color-danger`, `--color-info` (each has a `-light` version) |
| Fonts | `--font-sans` (body), `--font-heading` (serif headings) |
| Spacing | `--space-1` (0.25rem) to `--space-8` (4.5rem) |
| Shape | `--radius-sm`, `--radius`, `--radius-lg`, `--radius-pill`, `--shadow-sm`, `--shadow`, `--shadow-lg` |
| Layout | `--container-width`, `--sidebar-width`, `--topbar-height` |

## Components available in `styles.css`

### Layout
- `.container` — centred max-width wrapper. Put inside every section.
- `.section`, `.section--alt` (white bg), `.section--tint` (light maroon bg), `.section__header` (centred intro block)
- `.grid` with `.grid--2`, `.grid--3`, `.grid--4` — responsive columns (collapse on mobile)
- `.stack` / `.stack--lg` — vertical spacing between children
- `.cluster` / `.cluster--between` — horizontal flex row with gaps

### Typography
- `h1`–`h4` are styled globally. `.lead` (intro paragraph), `.eyebrow` (small caps label above a heading), `.text-muted`, `.text-small`

### Buttons
- `.btn` + one of `.btn--primary`, `.btn--accent`, `.btn--outline`, `.btn--ghost`
- Sizes: `.btn--sm`, `.btn--lg`. Full width: `.btn--block`

### Navbar and footer (use on public pages)
```html
<header class="navbar">
  <div class="container navbar__inner">
    <a href="index.html" class="navbar__brand"><span class="navbar__mark">A</span> Ashesi</a>
    <nav class="navbar__links">
      <a href="index.html" class="navbar__link is-active">Home</a>
      <a href="about.html" class="navbar__link">About</a>
      <a href="contact.html" class="navbar__link">Contact</a>
      <a href="login.html" class="btn btn--outline btn--sm">Log in</a>
      <a href="register.html" class="btn btn--primary btn--sm">Register</a>
    </nav>
  </div>
</header>
```
Put `is-active` on the link for the current page. The footer uses `.footer`, `.footer__grid`, `.footer__links`, `.footer__bottom`. **Copy the same navbar and footer onto every public page.**

### Hero
- `.hero` (maroon gradient), `.hero--compact` (shorter, for inner pages), `.hero__actions` (button row)

### Cards, badges, avatars
- `.card` with `.card--hover`, `.card__header`, `.card__title`
- `.badge` with `--success`, `--warning`, `--danger`, `--info`
- `.avatar` with `--sm`, `--lg`

### Forms
- `.form-group` wraps label + field. `.form-row` puts two fields side by side.
- `.form-label`, `.form-input`, `.form-select`, `.form-textarea`
- `.form-hint`, `.form-error`, `.form-check` (checkbox/radio row), `.is-invalid` on an input

### Auth pages (login and registration)
- `.auth` (full-height centred backdrop) > `.auth__card` (or `.auth__card--wide`) containing `.auth__title`, `.auth__subtitle`, a form, and `.auth__footer`

### Tables, progress, alerts
- `.table-wrap` > `.table` (scrolls sideways on mobile)
- `.progress` > `.progress__bar` (set width inline, e.g. `style="width:60%"`); variants `--accent`, `--success`
- `.alert` with `--success`, `--warning`, `--danger`, `--info`

### Dashboard (only `dashboard.html`)
- `.dash` > `.dash__toggle-input`, `.dash__sidebar`, `.dash__main`
- Sidebar: `.dash__brand`, `.sidebar-nav__group`, `.sidebar-nav__label`, `.sidebar-nav__link` (+ `.is-active`), `.sidebar-nav__icon`, `.dash__sidebar-footer`
- Top bar: `.dash__topbar`, `.dash__menu-btn`, `.dash__search`, `.dash__user`
- Content: `.dash__content`, `.dash__layout` (2/3 + 1/3 columns), `.dash__col`
- Widgets: `.welcome`, `.stat-card` (+ `__icon`, `__value`, `__label`), `.list-item` (+ `__body`, `__title`, `__meta`), `.schedule-time`, `.course-progress`
- The mobile menu works with a hidden checkbox (`#sidebar-toggle`) and a `<label for="sidebar-toggle">`. No JS required.

### Utilities
`.text-center`, `.text-right`, `.mt-0/4/6`, `.mb-0/4/6`, `.w-full`, `.hidden`, `.sr-only`

## Page checklist

Every page must have:
1. `<!DOCTYPE html>`, `<html lang="en">`, `<meta charset>` and `<meta name="viewport">`
2. A unique `<title>` ending in `| Ashesi` and a meta description
3. `<link rel="stylesheet" href="styles.css">`
4. Semantic tags (`header`, `nav`, `main`, `section`, `footer`)
5. Labels on every form field, alt text on every image
6. Works at phone width (test at 375px) and desktop width

## Branding note

Colours here are a maroon-and-gold scheme chosen to suit Ashesi. Swap in the official brand colours by editing the variables at the top of `styles.css`; every page updates at once. Do not add the official logo or photos unless the team has permission to use them.
