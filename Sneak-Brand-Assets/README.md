# Sneak brand assets

Exported from the Sneak Figma file on 4 Nov 2026.

## Logos: `logos/`

- `svg/` and `png/`: the 10 export canvases with safe space, on a solid background (white, black, paper, one-colour). PNGs come at 2x and 4x.
- `transparent/`: mark, wordmark, lockup and stacked in indigo and green, with no background and no safe space. Add clear space of half the mark's height when placing these.

## App icons: `app-icons/`

Dark, Brand, Paper and White, as SVG and 1024 px PNG. These have rounded corners and transparent outside the corners. The App Store needs a square master with no transparency, so export a square version before submitting.

## Artifacts: `artifacts/`

The file has no emoji. These are its equivalent:

- `hero/`: full colour, transparent, SVG and 1024 px PNG. Kill, Hit, Vendetta, Most Wanted, Streak.
- `glyph/`: one colour for small tags, transparent, SVG and 256 px PNG. Kill, Hit, Vendetta, Most Wanted. Streak has no glyph in the design system.

## Fonts: `fonts/`

From Google Fonts, under the SIL Open Font License (`OFL.txt` in each folder). The Geist, Geist Mono and Big Shoulders Display files are variable fonts that cover all the weights below.

| Family | Styles used | Used for |
|---|---|---|
| Big Shoulders Display | Black | Wordmark, display type, big numbers |
| Geist | Regular, Medium, SemiBold, Bold | Interface text |
| Geist Mono | Regular, Medium, SemiBold | Labels, tags, digits, timers |
| Instrument Serif | Italic | "Wink" accent style |

## Colours: `colours.json`

Every colour token in Light and Dark, as hex. An eight-digit hex includes alpha. `signal/secured` points to another token in Figma rather than holding its own value, so it's marked `alias`.
