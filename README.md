# Brand Creatives for Codex

Install one skill in each business project. Onboard the brand once, then use short briefs to create posters, ads, flyers, pamphlets, invitations and social graphics. Each project keeps its own guide, palette, assets and designs.

## Install from GitHub

From the root of the business project you want to use in Codex, run this in a terminal with Git installed. The command works in macOS, Linux, and Git Bash on Windows.

```sh
(
  set -eu
  brand_skill_tmp="$(mktemp -d)"
  trap 'rm -rf "$brand_skill_tmp"' EXIT

  git clone --depth 1 https://github.com/nikhilbhosale999/brand-creatives-skill.git "$brand_skill_tmp/repo"
  mkdir -p .agents/skills/brand-creatives
  cp -R "$brand_skill_tmp/repo/brand-creatives/." .agents/skills/brand-creatives/
  cp "$brand_skill_tmp/repo/LICENSE" .agents/skills/brand-creatives/
)
```

You can also [download the ZIP](https://github.com/nikhilbhosale999/brand-creatives-skill/archive/refs/heads/main.zip). Extract it, copy the `brand-creatives` folder into your project's `.agents/skills/` directory, and copy `LICENSE` into the installed folder.

Open the project in Codex and invoke `$brand-creatives`. Codex discovers it at `.agents/skills/brand-creatives/SKILL.md`. If the skill does not appear, reopen the project. See the [Codex skill discovery guide](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills).

## Onboard the business

**If you already have brand files**

> Use $brand-creatives to onboard this project. Import the existing brand.md and the logos, fonts and product photos in brand-intake/.

**If you have a business brief**

> Use $brand-creatives to onboard this project. Elm Cycle Repair is a neighborhood bicycle workshop for daily commuters and families. We want a friendly, practical voice. Propose a visual identity and starter assets based on this brief.

Codex saves or updates `brand.md`, creates `brand/palette.json` and stores approved files or proposed starter assets under `brand/assets/`. Identity choices based only on a business brief are proposed for review. Add a website or example designs to give Codex more evidence during onboarding.

## Use it again in a new chat

> Use $brand-creatives to make a 1080 × 1350 social poster for our Saturday free safety checks. The checks run from 10 am to 2 pm. Use “Drop in on Saturday” as the CTA.

> Use $brand-creatives to turn the selected poster into a double-sided A5 pamphlet. Keep the offer wording and use the printer’s specs in print-specs.pdf.

Each job is saved under `brand/outputs/` by default. It can include visual exports and editable sources, depending on the requested format and tools available in Codex. The skill installs without a separate API key or fixed design app.

## Keep business files in their project

This repository contains the reusable skill. The included `.gitignore` covers the default locations for local brand guides, assets, intake files and exports if you test onboarding in a clone of this repository. In a separate public project, add that project’s private brand files to its own Git ignore rules.

The skill is available under the [MIT License](LICENSE).
