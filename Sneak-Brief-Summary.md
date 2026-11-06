# Sneak: Brief Summary (from "Sneak (WIP).docx")

*Summarized 1 Nov 2026 for the lead brand and product designer. Everything below comes from the doc, except the sections marked **[Designer notes]**.*

---

## Decisions so far (updated 6 Nov 2026)

- **Closed beta:** launch uses beta codes, so the waitlist map is archived. Whether sign-up needs a code screen isn't decided.
- **Scouting:** removed.
- **Invites never ring:** the Ambush SMS starts a 5-minute timer. Make an account in time and you survived; miss it and you got hit. One person can have many invites running, so it can't be a real call.
- **Radar limit:** up to 10 friends, replacing the doc's 3 invites a week. Friends on Sneak must accept a request before joining, so nobody gets sneaked without agreeing.
- **No acceptances yet:** a new user skips First sneak and waits in the Arena until someone accepts. This replaces the doc's rule that users never see an empty feed.
- **Default filter:** set once on the first sneak or in Profile, so people don't pick every time. It can still be changed while ringing.
- **Replay:** opens the duel full screen with a back button.
- **Copy:** "Look alive." uses the italic Wink style. Losing reads "you got hit".

- **Name:** SNEAK stays.
- **Logo:** Corner Peek mark (a rounded bracket corner with an eye peeking round it, plus a green dot) with SNEAK in Big Shoulders Display Black. It's also the middle Sneak button in the tab bar.
- **Colour:** brand green #0CE662. Orange (#FF5A1F, soft #FF9A5C) is kept for urgency only: countdowns, Most Wanted, jump scare, sabotage.
- **Posting consent:** simple yes/no. Both yes: posted to your friends. Anyone says no: not posted, and it stays in both people's Duels tab. Either way it's deleted after 24 hours. Saying no is free. The preview has a big Replay button before you decide.
- **Tabs:** Arena (posted duels), Duels (not posted), Sneak (logo; starts a new sneak), Armory, Profile.
- **One person per sneak:** no group sneaks; the first sneak picks one person.
- **Radar (was Watchlist):** up to 10 friends: everyone you've invited to Sneak, plus friends on Sneak who accept your request. You get a notification when they join or accept, and then you can sneak up on them. Contacts are never added automatically. Only people on your radar can sneak you, so it isn't a setting.
- **Naming:** the feed is the **Arena**. **Kill** and **Hit** are kept from the doc (Gotcha/Slipped dropped). "Lair" is now **Profile**.
- **Themes:** Light is the main design (indigo headlines, grey secondary text). Dark is a second mode on the same tokens, following the system setting. Call screens stay black.
- **Duel / Hit:** the incoming buttons are labelled Duel (pick up) and Hit (reject). A Hit is −10, or −5 if the receiver gives a reason; the −5 is only explained on the reason screen. Before it rings, the caller can optionally guess what the person is doing; a right guess doubles their points and creates a "caught out" post ("Maya was in the shower when you sneaked on them").
- **Sneak setup order:** pick a person, add power-ups, optional guess, record permission, filter if no default is set, then it rings.
- **Ringing screen:** countdown on the top half and the caller's camera on the bottom, like the duel layout. Your filter (None, Fisheye, Clown, Thermal) is already on and can be changed here. It previews on their video and lands on the receiver at pick-up. The first filter is free (a proposal, not yet confirmed).
- **Duel start:** a "Duel starts in 10s" countdown replaces the Duel Locked tag, on both the core and invited paths. After that, the only tag is REC, if recording.
- **Recording permission:** the caller allows recording before the ring; the receiver allows it right after picking up. Continue without recording still goes ahead, with no REC tag, no duel to post and no duel points.
- **Artifacts:** Kill is a skull in crosshairs, Hit an impact burst, Vendetta a dagger, Most Wanted a sheriff star, used on tags, Arena cards, result screens and trophies.
- **Watermark:** white, on downloads only, with no options to set.
- **Sign-in:** "I already have an account" goes number, code, welcome back, Arena. Add your friends is one step, combining invites and friends on Sneak, with a progress bar through First sneak.
- **Power-ups (per use):** Incognito 5, Custom ringtone 3, Shield 5, Filters 3, Faster Sneak 5 (5-second ring). Applying one shows a toast.
- **Blackbox audio:** removed.
- **Vendetta:** its own indigo colour; Kill is green, Hit is red.
- **First hit is free:** shown as "Immunity".
- **Split-screen order:** receiver on top, caller below (flipped from the doc), in calls, posts and every export.
- **24h vs. downloads:** duels and other artefacts live on the platform for 24 hours, but users can download them. Every downloadable artefact (duel clips, Crime Scene cards, Most Wanted reports, wanted posters) carries a Sneak branding hook to pull in non-users.
- **Sign-up:** two flows (direct download, invited via Ambush SMS) are mapped on the Figma page "04 — Sign-up Flow".

## 1. The concept in one line
A social game app built on surprise: you "sneak up" on a friend with a **video call that rings for 10 seconds**. What happens next depends on whether they pick up and keep talking.

## 2. Core mechanic and scoring

| Outcome | Trigger | Caller | Receiver |
|---|---|---|---|
| **Kill** | Receiver doesn't pick up, or hangs up before 10s | **+10** | — |
| **Hit** | Same event, from the receiver's side | — | **−10** |
| **Duel** | Receiver picks up and talks **≥10s** (max **1 min**) | Points = upvotes they receive | Points = upvotes they receive |

- **Total points = Kill points + Duel points − Hit points**
- A duel is recorded as a **vertical split-screen** of both people.
- **Posting:** if both agree, the duel goes to the feed. **Choosing not to post costs 10 points.**
- Once posted, friends **upvote who won**. Each person earns points equal to their own upvotes.
- Posted duels are visible to friends for **24 hours**, then **deleted permanently**.

## 3. Game rules
- **Vendetta:** when A kills B, B instantly gets a **24-hour window** to sneak A for **double kill points** (a "Revenge Kill").
- **Most Wanted:** **3 kills in a row without being caught** crowns you Most Wanted in your friend group. You get a **badge or crown** next to your name until someone catches you.
  - Dueling or killing a Most Wanted player is worth **30 points**.
- **Power-ups** are bought with points and are one-time use. Each changes the rules of the next sneak:
  - **Incognito Mode:** hides the caller ID (20 pts/week)
  - **Custom Ringtone:** the receiver's phone plays a ringtone the caller picks (20 pts/week)
  - **Shield:** no hit penalty if you miss the next sneak (20 pts/week)
- **Purge window:** each person gets a **random 15-minute window every day** when kills and duels pay **3×**.
- **DND windows:** users can set do-not-disturb times. During DND, nobody can sneak them **and they can't sneak anyone either**.

## 4. Onboarding flow (in order)
1. **The Jump Scare (the aha moment).** Right after the user enters their name, the app fakes a sneak on their own phone: the screen flashes, the phone vibrates wildly, a countdown runs. When they pick up, a 5-second hype video plays: *"You survived. Now it's your turn to hunt."* This happens **before any permission request**.
2. **Rename the roster.** Never say "Invite Friends." Say **"Build Your Hitlist."** The contacts permission prompt reads: *"Sync contacts to find your targets."*
3. **The "First Blood" gate.** Users never see an empty feed. The contact list shows **crosshairs** next to names: *"Select 3 targets to initiate your first Sneak Up."* The user has to attack before the app unlocks.
4. **The "Ambush" SMS.** Friends who aren't on the app get an urgent, personalized SMS instead of a plain download link: *"🚨 [Name] is trying to Sneak Up on you. You have 5 minutes to download [App Name] and Duel them, or they get a free Kill on your record."*
5. **The Waiting Room.** The inviter lands on a tense screen with a **live radar and a ticking countdown**. When a friend downloads, the inviter gets a push: *"Target acquired. [Friend] is entering the zone. Get ready."*
6. **The "Bounty Hunter" incentive.** Every friend who converts earns the inviter a **rare power-up** (Incognito, Custom Ringtone, or Shield).

## 5. UGC hooks (getting people to post their 10-second videos)
The idea is to frame posting as **comedic evidence, a game mechanic, or retaliation**, not as being a "creator," so people get past the cringe.

1. **Sabotage Filter.** The caller picks an AR filter (fisheye, clown makeup, thermal vision) and it's **applied automatically to the receiver's face** when they pick up. Distortion removes vanity, so people are more willing to post.
2. **Auto-stitched "Kill Cams."** Both sides are recorded: **caller on top** (giggling, waiting), **receiver on the bottom** (confused). Both get a consent choice:
   - **Both yes:** the full video goes to **both** friend groups, and friends vote on either person.
   - **One yes, one no:** shown **only to the yes-person's friends**. It includes the yes-person's video plus **only the audio** of the no-person. **All votes go to the yes-person.**
   - **Both no:** not posted.
   - A sneak that gets "caught" (answered) is called a **duel**. Split-screen is native to TikTok and Reels, so clips export easily.
3. **"Mission Log" feed.** A polished, **Linear-inspired, enterprise-grade dark-mode UI**: stark black, crisp type, high-contrast **green/orange/red status tags** like `[TARGET SECURED]` and `[M.I.A]`. The ironic contrast is the brand: **"a serious tool for an unserious activity."**
4. **"Blackbox" audio.** If the camera is fully dark (covered, face-down), the duel becomes an **audio-only post** shown as a glowing waveform. This saves privacy-sensitive moments and creates a curiosity gap in the feed.

## 6. Virality ideas
- **"Crime Scene" artifacts.** After a kill or duel, the app auto-generates a shareable card or clip styled as forensic evidence: timestamp, blurred location, "suspect" silhouette, kill/duel ratio. It's built for group chats, IG Stories, and Discord, and carries a **personalized deep link** into a counter-sneak or a "view the evidence" teaser.
- **Group Hitlists and factional warfare.** Dorm floors, teams, and friend groups form shared hitlists or "territories." Cross-group kills and duels pay **multiples** and appear on a **public-ish campus leaderboard**.
- **Bounties.** Anyone can put a points bounty on a friend (or on themselves) for a limited window. A claim is broadcast to mutual friends with a flashy notification. Non-users get a reason to join, either to take part or to protect someone.
- **"Most Wanted" seasons and yearbooks.** At the end of each weekly or monthly season, the app produces an absurd "Most Wanted Report" ranking kills, longest survival, revenge ratio, and more, designed to be screenshotted.

## 7. Time-spent and retention ideas
- **Post-duel debrief threads.** Short, **expiring** threads for both players (and optionally mutual friends): reactions, voice notes, roasts, plans.
- **Streaks and survival chains.** Days without being killed, Most Wanted run length, revenge chains. Breaking someone's streak is a celebrated event, which makes people open the app defensively.
- **Seasonal rule modifiers.** For example, "Silent Night" (vibration only), a "Double Agent" weekend (kills award points to a random friend), and campus events tied to real calendars.
- **Personal "lair" or trophy room.** A persistent collection of masks, trophies, and wanted posters that grows with play, for showing off and arranging.
- **Scouting (removed 6 Nov 2026).** Before a sneak, users can review a friend's activity pattern, DND windows, and reaction style (*"usually picks up after 4 seconds," "often in class 2–3"*).

## 8. Go-to-market
1. **Micro-launch: density over volume.** Aim for 500 users in one dorm or school, not 10,000 spread worldwide.
   - **Patient Zero:** recruit 5–10 highly connected students (Greek life, club presidents, athletes).
   - **The bribe:** beta access plus **lifetime Most Wanted status** or unlimited currency. They get **one week** to sneak each other before the school-wide opening.
   - **Goal:** real-world gossip, e.g. *"You snuck up on me in the shower."*
2. **"Jump Scare" content pipeline.** Branded split-screen clips for TikTok, Shorts, and Reels. The team and beta testers **manually seed the first 20–30**. Overlay text: *"My friends downloaded this app that lets them ambush me on video for 10 seconds. I hate it here."* plus a link in bio. No ad spend.
3. **Guerrilla tactics.**
   - **AirDrop Ambush:** AirDrop a crosshair graphic to everyone in a library or lecture hall: *"Someone in this room just put a bounty on you. Check your hitlist."* plus a QR code.
   - **Stickers and chalk:** *"You're being hunted. [QR]"* on mirrors, tables, and bus stops.
4. **Velvet rope.**
   - **Ammunition limit (replaced 6 Nov 2026 by the 10-friend cap):** exactly **3 invites per week**.
   - **Geofenced waitlist map** outside the launch campus: *"Your city needs 500 more targets before Sneak unlocks in your area. Share this link to speed it up."*
5. **Trojan horse.** Drop Ambush links into existing WhatsApp and Discord groups. Barter with **hyper-local campus meme pages**: custom inside-joke ringtones or badges in exchange for pinned posts.

---

## 9. [Designer notes] Contradictions and open questions to settle before design

**Rules and scoring**
1. **Posting consent (resolved).** Simple yes/no: posted only if both say yes; otherwise it stays private in the Duels tab.
2. **Who pays the "don't post" penalty? (resolved)** Nobody. Keeping a duel private is free.
3. **Power-up pricing is unclear.** They're called "one-time use" but priced "20 pts/**week**." Is that a per-use cost, a weekly subscription, or a weekly cooldown?
4. **Multipliers aren't defined.** How do Vendetta 2×, Purge 3×, Most Wanted 30, and cross-group multiples stack? Whose purge window counts, the caller's or the receiver's? Is it hidden or visible?
5. **"Caught" is undefined for Most Wanted.** Does one duel end the reign, or only a kill?
6. **Duel scoring can go negative.** Upvotes are the only reward, while declining to post costs 10. An unanswered call pays +10 for certain, so callers may prefer the receiver *not* answer. Check that the incentives point where you want.
7. **Silent hits.** Should a hit count when the phone is off, there's no signal, or the user is driving, beyond what DND covers?
8. **Ephemerality conflicts (resolved: 24h in-app, downloadable with a branding hook).** Duels are deleted after 24h, yet the doc also proposes exports to TikTok, Crime Scene cards, yearbooks, a persistent trophy room, and scouting data. Decide what is ephemeral and what persists. That decision shapes the whole brand promise.
9. **The 5-minute Ambush SMS (resolved).** Make an account in time and you survived; miss it and you got hit. Nothing rings.

**Trust, safety, and policy risks (these affect brand and UI directly)**
- **Violent lexicon** (kill, hitlist, targets, hunted, crosshairs, bounty, "First Blood") with **high school and Gen Alpha** listed as audiences. This is a likely App Store review problem, could alarm schools and parents, and could cause real panic on campus. Stickers saying "You're being hunted" could be reported as threats. Consider a playful-spy or prank lexicon (*ambush, tag, caught, gotcha, evidence, case file*) that keeps the tension without weapons.
- **Recording consent.** Both sides are recorded automatically, and two-party-consent laws apply in some places. AR filters are put on the receiver's face without their say. Recording **minors** adds more risk.
- **Unsolicited SMS** may run into spam and telecom rules, and the 5-minute pressure reads as a dark pattern.
- **Blackbox audio** captures people in bathrooms or in bed. Audio-only posting needs explicit opt-in.

**Brand direction already implied by the doc**
- "A serious tool for an unserious activity": a Linear-style dark UI, monospace type (the doc itself uses **Roboto Mono**), and green/orange/red status tags.
- Vocabulary to own: mission log, status tags, evidence, debrief, case file, radar.
- Native formats to design for: a vertical split-screen template, a forensic evidence card, a waveform post, a wanted poster or crown badge, and the season report.

---

## 10. [Designer notes] Name ideas (alternatives to "Sneak")

The concept is surprise, being caught off guard, and a split-second reaction. A good name works as a verb (*"I just ___ed you"*), sounds playful rather than violent, and is easy to search.

| Name | Why it works | Watch out |
|---|---|---|
| **Gotcha** | The exact moment the game is built on. Works as a verb and an exclamation, and the push copy writes itself ("Gotcha'd by Maya"). | Common word; hard to trademark and search. |
| **Pounce** | Playful predator energy without weapons; a natural verb ("you got pounced"). Fits the cat-and-mouse loop and suits a mascot. | Some existing brands use it. |
| **Blindside** | Means "caught you off guard." Edgy without violence and fits the Mission Log tone. | Has a sports and tackle connotation. |
| **Lackin'** | Gen Z slang for being "caught lackin'," i.e. unprepared. Very native to the audience. | The slang comes from street and gun culture, so it shares the violence risk above. |
| **Ringer** | The call ringing, plus "put through the ringer" and "dead ringer." Clever and short. | Less obvious about the game. |
| **Peekaboo / Boo** | The jump-scare joke in its softest form, safest for younger users. | Can read as too cute for the dark-UI direction. |
| **10s / Tensec** | The mechanic is the name and reads well as a monospace wordmark. | Generic and harder to own. |

**Recommendation:** **Gotcha** if the brand leans into prank comedy, or **Blindside** if it leans into the "serious tool, unserious activity" Mission Log irony. Both remove the weapon language, which is the single biggest brand risk. *Trademark, App Store name, and domain availability haven't been checked.*
