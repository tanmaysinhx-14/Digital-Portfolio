# Tanmay — Digital Portfolio

Personal portfolio built with Next.js 16 and Bootstrap 5. Showcases projects in computer vision, backend development, and frontend implementation through a responsive single-page layout.

## Tech Stack

- **Framework:** Next.js 16 (App Router, Turbopack)
- **UI:** React 19, Bootstrap 5, custom CSS
- **Font:** Inter Variable via `@fontsource-variable/inter`
- **Analytics:** Vercel Analytics + Speed Insights
- **Language:** TypeScript
- **Deployment:** Vercel

## Project Structure

```
src/
  app/
    api/
      featured-work/route.ts   # Returns featuredWork array
      page-data/route.ts       # Returns composite page data
    components/
      about-me/
      communication-methods/
      education/
      experience/
      featured-work/
      footer/
      header/
      hero-section/
    globals.css
    layout.tsx
    page.tsx
  data/
    portfolio.ts               # Single source of truth for all content
public/
  images/
    feature-work/              # Project screenshots
    hero-sec/                  # Avatar + banner
    icon/                      # Tech stack and social SVGs
```

## Content

All copy, links, and structured data live in [`src/data/portfolio.ts`](src/data/portfolio.ts). Editing that file updates the page, API routes, and all components simultaneously — nothing is duplicated.

## Local Development

```bash
npm install
npm run dev        # http://localhost:3000 (Turbopack)
```

Validation:

```bash
npm run lint
npm run build
```

## API Routes

| Route | Returns |
|---|---|
| `GET /api/featured-work` | `{ featuredWork: FeaturedWorkItem[] }` |
| `GET /api/page-data` | Hero links, education, experience, expertise tags |
