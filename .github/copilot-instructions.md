# Project Guidelines

## Project Overview
- Mona Mayhem is an Astro v5 server-rendered app that compares GitHub contribution activity.
- Runtime is Node via `@astrojs/node` in standalone mode.
- Primary app code lives in `src/pages`; static assets live in `public`.

## Build and Dev Commands
- Install dependencies: `npm install`
- Start local dev server: `npm run dev`
- Build for production: `npm run build`
- Preview production build: `npm run preview`
- Run Astro CLI directly: `npm run astro -- <args>`

## Architecture
- Routing is file-based under `src/pages`.
- Main page entry: `src/pages/index.astro`.
- API endpoints live under `src/pages/api/**`.
- Dynamic route example: `src/pages/api/contributions/[username].ts`.

## Astro Best Practices
- Keep Astro files structured as frontmatter first, template markup second.
- Keep server logic in API routes with typed handlers (`APIRoute`).
- For runtime-only endpoints, set `export const prerender = false`.
- Return explicit status codes and JSON headers from API routes.
- Keep TypeScript strict-compatible (project extends `astro/tsconfigs/strict`).

## Conventions
- Prefer small, focused page and API files.
- Preserve existing formatting style (tabs in source files where already used).
- Do not use workshop content under `workshop/` as implementation requirements unless explicitly asked.

## References
- Project setup and context: `README.md`
- Astro framework docs: https://docs.astro.build/
- Node adapter docs: https://docs.astro.build/en/guides/integrations-guide/node/
