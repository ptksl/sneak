# Sneak push notifications

Every push the flows need, as of 6 Nov 2026. Figma has the same list on the Read Me page (node `274:226`). Copy is a draft, and names are samples. "Beta" is what's recommended for the closed beta launch, and "Later" can wait. That split is a proposal, not a decision yet.

## Sneaks and outcomes

| # | Event | Who gets it | Copy | Opens | When |
|---|---|---|---|---|---|
| N01 | Incoming sneak | Receiver | Maya is sneaking up on you (rings like a call) | 06 | Beta |
| N02 | You missed a sneak | Receiver | You got hit. Maya sneaked up on you. −10 | 10 | Beta |
| N03 | First hit, free | Receiver | You got hit by Maya, but your first one's free. No points lost. | 10 | Beta |
| N04 | Shield blocked a hit | Receiver | Your Shield blocked Maya's hit. No points lost. | 13 | Later |
| N05 | Kill | Caller | Kill. Rhea didn't pick up. +10 | 09 | Beta |
| N06 | Hit reason sent | Caller | Jay sent a reason: In class. | 09 | Later |
| N07 | Right guess | Caller | You called it. Jay was in the shower. 2× points. | C07 | Beta |
| N08 | Caught-out post | Receiver | You're in the Arena. Maya caught you in the shower. | 11 | Beta |
| N09 | Remind me (DND ended) | Caller who tapped "Remind me" on C04 | Rhea's do not disturb has ended. Sneak them now. | S01 | Beta |

## Duels

| # | Event | Who gets it | Copy | Opens | When |
|---|---|---|---|---|---|
| N10 | Other person wants to post | Other duelist | Maya wants to post your duel. Watch it back and decide. | 08 | Beta |
| N11 | Decision timer ending | Anyone undecided | Last chance to decide on your duel with Maya. | 08 | Beta |
| N12 | Duel posted | Both duelists | Your duel with Maya is live in the Arena. | 11 | Beta |
| N13 | Duel not posted | Both duelists | Your duel with Maya wasn't posted. It's in Duels for 24 hours. | 11c | Beta |
| N14 | New votes, batched | Both duelists | 8 friends voted on your duel. You're ahead 12–7. | 11 | Beta |
| N15 | Friend posted a duel | Their friends | Maya and Jay just dueled. Who won? | 11 | Later |
| N16 | Duel about to expire | Both duelists | Your duel with Maya disappears in 1 hour. Save it now. | 11b | Beta |
| N17 | Final result | Both duelists | Duel over: you won 12–7. +12 points. | 12 | Later |

## Vendetta

| # | Event | Who gets it | Copy | Opens | When |
|---|---|---|---|---|---|
| N18 | Vendetta open | Person killed | You've got 24 hours to get Maya back for ×2. | S01 | Beta |
| N19 | Vendetta on you | Person who killed | Jay has a Vendetta on you. 24 hours to dodge it. | 11 | Beta |
| N20 | Vendetta ending | Person killed | 1 hour left to get Maya back. | S01 | Later |
| N21 | Revenge landed | Avenger | Revenge. You got Maya back. +20 | 09 | Beta |
| N22 | Revenge on you | Target | Jay got their revenge. You got hit. | 10 | Beta |

## Most Wanted

| # | Event | Who gets it | Copy | Opens | When |
|---|---|---|---|---|---|
| N23 | One kill away | Player on 2 kills | One more kill and you're Most Wanted. | S01 | Later |
| N24 | You're Most Wanted | Player | You're Most Wanted. Everyone's after you now. | 12 | Beta |
| N25 | Friend is Most Wanted | Their friends | Rhea is Most Wanted. Catch them for 30 points. | S01 | Beta |
| N26 | You caught the Most Wanted | Catcher | You caught Rhea. +30 | 09 | Beta |
| N27 | You were caught | Most Wanted | Tobi caught you. Your Most Wanted run is over. | 12c | Beta |
| N28 | Friend was caught | Their friends | Tobi caught Rhea. Most Wanted is up for grabs. | 11 | Later |
| N29 | Weekly report | Everyone | This week's Most Wanted Report is out. | Artefact E | Later |

## Purge, streaks and trophies

| # | Event | Who gets it | Copy | Opens | When |
|---|---|---|---|---|---|
| N30 | Your Purge started | Player | Your Purge is on. Sneaks pay ×3 for 15 minutes. | S01 | Beta |
| N31 | Streak broken | Player | Maya broke your 5-day streak. | 12 | Later |
| N32 | Trophy earned | Player | New trophy: Vendetta paid. | 12e | Later |

## Radar and invites

| # | Event | Who gets it | Copy | Opens | When |
|---|---|---|---|---|---|
| N33 | Radar request | Person added | Jay wants you on their radar. | R04 | Beta |
| N34 | Request accepted | Person who asked | Rhea accepted. You can sneak them now. | S01 | Beta |
| N35 | Invited friend joined | Inviter | Jay joined Sneak and is on your radar. | S01 | Beta |
| N36 | Invited friend survived | Inviter | Jay made it in time and survived. | S01 | Beta |
| N37 | Invite timer ran out | Inviter | Time's up. Jay didn't make it, so you scored. | 11 | Beta |
| N38 | Bounty Hunter reward | Inviter | Jay joined, so you earned a Shield. | 13 | Beta |
| N39 | Invites refilled | Player | You've got 3 new invites this week. | 12 | Later |
| N40 | Radar slot freed | Player at 10 friends | You've got room on your radar again. | 12 | Later |

## Not push notifications

- **SMS:** the Ambush SMS (B00) and verification codes go by text. Someone who hasn't got the app can't receive a push.
- **In-app only:** toasts, the screens a caller sees when a sneak can't go through (C03, C04, C05), and the timer banner during invited sign-up. Notifications aren't allowed until just before the first sneak, so nothing can be pushed during sign-up.
- **"While you were gone" on L03:** nothing sends while logged out, so this list catches people up on these same events when they log back in.

## Rules to confirm

These aren't decided yet, so check with design before building them.

1. **Do not disturb:** N01 can't happen during DND. Should everything else wait until it ends, or send silently?
2. **Revealing who said no:** N13 is written so it doesn't say who declined. N10 does reveal that the other person said yes.
3. **Batching:** votes (N14) and friend activity (N15, N25, N28) need a limit so a busy friend group doesn't flood people.
4. **Purge privacy:** the Purge window is hidden from friends, so N30 goes only to the player.
5. **Settings:** Profile has one Notifications row. Decide whether people can mute by group. N01 should stay on, because a muted sneak still costs points.
6. **Decision timer:** 08 says "Decide in 00:42", but what happens at zero isn't defined. N11 depends on it.
