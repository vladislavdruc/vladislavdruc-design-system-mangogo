# AGENTS.md — Design System Instructions for AI

When generating any UI code for this project, follow these rules strictly.

---

## Fonts

- `Unbounded` → ONLY for sizes 48px and above (--text-display-lg, --text-display-xl, --text-display-2xl)
- `Inter` → everything else (all body, UI, labels, buttons, inputs)
- Never hardcode font-family strings — use `var(--font-display)` or `var(--font-body)`

## Colors — NEVER hardcode hex values

Always use CSS variables:
```css
/* ✅ Correct */
color: var(--color-primary);
background: var(--color-primary-surface);
border-color: var(--color-border);

/* ❌ Wrong */
color: #EC6724;
background: #FDEFE8;
```

### Primary brand color
- Action buttons, links, active states: `var(--color-primary)` → #EC6724
- Hover: `var(--color-primary-hover)` → #C04B11
- Icon backgrounds, tinted surfaces: `var(--color-primary-surface)` → #FDEFE8
- Lightest tint: `var(--color-primary-surface-sm)` → #FFF9F6
- Accent (blue): `var(--color-accent)` → #24A9EC

### Text
- Primary text: `var(--color-text)` → #171717
- Muted/secondary: `var(--color-text-muted)` → #525252
- Faint/disabled: `var(--color-text-faint)` → #A3A3A3

### Surfaces & borders
- Page background: `var(--color-bg)` → #FFFFFF
- Card / table header bg: `var(--color-surface)` → #FAFAFA
- Borders: `var(--color-border)` → #E5E5E5

## Spacing — use 4px grid tokens only
```css
/* ✅ */
gap: var(--space-3);           /* 12px */
padding: var(--space-4);       /* 16px */
margin-bottom: var(--space-6); /* 24px */

/* ❌ */
gap: 12px;
padding: 16px;
```

## Shadows
```css
box-shadow: var(--shadow-sm);  /* cards, inputs */
box-shadow: var(--shadow-md);  /* dropdowns */
box-shadow: var(--shadow-lg);  /* modals, tooltips */
```

## Border radius
```css
border-radius: var(--radius-md);   /* 8px — buttons, inputs, badges */
border-radius: var(--radius-xl);   /* 12px — cards, modals, tables */
border-radius: var(--radius-full); /* pill — badges, avatars */
```

## Components — use existing classes

Do NOT reinvent components. Use the classes from these files:

| Need | Class | File |
|---|---|---|
| Button | `.btn .btn--primary` | buttons.css |
| Input | `.input` | inputs.css |
| Badge | `.badge .badge--brand` | badges.css |
| Checkbox | `.checkbox` | checkbox.css |
| Toggle | `.toggle` | toggle.css |
| Dropdown | `.dropdown` | dropdown.css |
| Tooltip | `.tooltip` | tooltip.css |
| Toast | `.toast` | toast-alert.css |
| Alert | `.alert` | toast-alert.css |
| Loader | `.spinner` `.skeleton` | loader.css |
| Navbar | `.navbar` | navbar.css |
| Footer | `.footer` | footer.css |
| Pagination | `.pagination` | pagination.css |
| Table | `.table-card .table` | table.css |
| Modal | `.modal .modal-overlay` | modal-popup.css |
| Popup | `.popup` | modal-popup.css |

## Transitions
```css
transition: color var(--transition-base), background var(--transition-base);
```

## Grid
```html
<div class="container">
  <div class="grid-12">
    <div class="col-6">...</div>
    <div class="col-6">...</div>
  </div>
</div>
```
