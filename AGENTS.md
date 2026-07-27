# AGENTS.md

This document provides an overview of the project structure for developers and AI agents working on this codebase.

## Project Overview

A marketing/product showcase site listing products with detail pages, built with TanStack Start and deployed on Netlify.

### Tech Stack

| Layer | Technology |
|-------|------------|
| Framework | TanStack Start |
| Frontend | React 19, TanStack Router v1 |
| Build | Vite 7 |
| Styling | Tailwind CSS 4 |
| Language | TypeScript |
| Deployment | Netlify |

## Directory Structure

```
├── public/                     # Static assets (favicon, images)
├── src/
│   ├── data/
│   │   └── products.ts         # Product data source
│   ├── routes/
│   │   ├── __root.tsx          # Root document shell (head, html/body)
│   │   ├── index.tsx           # Home page — product listing
│   │   └── products/
│   │       └── $productId.tsx  # Product detail page (dynamic route)
│   ├── router.tsx               # Router configuration
│   └── styles.css               # Global styles / Tailwind entry
├── netlify.toml                 # Netlify build/deploy configuration
└── vite.config.ts               # Vite + plugin configuration
```

## Conventions

- Routes are file-based under `src/routes/` using TanStack Router's `createFileRoute`.
- Product data currently lives in `src/data/products.ts` as a static array; replace with a real data source (e.g. Netlify Database) if the catalog needs to grow or be editable.
- Styling uses Tailwind utility classes directly in components.

## Development Commands

```bash
pnpm dev      # Start dev server
pnpm build    # Production build
```
