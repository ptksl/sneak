# Changelog

Design and handoff changes, newest first. Figma keeps a linked version of each round on the Read Me page, and old screens are kept on page 99 rather than deleted. Add an entry whenever a screen, rule or handoff file changes.

## 6 Nov 2026

Figma review log: node `274:13`.

### Added

- **08b Duel replay:** Replay duel on the post screen now opens the duel full screen, with a back button.
- **R04 Radar request:** the other side of Add. Nobody joins a radar, or can sneak you, until you accept.
- **C08 Pick a filter:** shown until a default filter is set.
- **Default filter:** a new setting in Profile, so people don't choose every time.
- **A13a to A13c and B13a to B13c:** guess for 2× points, recording permission and filter, straight after First sneak.
- **11d Arena · waiting:** where a new user waits if nobody has accepted yet. Someone accepting opens First sneak.
- **12f Radar, 12g Add friends and 12h Remove from radar:** manage friends after sign-up, opened from the Radar row in Profile.
- **R04b Radar full:** at 10 of 10 you must remove someone before accepting. The request stays pending.
- **B07 You survived:** shown when an invited person finishes their account in time.
- **Push notifications:** a list of 39 in `NOTIFICATIONS.md` and on the Read Me page.
- **10-friend cap:** explained on the invite screen, and shown as "4 of 10" in Profile. It replaces the 3 invites a week.

### Changed

- **Invited flow:** nothing rings from an invite. One person can have many invites running at once, so it can't be a real call. Make an account in time and you survive, or you got hit.
- **Invited flow order:** camera, mic and alerts (B06) moved to just before the first sneak, and the timer banner came off that screen. B13 is now "Who's your first sneak?".
- **Invite screens:** A11 and B12 are one screen, "Add your friends", with friends on Sneak and contacts together.
- **A00:** "Look alive." now uses Instrument Serif Italic.
- **A01:** "10 seconds to pick up. Miss it and it's a "hit"."
- **You got hit:** replaces "hit" on A04b, B08b and screen 10. B08b was "Too late".
- **A12 and B06:** new lines for camera, microphone and notifications.
- **Ambush SMS, B01 and share card F:** new copy for surviving or getting hit. The B01 button is now "Beat the clock".
- **A11 and B12:** the count now says 3 of 10 friends, matching the people listed.
- **A11, B12 and 12g callout:** now "10 spots. Choose wisely", saying only people you add can sneak you and you them, with emoji for a closed-circle feel. It no longer explains requests, because the button shows that.
- **A14 and B14:** now show the guess and the chosen filter.
- **User flow diagram:** updated for all of the above.

### Removed (moved to page 99, node `268:1054`)

- **Scouting:** 14 Scouting Sheet, and the Scout tips on screen 10 and B08b.
- **3 invites a week:** the limit, the Invites row in Profile, and share card J · Velvet rope.
- **Waitlist, for the closed beta:** A08 and share card I, plus the campus check in the flow.
- **Separate friends step:** A11c and B12c.
- **Ringing from an invite:** old B07 Incoming sneak, B08a, B08 and B09.

## 5 Nov 2026

### Added

- **Build handoff:** `CLAUDE.md`, `Sneak-Build-Map.md`, `DESIGN-HANDOFF.md`, `README.md` and this repo.

### Changed

- **Recorded duels:** shown close to their recorded shape, about 1:2, on 08, B09 and the Arena card. The download stays 9:16, and 11b shows a true 9:16 preview.
- **Arena duel card:** the video moved to the left, with names and votes beside it. Vote rows are now identical.
- **File structure:** each screen, label and note is grouped in flow order, generic layers are named, and the prototype is in sections.
- **Screen corners:** all screen frames are square.
