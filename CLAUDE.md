# Pokémon ROM Hack — Project Context

## Overview
A Pokémon ROM hack based on **FireRed**, built from the **pret/pokefirered** decompilation (C source).
The story is being written by my son. The game has **three regions: England, Scotland and Ireland**.

## Environment
- Windows + WSL (Ubuntu); VS Code opened from WSL with `code .`
- Toolchain: build-essential, binutils-arm-none-eabi, git, libpng-dev, plus **agbcc** built into the project (see INSTALL.md)
- Build: `make` → `pokefirered.gba`
- Test in **mGBA**
- Maps edited with **Porymap**
- Git: this is my own fork of pret/pokefirered — commit after each working change

## Design plan
- Reuse FireRed's **Sevii Islands / Seagallop ferry** system for travel between regions
  (e.g. a ferry crossing to Ireland; Scotland connected to England by land)
- Adapt the **Town Map**, which already switches between Kanto and Sevii, to show three regions (new graphics needed)
- Gate access to each region with **story flags**, the same way Sevii is unlocked
- Story details (start town, region order, gym split, rival, villain team, legendary) are still being written — ask me rather than inventing them

## How to work with me
- I'm comfortable with code; explain FireRed-specific engine details when relevant
- Work in small steps: get one town, one route and one scripted event working end to end before expanding
- Always run `make` after changes and fix build errors before moving on
- Never commit or distribute the ROM itself; releases are shared as a `.bps` patch
