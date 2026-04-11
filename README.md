# Design System

Brand: **#EC6724** (Brand/500 — Оранжевый)  
Accent: **#24A9EC** (Complimentary/Blue)  
Display font: **Unbounded** (48px+)  
Body/UI font: **Inter** (all other sizes)

---

## Быстрый старт

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="design-system/index.css">
```

---

## Структура

```
design-system/
├── index.css                  ← подключи только этот файл
├── tokens/
│   ├── colors.css             ← вся палитра + семантические алиасы
│   ├── typography.css         ← шрифты, размеры, line-height
│   ├── spacing.css            ← 4px grid (--space-1 → --space-32)
│   ├── radius.css             ← --radius-xs → --radius-full
│   ├── shadows.css            ← --shadow-xs → --shadow-3xl + blurs
│   └── grid.css               ← 12/6 колонок + .container
├── base/
│   ├── fonts.css              ← @import Google Fonts
│   └── reset.css              ← CSS reset
├── components/
│   ├── badges.css             ← .badge (все цвета и размеры)
│   ├── badge-group.css        ← .badge-group
│   ├── buttons.css            ← .btn (primary/secondary/ghost/link, все размеры)
│   ├── inputs.css             ← .input, .input-group, .input-label
│   ├── checkbox.css           ← .checkbox, .checkbox-group
│   ├── toggle.css             ← .toggle (sm/md/lg)
│   ├── dropdown.css           ← .dropdown, .dropdown-item
│   ├── tooltip.css            ← .tooltip (top/bottom/left/right)
│   ├── toast-alert.css        ← .toast, .alert (все статусы)
│   ├── loader.css             ← .spinner, .skeleton
│   ├── navbar.css             ← .navbar (desktop + mobile burger)
│   ├── footer.css             ← .footer (desktop + mobile)
│   ├── pagination.css         ← .pagination, .pagination-dots
│   ├── table.css              ← .table-card (desktop + mobile accordion)
│   └── modal-popup.css        ← .modal, .modal-overlay, .popup
└── AGENTS.md                  ← инструкция для AI/вайбкодинга
```

---

## Цветовая палитра

| Токен | Hex | Применение |
|---|---|---|
| `--color-primary` | `#EC6724` | Кнопки, акценты, активные состояния |
| `--color-primary-hover` | `#C04B11` | Hover на primary |
| `--color-primary-surface` | `#FDEFE8` | Фоны иконок, выделений |
| `--color-accent` | `#24A9EC` | Дополнительный акцент (синий) |
| `--color-text` | `#171717` | Основной текст |
| `--color-text-muted` | `#525252` | Вспомогательный текст |
| `--color-border` | `#E5E5E5` | Границы компонентов |
| `--color-surface` | `#FAFAFA` | Фон таблиц, хедеров |

## Типографика

| Размер | Токен | Шрифт | Применение |
|---|---|---|---|
| 72px | `--text-display-2xl` | **Unbounded** | Hero заголовки |
| 60px | `--text-display-xl` | **Unbounded** | Крупные заголовки |
| 48px | `--text-display-lg` | **Unbounded** | Заголовки секций |
| 36px | `--text-display-md` | Inter | Подзаголовки |
| 30px | `--text-display-sm` | Inter | |
| 24px | `--text-display-xs` | Inter | |
| 20px | `--text-xl` | Inter | Lead text |
| 18px | `--text-lg` | Inter | Заголовки карточек |
| 16px | `--text-md` | Inter | Основной текст (body) |
| 14px | `--text-sm` | Inter | UI, кнопки, подписи |

> **Правило:** Unbounded — строго для 48px+. Inter — всё остальное.

---

## Для AI / вайбкодинга

Смотри `AGENTS.md` — там правила использования токенов для генерации кода.
