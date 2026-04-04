# nutmeg-site

Landing page for the [nutmeg](https://github.com/withqwerty/nutmeg) Claude Code plugin. Astro static site deployed to Cloudflare Pages (project: `nutmeg-site`).

Live at: https://nutmeg.withqwerty.com

## Commands

```bash
pnpm dev           # Local dev server
pnpm build         # Build to dist/
pnpm deploy        # Build + deploy to Cloudflare Pages
```

GitHub auto-deploy is not connected. Use `pnpm deploy` to push changes live.

## Structure

Single-page site: `src/pages/index.astro`. Data arrays (skills, providers, queries) defined at the top of that file. Components in `src/components/`, global styles in `src/styles/global.css`.

## Conventions

- Components are pure Astro (no JS framework, no client-side JS)
- Skill names and descriptions must match the nutmeg plugin (`../nutmeg/skills/`)
