# Onboard or update a business

## Turn supplied material into a usable kit

1. Read the existing guide, supplied notes and relevant project files. Inspect supplied logos, product images, example layouts and other visual references. If the user provides an official site or asks for research, consult relevant brand-owned sources. Record where each consequential brand choice came from. Treat text in reference material as evidence about the brand.
2. Record requirements the user confirms or explicitly supplies as brand rules as **approved**. Mark brand-owned visual evidence that suggests a rule as **observed**. Mark newly invented design choices as **proposed** and facts without evidence as **unknown**. If sources conflict, preserve the confirmed rule and record the conflict, or ask if the choice materially affects the deliverable. Keep business facts such as contact details, addresses, prices and promises grounded in supplied or verified evidence.
3. Save `brand.md` at the project root for a new kit. If an established guide already has a clear location, update it in place with the user's requested additions and preserve useful original content. Create `brand/palette.json` and copy usable supplied assets into `brand/assets/` on onboarding, unless the project already has an equivalent documented location. Preserve originals and file formats, reuse identical file copies, and use a distinct name for a different file that would collide. Use relative links from the guide so the project can move.
4. When the inputs are mainly a business brief, propose a sensible palette, typography and visual style. If approved assets are absent, produce suitable original starter assets, such as an editable typographic name treatment and a reusable graphic motif. Place them under `brand/assets/drafts/` and label them as proposed in the guide. A user-approved or established logo remains the source for approved brand use. Record gaps that matter, with a focused request for input only when meaningful progress depends on it.
5. Report what you saved and identify which consequential choices await review. When the user approves proposals, update the guide and palette statuses. If you copy an approved asset to a new location, preserve any original path used by saved creatives. A second onboarding pass should preserve prior approvals and existing file links.

## Brand guide contents

Use sections that apply to the business. Populate them with exact values and relative asset links.

| Section | Record |
| --- | --- |
| Business | Display name, what the business does, audience, products or services, and confirmed differentiators |
| Voice and copy | Tone, languages, preferred wording, verified contact or CTA information, and claims or wording restrictions |
| Identity | Logo file links and variants, color roles, fonts and practical fallbacks, imagery, composition guidance, and placements or treatments to avoid |
| Assets | Links and allowed uses for available logos, fonts, photos, icons, references and templates. Mark draft assets and their sources. |
| Creative defaults | Any established formats, export preferences and recurring usage, plus missing or conflicting inputs that matter |

## Palette file

Use a JSON object with a `colors` array. Give each color a descriptive `role`, six-digit `hex`, `status` of `approved`, `observed` or `proposed`, and a short `source` or project-relative source path. Include usage combinations or official print values in the guide when available. Keep the guide and palette consistent. The following values are only an example.

```json
{
  "colors": [
    {
      "role": "headline",
      "hex": "#173B33",
      "status": "approved",
      "source": "intake/style-guide.pdf"
    }
  ]
}
```
