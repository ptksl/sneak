# Sneak design handoff

For whoever is building the iOS app. Screen IDs and navigation are in [Sneak-Build-Map.md](Sneak-Build-Map.md). This document covers what the map can't: how to read the designs, which rules apply, and what isn't decided.

## Which source wins

When sources disagree, use this order:

1. The screen in Figma, on pages 02, 03, 04 or DS
2. The note beside that screen
3. "Decisions so far" at the top of [Sneak-Brief-Summary.md](Sneak-Brief-Summary.md)
4. The rest of the brief, which summarises the original doc

Several ideas in the original doc have been overturned, so don't build from sections 2 to 5 of the brief without checking the decisions first. For example, the doc charges 10 points for not posting and puts the caller on top. Keeping a duel private is now free, and the receiver is on top.

## How to read the designs

- **Canvas:** screens are 390 wide and 844 tall. Taller frames scroll. Lay screens out responsively rather than fixing them to these sizes.
- **Screen corners:** frames are square. The phone supplies the rounded display corners.
- **Status Bar and System / Keyboard:** these components show system UI. Don't rebuild them.
- **Video / Placeholder:** stands in for a live camera feed or recorded video.
- **Sample content:** names such as Maya and Jay, scores and timers are examples.
- **Colour and type:** use the tokens and text styles rather than values read off a frame. Colours are in `Sneak-Brand-Assets/colours.json`.
- **Dark mode:** not redrawn. It's the same screens with the Dark token values, following the phone's setting. Call screens stay black in both modes.
- **Page 05 and page 06:** copies of other screens. Build from the originals.
- **Prototype triggers:** "auto" steps and taps on a whole screen stand in for real events, such as a timer ending or the other person answering.

## Suggested build order

This is a suggestion, not a design requirement.

1. **Foundations:** colour and layout tokens, text styles, fonts, light and dark modes
2. **Shared components:** Button, Chip, Input, Code Cell, Avatar, Status Tag, Progress Bar, Toast, Dialog, Callout, Tab Bar and the artifacts
3. **Sign-up and log in:** flows A and L
4. **The core loop:** sneak setup, ringing, incoming, duel, post consent, Kill and Hit results
5. **Main tabs:** Arena, Duels, Armory, Profile
6. **Invited flow:** B, which mostly reuses earlier screens
7. **Exports and sharing:** the 9:16 download and the page 03 artefacts

Flow B repeats much of flow A and the core loop, with an Invite Timer Banner on its sign-up steps. For example, B02 is A02 with the banner, and B07 and B08 come from 06 and 07. Share one view with options rather than building each one twice.

## Rules to build

### Scoring

| Event | Points |
|---|---|
| Kill: no pick-up, or hung up before 10s | Caller +10 |
| Hit: the receiver's side of a Kill | Receiver −10, or −5 if they give a reason |
| First hit | Free, shown as "Immunity" |
| Duel: picked up and talked 10s to 60s | Each person gets their own upvotes, 1 point per vote |
| Keeping a duel private | Free |
| Right guess before ringing | Doubles the caller's points and creates a "caught out" post |
| Vendetta: 24h after being killed | Revenge kill pays ×2 |
| Purge: a random 15-minute window each day | ×3 |
| Dueling or killing the Most Wanted | 30 |

Most Wanted is earned with 3 kills in a row.

### Power-ups (points per use)

Incognito 5 · Custom ringtone 3 · Shield 5 · Filters 3 · Faster Sneak 5 (5-second ring). Applying one shows a toast.

### The sneak, in order

1. Pick one person. There are no group sneaks.
2. Add power-ups.
3. Optional guess at what they're doing.
4. Record permission.
5. It rings for 10 seconds. The countdown is on the top half and the caller's camera on the bottom.
6. If the Filters power-up is on, the caller picks None, Fisheye, Clown or Thermal while ringing. It previews on their video and lands on the receiver at pick-up.

### Duels

- **Layout:** receiver on top, caller below, in calls, posts and every export.
- **Start:** a "Duel starts in 10s" countdown runs first. After that, the only tag is REC, if recording.
- **Recording:** the caller allows it before the ring, and the receiver right after picking up. Without it, the call still goes ahead, with no REC tag, no duel to post and no duel points.
- **Receiver notice:** the incoming screen says their video shows as soon as they tap Duel.
- **Posting:** both say yes and it's posted to friends. Anyone says no and it stays in both people's Duels tab. Either way, it's deleted after 24 hours.

### Video shape

- **In the app:** close to the recorded shape, about 1:2 (08, B09, Arena card). Don't stretch it to fill wider spaces.
- **Downloads:** 9:16, for Reels, TikTok and Shorts (11b). The white watermark appears on downloads only.

### Access and limits

- Only people on your radar can sneak you. Radar means people you've invited, plus friends already on Sneak that you add. Contacts are never added automatically.
- During a do-not-disturb window, nobody can sneak you and you can't sneak anyone.
- Invites are limited to 3 per week.
- Every downloadable artefact carries a Sneak branding hook, for people who don't have the app.

## Not decided yet

Check with design before building these.

### Product questions

| Question | Where it matters | Used in the designs for now |
|---|---|---|
| Does the Profile ringtone setting replace the Custom ringtone power-up? | 12, 13, 14, S01 | Both exist |
| Is the first filter free? | A14, B14 | Free, then 3 per use (a proposal) |
| Does the filter land on the receiver or the caller? | Ringing, 06, 07 | Receiver, with the caller previewing it |
| What shows when Filters wasn't added? | Ringing | Not drawn. The assumption is no picker |
| Do Vendetta, Purge and Most Wanted stack? Whose Purge window counts, and is it visible? | Scoring | Not defined |
| Does a duel end a Most Wanted run, or only a kill? | Most Wanted | Not defined |
| Do hits count with the phone off, no signal or while driving? | Hit | Not defined |
| What happens when the Ambush SMS's 5 minutes end? | B00, B01 | Not defined |

### Legal and App Store risks

These need a decision from someone other than the build team, and they could change copy and flows.

- **Language:** Kill, Hit, hunted and bounty, aimed at a young audience, could cause problems with App Store review, schools and parents.
- **Recording:** consent laws vary by place, and recording minors adds risk.
- **Filters:** one is applied to the receiver's face without them choosing it.
- **SMS:** the Ambush SMS may fall under spam and telecom rules.
- **Scouting:** the Scouting Sheet shows behaviour patterns, which raises a stalking concern.

### Design gaps

- **12e Trophies:** the list is sample content.
- **Prototype:** nobody has clicked through it from start to finish, and nothing in it leads to 09 Kill.
- **Sneak Maya button:** A13, B13 and S01 use a brighter green than other primary buttons. It may not be final.
- **App icons:** the App Store needs a square master with no transparency, and it hasn't been made. The mark is also about 8 px off-centre at 1024.

## Getting a design question answered

Each screen's note in Figma records what it's for and why it looks that way, so check that first. Anything still unclear, or any rule you need to change, should go to design and be recorded here and in the brief. That way the next person doesn't have to ask again.
