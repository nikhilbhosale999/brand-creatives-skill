# Brand Creatives

Install the skill in Codex, Claude Code, Cursor or another compatible coding agent. Onboard each business once, then use short briefs to create posters, ads, flyers, pamphlets, invitations and social graphics. Each project keeps its own guide, palette, assets and designs.

## Install from GitHub

Run this from the root of your business project with Node.js 22.20 or later.

```sh
npx skills add nikhilbhosale999/brand-creatives-skill --skill brand-creatives
```

The installer uses the current project by default. Select your coding agent when prompted, or target it explicitly.

```sh
npx skills add nikhilbhosale999/brand-creatives-skill --skill brand-creatives --agent codex
```

Use `--agent claude-code` or `--agent cursor` for those agents. See the [full list of supported agents](https://github.com/vercel-labs/skills/blob/main/docs/agents.md).

Open the project in your agent and ask it to use the `brand-creatives` skill. In Codex, invoke `$brand-creatives`.

For a manual Codex install, [download the ZIP](https://github.com/nikhilbhosale999/brand-creatives-skill/archive/refs/heads/main.zip) and copy the extracted `brand-creatives` folder into your project's `.agents/skills/` directory.

## Onboard the business

**If you already have brand files**

> Use the brand-creatives skill to onboard this project. Import the existing brand.md and the logos, fonts and product photos in brand-intake/.

**If you have a business brief**

> Use the brand-creatives skill to onboard this project. Elm Cycle Repair is a neighborhood bicycle workshop for daily commuters and families. We want a friendly, practical voice. Propose a visual identity and starter assets based on this brief.

Your agent saves or updates `brand.md`, creates `brand/palette.json` and stores approved files or proposed starter assets under `brand/assets/`. Identity choices based only on a business brief are proposed for review. Add a website or example designs to give Codex more evidence during onboarding.

## Use it again in a new chat

> Use the brand-creatives skill to make a 1080 × 1350 social poster for our Saturday free safety checks. The checks run from 10 am to 2 pm. Use “Drop in on Saturday” as the CTA.

> Use the brand-creatives skill to turn the selected poster into a double-sided A5 pamphlet. Keep the offer wording and use the printer’s specs in print-specs.pdf.

Each job is saved under `brand/outputs/` by default. It can include visual exports and editable sources, depending on the requested format and tools your agent provides. The skill installs without a separate API key or fixed design app.

## Keep business files in their project

This repository contains the reusable skill. The included `.gitignore` covers the default locations for local brand guides, assets, intake files and exports if you test onboarding in a clone of this repository. In a separate public project, add that project’s private brand files to its own Git ignore rules.

The skill is available under the [MIT License](LICENSE).
