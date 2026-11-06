# Sneak design handoff

For whoever is building the iOS app. Screen IDs and navigation are in [Sneak-Build-Map.md](Sneak-Build-Map.md), and push notifications are in [NOTIFICATIONS.md](NOTIFICATIONS.md). This document covers what the map can't: how to read the designs, which rules apply, and what isn't decided.

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
- **Emoji:** standard system emoji in copy, not images.
- **Colour and type:** use the tokens and text styles rather than values read off a frame. Colours are in `Sneak-Brand-Assets/colours.json`.
- **Dark mode:** not redrawn. It's the same screens with the Dark token values, following the phone's setting. Call screens stay black in both modes.
- **Page 05 and page 06:** copies of other screens. Build from the originals.
- **Page 99:** removed screens, including Scouting and the waitlist. Don't build them.
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
8. **Push notifications:** alongside each flow, using [NOTIFICATIONS.md](NOTIFICATIONS.md)

Flow B repeats much of flow A, with an Invite Timer Banner on its sign-up steps. For example, B02 is A02 with the banner. The setup steps A13a to A13c and B13a to B13c are the same screens as C06, C01 and C08. Share one view with options rather than building each one twice.

## Rules to build

### Scoring

| Event | Points |
|---|---|
| Kill: no pick-up, or hung up before 10s | Caller +10 |
| Hit: the receiver's side of a Kill | Receiver −10, or −5 if they give a reason |
| First hit | Free, shown as "Immunity" |
| Duel: picked up and talked 10s to 60s | Each person gets their own upvotes, 1 point per vote |
| Keeping a duel private | Free |
| Invite timer ends before the account is finished | Invited person got hit, with the first hit free |
| Right guess before ringing | 2× points for the caller, and creates a "caught out" post |
| Vendetta: 24h after being killed | Revenge kill pays ×2 |
| Purge: a random 15-minute window each day | ×3 |
| Dueling or killing the Most Wanted | 30 |

Most Wanted is earned with 3 kills in a row.

### Power-ups (points per use)

Incognito 5 · Custom ringtone 3 · Shield 5 · Filters 3 · Faster Sneak 5 (5-second ring). Applying one shows a toast.

### The sneak, in order

1. Pick one person. There are no group sneaks.
2. Add power-ups.
3. Optional guess at what they're doing, for 2× points.
4. Record permission.
5. Pick a filter (None, Fisheye, Clown or Thermal), only if no default is set. "Use this for every sneak" saves it as the default in Profile. From then on this step doesn't appear.
6. It rings for 10 seconds. The countdown is on the top half and the caller's camera on the bottom. The filter can still be changed here for this sneak. It previews on the caller's video and lands on the receiver at pick-up.
7. During the duel, the caller can change the filter with the 🎭 button (07c). The receiver doesn't get this button.

### Duels

- **Layout:** receiver on top, caller below, in calls, posts and every export.
- **Start:** a "Duel starts in 10s" countdown runs first. After that, the only tag is REC, if recording.
- **Recording:** the caller allows it before the ring, and the receiver right after picking up. Without it, the call still goes ahead, with no REC tag, no duel to post and no duel points.
- **Receiver notice:** the incoming screen says their video shows as soon as they tap Duel.
- **Replay:** Replay duel opens 08b full screen, with a back button to the post screen.
- **Posting:** both say yes and it's posted to friends. Anyone says no and it stays in both people's Duels tab. Either way, it's deleted after 24 hours.

### Video shape

- **In the app:** close to the recorded shape, about 1:2 (08, B09, Arena card). Don't stretch it to fill wider spaces.
- **Downloads:** 9:16, for Reels, TikTok and Shorts (11b). The white watermark appears on downloads only.

### Access and limits

- Only people on your radar can sneak you. Radar means people you've invited, plus friends on Sneak who accepted your request (R04). Contacts are never added automatically.
- If nobody has accepted by the end of sign-up, a new user skips First sneak and waits in the Arena (11d). Someone accepting opens First sneak.
- Manage your radar in Profile › Radar (12f): answer requests, remove friends (12h) and add more (12g).
- At 10 of 10, you can't accept a request (R04b) or add and invite anyone until you remove someone. Requests stay pending.
- A radar holds up to 10 friends. This is the only limit on invites and requests: there's no weekly allowance.
- During a do-not-disturb window, nobody can sneak you and you can't sneak anyone.
- Every downloadable artefact carries a Sneak branding hook, for people who don't have the app.

### Invites

An invite never rings, because one person can have many invites running at once. The Ambush SMS starts a 5-minute timer. Finish the account in time and you survive (B07). Miss it and you get hit (B08b).

## Not decided yet

Check with design before building these.

### Product questions

| Question | Where it matters | Used in the designs for now |
|---|---|---|
| Does the Profile ringtone setting replace the Custom ringtone power-up? | 12, 13, S01 | Both exist |
| Does joining from an invite count as accepting? | B10, B12 | Yes, the inviter is on your radar straight away |
| Do requested and invited people count towards the 10? | A11, 12f | Yes |
| Is removing someone silent and two-way? | 12h | Yes to both |
| Does removing someone cancel a running Vendetta? | 12h | Not defined |
| Does a default filter keep costing 3 points per sneak? | C08, S01 | Yes, and None if you can't afford it |
| Who confirms a typed Other… guess? | C06b | Not drawn. It can't be matched automatically |
| What does changing the filter during a duel cost? | 07c | Nothing extra once paid on that sneak. If none was added, 3 points or first one free |
| Does a closed beta need a screen for entering a beta code? | Sign-up | Not drawn |
| Does surviving an invite earn points, and does the inviter get +10 for a hit? | B07, B08b | No points for surviving, +10 for the inviter |
| What happens when the decision timer on the post screen reaches zero? | 08 | Not defined |
| Is the first filter free? | A14, B14 | Free, then 3 per use (a proposal) |
| Does the filter land on the receiver or the caller? | Ringing, 06, 07 | Receiver, with the caller previewing it |
| What shows when Filters wasn't added? | Ringing | Not drawn. The assumption is no picker |
| Do Vendetta, Purge and Most Wanted stack? Whose Purge window counts, and is it visible? | Scoring | Not defined |
| Does a duel end a Most Wanted run, or only a kill? | Most Wanted | Not defined |
| Do hits count with the phone off, no signal or while driving? | Hit | Not defined |

### Legal and App Store risks

These need a decision from someone other than the build team, and they could change copy and flows.

- **Language:** Kill, Hit, hunted and bounty, aimed at a young audience, could cause problems with App Store review, schools and parents.
- **Recording:** consent laws vary by place, and recording minors adds risk.
- **Filters:** one is applied to the receiver's face without them choosing it.
- **SMS:** the Ambush SMS may fall under spam and telecom rules.

### Design gaps

- **12e Trophies:** the list is sample content.
- **Prototype:** nobody has clicked through it from start to finish, and nothing in it leads to 09 Kill.
- **Sneak Maya button:** A13, B13 and S01 use a brighter green than other primary buttons. It may not be final.
- **App icons:** the App Store needs a square master with no transparency, and it hasn't been made. The mark is also about 8 px off-centre at 1024.

## Getting a design question answered

Each screen's note in Figma records what it's for and why it looks that way, so check that first. Anything still unclear, or any rule you need to change, should go to design and be recorded here and in the brief. That way the next person doesn't have to ask again.
