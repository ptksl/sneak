# Sneak build map

Index of the Sneak Figma file for building the iOS app in Xcode. Read this before opening Figma.

- **File key:** `YPJMBELCIik1hbaE8RnDBn`
- **Link format:** `https://www.figma.com/design/YPJMBELCIik1hbaE8RnDBn/Sneak?node-id=7-253` (the ID with `-` in place of `:`)
- **Product rules:** [Sneak-Brief-Summary.md](Sneak-Brief-Summary.md)
- **Exported assets:** [Sneak-Brand-Assets/](Sneak-Brand-Assets/) (logos, app icons, artifacts, fonts, `colours.json`)
- **Push notifications:** [NOTIFICATIONS.md](NOTIFICATIONS.md)
- **What changed recently:** [CHANGELOG.md](CHANGELOG.md)

## Using Figma without wasting tokens

1. Find the screen below and request only its node ID. Never read a whole page or section.
2. Build shared components first, then reuse them. The "Uses" column shows what each screen needs.
3. Read a note only if you need the reasoning. Each note holds what the screen is, quotes from the doc, and design calls.
4. Take colours from `colours.json` and fonts from `Sneak-Brand-Assets/fonts/`. Don't re-read the token pages.
5. Build from pages 02, 03, 04 and DS. Pages 05 and 06 hold copies, and 01 and 99 aren't for building.

## How the file is arranged

| Page | ID | Use |
|---|---|---|
| 00 — Read Me | `0:1` | Overview, open questions, build map, review log |
| 01 — Brand Exploration · reference | `1:17` | Not for building |
| DS — Design System | `51:47` | Components and tokens |
| 02 — Product UI | `1:18` | Main app screens |
| 03 — Share & Social | `1:19` | Exported and shared artefacts |
| 04 — Sign-up Flow | `40:10` | User flow diagram (`40:11`) and sign-up screens |
| 05 — Dark mode · reference | `73:10` | Same screens with the Dark variable mode |
| 06 — Prototype · reference | `107:10` | Clickable copies. Navigation is listed below |
| 99 — Archive · do not build | `32:91` | Rejected directions, and screens removed from the flows (section `268:1054`) |

On pages 02, 03 and 04, the layers run: `Section › Flow · name › Screens in order › Group · screen › label, screen, note`. Screens are 390 wide. Heights over 844 mean the screen scrolls.

## Screens

Columns: screen, node ID, note ID, components used. Status Bar is on every screen, so it's left out.

### A · Direct download (section `42:10`)

| Screen | ID | Note | Uses |
|---|---|---|---|
| A00 Splash | `100:868` | `104:1730` | Logo / Lockup — Stacked |
| A01 Welcome | `42:13` | `46:414` | Logo / Lockup — Stacked, Button |
| A02 Your name | `42:44` | `46:424` | Progress Bar, Input, Button, System / Keyboard |
| A03 Jump Scare | `43:117` | `46:523` | none |
| A04 You survived | `43:149` | `46:537` | Video / Placeholder, Button |
| A04b You got sneaked | `43:173` | `46:551` | Video / Placeholder, Button |
| A05 Phone number | `42:68` | `46:438` | Progress Bar, Input, Button, System / Keyboard |
| A06 Verify code | `42:94` | `46:448` | Progress Bar, Code Cell, Button, System / Keyboard |
| A07 Birthday | `42:128` | `46:458` | Progress Bar, Input, Button, System / Keyboard |
| A09 Build your radar | `43:197` | `46:561` | Progress Bar, Avatar, Button |
| A11 Add your friends | `100:888` | `104:1738` | Progress Bar, Chip, Callout, Contact Row, Button |
| A11b Add people manually | `42:351` | `46:499` | Progress Bar, Input, Button, Avatar |
| A12 Camera, mic & alerts | `42:394` | `46:509` | Progress Bar, Permission Row, Button |
| A13 First sneak | `43:231` | `46:575` | Progress Bar, Input, Contact Row, Button |
| A13a Guess for 2× points | `269:1234` | `269:1252` | Chip, Button |
| A13b Recording permission | `269:1262` | `269:1278` | Avatar, Chip, Button, Dialog |
| A13c Pick a filter | `269:1288` | `269:1308` | Video / Placeholder, Chip, Toggle, Button |
| A14 Ringing Maya | `102:1343` | `46:589` | Video / Placeholder, Chip, Button |

### B · Invited by a friend (section `44:195`)

| Screen | ID | Note | Uses |
|---|---|---|---|
| B00 Ambush SMS | `44:198` | `46:603` | Avatar, Logo / Mark |
| B01 Invite landing | `44:230` | `46:617` | Logo / Lockup — Horizontal, Avatar, Button |
| B02 Your name | `44:262` | `46:631` | Invite Timer Banner, Progress Bar, Input, Button, System / Keyboard |
| B03 Phone number | `44:291` | `46:641` | Invite Timer Banner, Progress Bar, Input, Button, System / Keyboard |
| B04 Verify code | `44:322` | `46:651` | Invite Timer Banner, Progress Bar, Code Cell, Button, System / Keyboard |
| B05 Birthday | `44:361` | `46:658` | Invite Timer Banner, Progress Bar, Input, Button, System / Keyboard |
| B07 You survived | `269:1430` | `269:1440` | Video / Placeholder, Button |
| B08b You got hit | `44:534` | `46:703` | Artifact / Hero, Status Tag, Avatar, Button |
| B10 Build your radar | `44:618` | `46:730` | Progress Bar, Avatar, Button |
| B12 Add your friends | `100:991` | `104:1746` | Progress Bar, Chip, Callout, Contact Row, Button |
| B12b Add people manually | `44:716` | `46:750` | Progress Bar, Input, Button, Avatar |
| B06 Camera, mic & alerts | `44:396` | `46:668` | Progress Bar, Permission Row, Button |
| B13 First sneak | `44:759` | `46:760` | Progress Bar, Input, Contact Row, Button |
| B13a Guess for 2× points | `269:1318` | `269:1336` | Chip, Button |
| B13b Recording permission | `269:1346` | `269:1362` | Avatar, Chip, Button, Dialog |
| B13c Pick a filter | `269:1372` | `269:1392` | Video / Placeholder, Chip, Toggle, Button |
| B14 Ringing Maya | `102:1371` | `46:774` | Video / Placeholder, Chip, Button |

### L · Already have an account (section `170:953`)

| Screen | ID | Note | Uses |
|---|---|---|---|
| L01 Log in · number | `170:956` | `170:1126` | Input, Button, System / Keyboard |
| L02 Log in · code | `170:982` | `170:1136` | Code Cell, Button, System / Keyboard |
| L03 Welcome back | `170:1019` | `170:1146` | Avatar, Arena Card, Button |
| L04 No account found | `170:1094` | `170:1156` | Code Cell, Button, System / Keyboard, Dialog |

### Sneak, both sides (section `101:216`)

| Screen | ID | Note | Uses |
|---|---|---|---|
| C06 Caller · guess before ringing | `101:488` | `104:747` | Chip, Button |
| C01 Caller · record permission | `101:248` | `104:696` | Avatar, Chip, Button, Dialog |
| C08 Caller · pick a filter | `268:1058` | `268:1076` | Video / Placeholder, Chip, Toggle, Button |
| C02 Caller · ringing | `101:219` | `104:688` | Video / Placeholder, Chip, Button |
| C07 Caller · guessed right | `101:526` | `104:755` | Artifact / Hero, Avatar, Button |
| C03 Caller · no internet | `101:290` | `104:704` | Avatar, Chip, Button, Dialog |
| C04 Caller · on DND | `101:330` | `104:712` | Avatar, Chip, Button, Dialog |
| C05 Caller · couldn't reach | `101:370` | `104:720` | Avatar, Chip, Button, Dialog |
| R02 Receiver · record permission | `101:410` | `104:728` | Video / Placeholder, Dialog |
| R03 Receiver · hit reason | `101:448` | `104:739` | Artifact Tag, Chip, Button |
| R04 Receiver · radar request | `268:1172` | `268:1183` | Avatar, Callout, Button |

### Core loop (section `7:161`)

| Screen | ID | Note | Uses |
|---|---|---|---|
| 06 Incoming Sneak | `7:164` | `13:349` | Status Tag, Avatar |
| 07a Duel starting | `162:695` | `172:1052` | Video / Placeholder, Status Tag |
| 07 Live Duel | `7:208` | `13:367` | Video / Placeholder, Status Tag |
| 07b Live Duel · not recording | `162:740` | `172:1060` | Video / Placeholder |
| 08 Post Consent | `7:253` | `13:385` | Video / Placeholder, Avatar, Status Tag, Button |
| 08b Duel replay | `268:1117` | `268:1141` | Video / Placeholder |
| 09 Kill (caller) | `7:301` | `13:404` | Artifact / Hero, Artifact / Glyph, Button |
| 10 Hit + Vendetta | `7:334` | `13:422` | Artifact / Hero, Artifact / Glyph, Avatar, Button |

### Arena and meta (section `8:168`)

| Screen | ID | Note | Uses |
|---|---|---|---|
| 11 Arena | `8:171` | `13:440` | Video / Placeholder, Status Tag, Chip, Arena Card, Avatar, Tab Bar |
| 11b Save duel (9:16) | `104:441` | `104:766` | Video / Placeholder, Logo / Lockup — Horizontal, Button |
| 11c Duels | `137:531` | `137:860` | Video / Placeholder, Status Tag, Button, Tab Bar |
| 11d Arena · waiting | `280:1149` | `280:1195` | Callout, Contact Row, Button, Tab Bar |
| S01 New sneak | `137:645` | `137:871` | Input, Contact Row, Chip, Button |
| 12 Profile | `104:484` | `13:458` | Avatar, Artifact Tag, Button, Chip, Artifact / Hero, Toggle, Tab Bar |
| 12b Do not disturb · new window | `104:613` | `104:774` | Input, Chip, Button |
| 12c Profile · not Most Wanted | `137:711` | `137:879` | Avatar, Artifact Tag, Button, Artifact / Hero, Toggle, Tab Bar |
| 12d Profile · Do not disturb open | `165:969` | `172:1068` | Avatar, Artifact Tag, Button, Chip, Artifact / Hero, Toggle, Tab Bar |
| 12e Trophies | `165:1126` | `172:1076` | Artifact / Hero |
| 12f Radar | `283:2648` | `283:2690` | Contact Row, Button |
| 12g Add friends | `283:2760` | `283:2777` | Chip, Callout, Contact Row, Button |
| 12h Remove from radar | `283:2839` | `283:2858` | Contact Row, Button, Dialog |
| 13 Armory | `8:425` | `13:476` | Tab Bar |
| 13b Armory · Shield applied | `103:417` | `104:782` | Tab Bar, Toast |

### Share and social artefacts (page 03)

| Artefact | ID | Note | Size |
|---|---|---|---|
| A · Evidence: Case File (Story) | `9:5` | `14:34` | 360×640 |
| B · Evidence: Arena (Story) | `9:174` | `14:50` | 360×640 |
| C · Kill Cam export | `9:354` | `14:66` | 360×640 |
| D · End card | `9:379` | `14:84` | 360×640 |
| E · Most Wanted Report (4:5) | `9:395` | `14:100` | 480×600 |
| F · Ambush SMS | `9:445` | `14:116` | 390×844 |
| G · Campus sticker | `9:477` | `14:168` | 300×300 |
| H · AirDrop image | `9:631` | `14:182` | 300×380 |
| K · Wanted poster | `65:282` | `65:434` | 390×488 |

## Components (DS page)

| Group | Components (node ID) |
|---|---|
| Brand | Logo / Mark `31:25`, Logo / Wordmark `31:27`, Logo / Lockup — Horizontal `31:29`, Logo / Lockup — Stacked `31:35`, App Icon / Dark `31:41`, Brand `31:45`, Paper `31:49`, White `139:42` |
| Navigation | Status Bar `5:18`, System / Keyboard `55:43`, Tab Bar `136:3542` |
| Actions | Button `5:11`, Chip `52:51`, Toggle `52:68` |
| Inputs | Select `52:75`, Input `52:91`, Code Cell `52:147` |
| Lists | Contact Row `53:71`, Permission Row `53:72` |
| Feedback | Status Tag `52:42`, Invite Timer Banner `53:80`, Dialog `98:37`, Toast `98:59`, Callout `99:39`, Progress Bar `169:93` |
| Media | Avatar `5:12`, Video / Placeholder `5:14` |
| Artifacts | Artifact / Hero `160:86`, Artifact / Glyph `160:100`, Artifact Tag `161:65`, Arena Card `161:136` |
| Diagrams only, skip in the app | Flow Node `53:105` |

## Tokens

- **Colour:** collection `Sneak / Color`, modes Light and Dark, 33 variables in the groups bg, line, text, brand, signal, paper, accent, tint. Values are in `Sneak-Brand-Assets/colours.json`.
- **Layout:** collection `Sneak / Layout`, 18 variables in the groups space and radius. Tokens page: `60:1304`.
- **Dark mode:** not redrawn. Same screens with the Dark values, following the phone's setting.
- **Text styles:** Display/XL, L, M · Title/L, M, S · Heading · Body/L, M, S · Label/L, M, S, Button · Input · Mono/Eyebrow, Body, Digit, Caption, Small · Wink
- **Fonts:** Big Shoulders Display, Geist, Geist Mono, Instrument Serif.

## Navigation

From the prototype's connections. Steps marked "auto" and taps on a whole screen stand in for real events such as a timer, a call ending or the other person answering. Check the screen's note for the real trigger.

**Tab bar, on 11, 11c, 12, 12c, 12d, 13 and 13b:** Arena → 11 · Duels → 11c · centre logo → S01 · Armory → 13 · Profile → 12

```
Sign-up
A00 auto→ A01
A01 Get started→ A02 · I already have an account→ L01
A02 Continue→ A03 · A03 Duel→ A04 · A04 Let's Go→ A05
A05 Send code→ A06 · A06 Verify→ A07 · A07 Continue→ A09
A09 Sync contacts→ A11 · Add numbers manually→ A11b→ A12
A11 Continue→ A12
A12 Allow and continue→ A13 if someone accepted · otherwise 11d
11d Add more friends→ 12g · someone accepts (N34)→ A13
A13 Sneak Maya→ A13a (C06)

Caller
C06 Lock in guess / Skip, just ring→ C01
C01 Allow & sneak→ C08 · Continue without recording→ A14 (no recording)
C08 Continue / No filter→ A14
A14 auto→ 07a · Cancel sneak→ A13
07a auto→ 07 · 07 call ends→ 08
08 Replay duel→ 08b · 08b Back→ 08
A14 (no recording) auto→ 07a (no recording) auto→ 07b · 07b call ends→ 11
08 Post it→ 11 · Keep private→ 11c

Receiver
06 Hit→ R03 · Duel→ R02
R02 Allow & duel→ 07a · Continue without recording→ 07a (no recording)→ 07b→ 11
07a auto→ 07 · 07 call ends→ 08
08 Replay duel→ 08b · 08b Back→ 08
R03 Send reason (−5) / Skip (−10)→ 10
10 Plan revenge→ S01
09 Share the evidence / Back to Arena→ 11

Caller outcomes
C02 → C07 · C07 Post it→ 11 · Keep private→ 11c
C03 Try again→ C02 · C04 Remind me at 6→ C02 · C05 Try later→ C02

Log in
L01 Send code→ L02 · L02 Log in→ L03 · Wrong number?→ L01
L03 Back to the Arena→ 11
L04 Create an account→ A02 · Try another number→ L01

Invited (not in the prototype, see the flow diagram)
B00 → B01 → B02 → B03 → B04 → B05
B05 in time→ B07 · timer ran out→ B08b
B07 / B08b → B10 → B12 (or B12b) → B06 → B13 → B13a → B13b → B13c → B14

Main app
11 Save→ 11b · 11b Save to Photos / Share to Reels / TikTok→ 11
11c Post it→ 11
S01 Sneak Maya→ C06 · Cancel→ 11
13 Shield→ 13b · 13b auto→ 13
12 Trophy shelf→ 12e · Do not disturb→ 12d · 12e Profile→ 12
12d Do not disturb→ 12 · Trophy shelf→ 12e · Add a window→ 12b
12b Save window / Cancel→ 12d
12 / 12c / 12d Radar→ 12f · 12f Profile→ 12
12f Review→ R04 · R04 Accept / Not now→ 12f
12f Remove→ 12h · 12h Keep / Remove→ 12f
12f Add more friends→ 12g · 12g Done / Radar→ 12f
12c Trophy shelf→ 12e
```

**In Figma but not in the prototype:** A04b, A09, A11b, 11d and all of B. A13a to A13c use C06, C01 and C08 there. Read the notes for how screens connect, and the flow diagram `40:11` for sign-up.

**Later sneaks skip C08** once a default filter is set. The steps become S01 → C06 → C01 → C02.

## Decisions that are easy to get wrong

- In-app duels show close to their recorded shape, about 1:2. Only the download is 9:16 (11b).
- The white watermark appears on downloads only, never in the app.
- Video placeholders stand in for live camera feeds. Build real video there, not images.
- Nothing rings from an invite. The timer decides: survive, or you got hit.
- Nobody joins a radar without accepting. Radar holds up to 10 friends, counting people requested and invited.
