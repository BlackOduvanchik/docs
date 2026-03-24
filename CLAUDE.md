# CLAUDE.md — Antidetect Browser Documentation

## Project overview

- Mintlify documentation site for an antidetect browser product
- Two tabs: **Documentation** (user guides) and **API Reference** (for developers/AI agents)
- Style reference: docs.polymarket.com (concise, technical). Structure reference: docs.browser.vision

## Stack & structure

- **Mintlify** with `docs.json` (NOT `mint.json` — deprecated)
- MDX files with YAML frontmatter (`title` and `description` required on every page)
- Theme: `maple`
- Language: English
- Components: Cards, CardGroup, Steps, Tabs, Callouts (Note/Warning/Info), CodeGroup, Accordion, Columns

## Commands

```bash
# Local preview
npx mintlify@latest dev

# If port 3000 is busy
npx mintlify@latest dev --port 3333

# Check broken links
npx mintlify@latest broken-links

# Validate build
npx mintlify@latest validate
```

## Content rules

- Concise, technical writing — no filler
- Second-person voice ("you")
- Sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, code references
- Screenshot placeholders: `<!-- Screenshot: description -->`
- Code blocks must have a language tag
- Internal links use relative paths (no domain)
- NO emoji in headings
- Every MDX file must have frontmatter with `title` and `description`

## docs.json rules

- Schema: `https://mintlify.com/docs.json`
- Navigation uses groups with Font Awesome icons
- Two tabs: "Documentation" and "API Reference"
- After adding a new page, always add it to `docs.json` navigation

## Git workflow

- Never use `--no-verify` when committing
- Commit often, in logical blocks
- Commit messages in English
- Never skip or disable pre-commit hooks
