# nutmeg-site

Marketing/landing page for the nutmeg Claude Code plugin. Built with Astro 6, static output.

## Stack

- Astro 6 (static output, no SSR)
- pnpm
- Node >= 22.12.0

## Structure

```
src/
  pages/index.astro      # Single page — all data arrays (skills, providers, queries) defined here
  layouts/BaseLayout.astro
  components/             # Hero, SkillsGrid, ProvidersGrid, ExampleQueries, InstallRow, etc.
  styles/global.css
```

## Deploy

Static site hosted on Cloudflare Pages. No wrangler config — deploy manually:

```
pnpm build && npx wrangler pages deploy dist --project-name=nutmeg-site
```

## Conventions

- Single-page site — all content lives in `src/pages/index.astro`
- Components are pure Astro (no JS framework)
- Skill names and descriptions must match the nutmeg plugin (`../nutmeg/skills/`)
- No client-side JavaScript unless absolutely necessary
