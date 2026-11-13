# Changelog

Design and handoff changes, newest first. Figma keeps a linked version of each round on the Read Me page, and old screens are kept on page 99 rather than deleted. Add an entry whenever a screen, rule or handoff file changes.

## 13 Nov 2026

### Added

- **12j Delete account and 12k Delete account · code:** a Delete account row in Profile settings, a confirm screen, and an SMS code before deleting.
- **L03 Arena · welcome back:** logging in lands in the Arena, with "While you were gone" at the top.

### Changed

- **Arena duel card:** names sit on the video, top left in white. Time left and Save move to the bottom of the video. The separate "Maya vs Jay" line is gone.
- **A03 Jump Scare:** now looks like a real incoming sneak (06), with Hit and Duel and a "Practice · no points" tag.
- **Filters are free:** removed from the Armory and from S01's power-ups. The "first one's free" copy is gone.
- **Faster Sneak:** has its own lightning icon instead of the shield.
- **12b Do not disturb:** quick pauses are 1h to 5h, replacing "Until tonight" and "Until tomorrow".
- **Profile settings:** the Purge window and Notifications rows are removed.
- **07a:** just a counter, with no "Duel starts in" label, and REC from pick-up.
- **07 Live Duel:** the green duel-time bar at the top is removed, because the timer already shows it. Replays keep their playback bar.
- **08 Post Consent:** the preview fills most of the screen, and the outcomes box is now one line.
- **Typed guesses:** the app matches them itself.

### Removed (moved to page 99)

- **L03 Welcome back.**
- **R03c Receiver · confirm the guess,** and push N40.

## 12 Nov 2026 (later)

### Added

- **A02a and B02a Pick a username:** suggested from the name, with taken and available states.
- **11e Arena · empty:** one-tap faces to sneak, a Purge countdown and a Sneak someone button.
- **Back links** on 11b, 12b, R04 and R04b.
- **Radar button** on Profile, next to Edit profile.
- **Add someone by phone number** on A11, B12 and 12g.

### Changed

- **10-friend cap:** only accepted friends count. Spot counts updated everywhere.
- **Status lines:** just "Requested" and "Invited". Invites get a Cancel button, and On radar becomes Remove.
- **Arena duel card:** 9:16, with time left and Save on the video.
- **Requests banner:** "N people saved you a spot on their radar", with no names.
- **Feed:** "Zara hit Rohan's sneak" becomes "Rohan got Zara · Zara's excuse: in class", so a missed sneak is always told one way.
- **11b:** bigger 9:16 preview, no watermark line.
- **Profile:** the sample address is removed.
- **N35:** says that joining from an invite counts as accepting.

## 12 Nov 2026

### Added

- **A02b and B02b Add your photo:** a skippable profile photo step after the name. **12i Edit profile** changes it later.
- **Five filters, locked:** Fisheye, Clown, Thermal, Bobblehead, Old age, in every picker. C08 and C08b to C08e show each on a sample face.
- **R03b and R03c:** the receiver can type an Other… reason, and confirms the caller's typed guess. Push N40.
- **07d random topic:** an exploration, not in any flow yet.
- **Sample photos:** on A04, A04b and B07, and on the DS page.

### Changed

- **Sent requests:** the button now says Cancel instead of Requested. The status line still says "Requested · waiting for them".
- **Mutuals:** removed everywhere, including the Contact Row component.
- **Request signposts:** Arena banner, Profile tab dot and a request count on the Radar row. Radar shows two requests to show the list.
- **Arena duel card:** full width again, video cropped to fill, votes underneath.
- **08 Post Consent:** preview almost full width, cropped to fill, options below.
- **A11:** shows a first-time user, with no accepted friends. "On your radar" replaces "Accepted · on your radar".

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
- **07c Live Duel · change filter:** a 🎭 button lets the caller change the filter during the duel.
- **C06b guess, Other:** tapping Other… opens a text field and the keyboard.
- **Second-sneak path in the prototype:** S01 goes through guess and recording straight to ringing, with no filter step.
- **B07 You survived:** shown when an invited person finishes their account in time.
- **Push notifications:** a list of 39 in `NOTIFICATIONS.md` and on the Read Me page.
- **10-friend cap:** explained on the invite screen, and shown as "4 of 10" in Profile. It replaces the 3 invites a week.

### Changed

- **Invited flow:** nothing rings from an invite. One person can have many invites running at once, so it can't be a real call. Make an account in time and you survive, or you get hit.
- **Invited flow order:** camera, mic and alerts (B06) moved to just before the first sneak, and the timer banner came off that screen. B13 is now "Who's your first sneak?".
- **Invite screens:** A11 and B12 are one screen, "Add your friends", with friends on Sneak and contacts together.
- **A00:** "Look alive." now uses Instrument Serif Italic.
- **A01:** "10 seconds to pick up. Miss it and it's a "hit"."
- **You got hit:** replaces "hit" on A04b, B08b and screen 10. B08b was "Too late".
- **A12 and B06:** new lines for camera, microphone and notifications.
- **Ambush SMS, B01 and share card F:** new copy for surviving or getting hit. The B01 button is now "Beat the clock".
- **A11 and B12:** the count now says 3 of 10 friends, matching the people listed.
- **A11, B12 and 12g callout:** now "10 spots. Choose wisely", saying only people you add can sneak you and you them, with emoji for a closed-circle feel. It no longer explains requests, because the button shows that.
- **Closed-circle tone:** new copy and emoji on A01, A09, B10, A13, B13, S01, 11d, R04, R04b, 12f, 12g and push notifications N33 and N34.
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
