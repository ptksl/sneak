# Sneak

A social game for iOS. You sneak up on a friend with a video call that rings for 10 seconds. If they miss it, you get a Kill. If they pick up and keep talking, it becomes a Duel: a recorded split-screen that friends can vote on for 24 hours.

This repo holds everything needed to build the app from the designs. The Xcode project should be created here too, so it sits alongside these files.

## What's here

| Path | What it's for |
|---|---|
| [DESIGN-HANDOFF.md](DESIGN-HANDOFF.md) | Start here: what to build, in what order, and what's still undecided |
| [Sneak-Build-Map.md](Sneak-Build-Map.md) | Every screen's Figma node ID, its components, and the navigation |
| [Sneak-Brief-Summary.md](Sneak-Brief-Summary.md) | Product rules and decisions |
| [NOTIFICATIONS.md](NOTIFICATIONS.md) | Every push notification, with draft copy |
| [CHANGELOG.md](CHANGELOG.md) | What changed in the designs and docs, newest first |
| [Sneak-Brand-Assets/](Sneak-Brand-Assets/) | Logos, app icons, artifacts, fonts and colour tokens |
| [CLAUDE.md](CLAUDE.md) | Loaded automatically by Claude Code, and points it to the files above |

Designs are in [Figma](https://www.figma.com/design/YPJMBELCIik1hbaE8RnDBn/Sneak).

## Getting started

1. Ask for access to this repo and the Figma file. The Figma link alone doesn't give you access.
2. Clone the repo.
3. Connect Figma to your Claude Code so it can read the screens.
4. Run Claude Code from the repo root, so `CLAUDE.md` loads.
5. Read [DESIGN-HANDOFF.md](DESIGN-HANDOFF.md).

## Keeping things in sync

The Figma file is the source of truth for design. The build map and exported assets are snapshots of it, so when a screen is added or changed, update them and [CHANGELOG.md](CHANGELOG.md) in the same commit as the work.

This repo is private because Sneak is unreleased.
