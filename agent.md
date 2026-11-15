# ONODA — Agent Context

This file is the working memory for AI agents contributing to the ONODA website.
Read it before making changes, and update it whenever the architecture, routes,
design system or conventions change.

## Project overview

ONODA is a premium martial arts academy. The site is a brochure-style marketing
website with no backend, authentication, database or API.

- **Framework:** Nuxt 4.6 (`app/` source directory)
- **UI:** Vue 3.5 Single File Components + TypeScript
- **Styling:** Tailwind CSS v4 via `@tailwindcss/vite`
- **Router:** Nuxt file-based routing (`app/pages/`)
- **Package manager:** npm

## Commands

```bash
npm run dev       # development server (http://localhost:3000)
npm run build     # production build
npm run preview   # preview a production build
npm run generate  # static generation
```

## Directory map

```text
app/
├─ app.vue                    # Root: NuxtLayout > NuxtPage
├─ assets/css/main.css        # Tailwind import, @theme tokens, global base styles
├─ components/
│  ├─ HeroSection.vue         # Homepage hero (SVG sun artwork + samurai image)
│  └─ SiteHeader.vue
    - SiteFooter.vue
├─ layouts/
│  └─ default.vue             # SiteHeader + <slot/> + SiteFooter
└─ pages/
   ├─ index.vue               # Home (HeroSection + vermilion rule)
   ├─ about.vue               # Placeholder
   ├─ classes.vue             # Placeholder
   ├─ coaches.vue             # Placeholder
   └─ contact.vue             # Placeholder
```

## Routes

| Route      | File                    | Status               |
| ---------- | ----------------------- | -------------------- |
| `/`        | `app/pages/index.vue`   | Hero implemented     |
| `/about`   | `app/pages/about.vue`   | Semantic placeholder |
| `/classes` | `app/pages/classes.vue` | Semantic placeholder |
| `/coaches` | `app/pages/coaches.vue` | Semantic placeholder |
| `/contact` | `app/pages/contact.vue` | Semantic placeholder |

`SiteHeader` and `SiteFooter` both navigate with `NuxtLink`. The hero CTA also
uses `NuxtLink` to `/classes`.

## Layout and rendering

`app/app.vue` deliberately contains only:

```vue
<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>
```

`app/layouts/default.vue` owns the shared page shell: full-height flex column,
`bg-stone text-ink`, `SiteHeader`, a flexible `<main>` with `<slot />`, and
`SiteFooter`. Do not put page content or `<NuxtPage />` in `app.vue`.

## Design system

Defined in `app/assets/css/main.css` under `@theme`. Preserve these tokens.

| Token               | Value      | Use                   |
| ------------------- | ---------- | --------------------- |
| `--color-stone`     | `#f2efe8`  | Page background       |
| `--color-ink`       | `#101010`  | Primary text          |
| `--color-vermilion` | `#e5392d`  | Accent / brand dot    |
| `--color-slate`     | `#707070`  | Secondary text        |
| `--color-mist`      | `#d9d7d1`  | Muted surfaces        |
| `--font-display`    | Bebas Neue | Headings, brand, hero |
| `--font-body`       | Inter      | Body copy             |

Conventions used in existing components:

- Tailwind utilities in templates; scoped CSS only for the hero artwork.
- Uppercase display headings, tight leading, `tracking-tight`/custom tracking.
- Small uppercase eyebrow labels: `text-xs font-semibold uppercase tracking-[0.2em] text-slate`.
- Interactive links use `hover:text-vermilion` and
  `focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-vermilion`.
- Public assets live in `public/images/`; reference them as `/images/<file>`.

## Constraints

- Preserve global CSS, Tailwind v4 configuration, colour palette and typography.
- Do not overwrite or redesign existing components; make targeted edits only.
- Do not add dependencies, backend features, auth or APIs.
- Prefer Nuxt 4 conventions and `NuxtLink` for internal navigation.
- Keep the implementation straightforward; avoid unnecessary abstractions.
- Placeholder pages are intentionally minimal — no elaborate page design yet.

## Change log

### 2026-11-15 — Multi-page architecture

Created:

- `app/layouts/default.vue` — shared shell with header, main slot and footer.
- `app/components/SiteFooter.vue` — semantic footer with ONODA brand, footer
  navigation and copyright line.
- `app/pages/index.vue` — existing homepage content (`HeroSection` + vermilion
  accent rule) moved here.
- `app/pages/about.vue` — heading, eyebrow and intro placeholder.
- `app/pages/classes.vue` — heading, eyebrow and intro placeholder.
- `app/pages/coaches.vue` — heading, eyebrow and intro placeholder.
- `app/pages/contact.vue` — heading, eyebrow and intro placeholder.
- `agent.md` — this context file.

Modified:

- `app/app.vue` — replaced the single-page shell (header + hero) with
  `NuxtLayout` wrapping `NuxtPage`.
- `app/components/HeroSection.vue` — hero CTA changed from a raw
  `<a href="/classes">` to `<NuxtLink to="/classes">`. Markup, classes, copy and
  SVG artwork are otherwise unchanged.

Unchanged:

- `app/components/SiteHeader.vue` — already used `NuxtLink` for every nav item.
- `app/assets/css/main.css` — design tokens and global styles preserved.
- `nuxt.config.ts`, `package.json`, images and other assets.

## Verification performed

- `npm run build` completes successfully on Nuxt 4.6.0.
- Production server smoke test returned HTTP 200 for `/`, `/about`, `/classes`,
  `/coaches` and `/contact`.
- Rendered HTML contains both the shared header and footer.

## Known notes / possible follow-ups

- `app/assets/css/main.css` contains a duplicated `@import "tailwindcss";`
  (lines 2 and 4). It is harmless and was left untouched to honour the
  "preserve existing global CSS" constraint. De-duplicate only if asked.
- Placeholder pages do not yet set SEO titles/descriptions.
- No test suite or linter is configured yet.
- `README.md` is still the default Nuxt starter README.
