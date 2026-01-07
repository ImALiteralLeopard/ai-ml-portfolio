# System Build Plan

## System: XP & Rank Progression

---

## Purpose
Track player progression through XP and levels, and reward players at major rank milestones without overloading the system with constant unlocks.

This system is designed to be simple at first, scalable later, and compatible with persistent data saving.

---

## XP Sources
Players can earn XP from multiple gameplay activities:
- Training modes
- Enemy kills
- Completing quests
- Time played
- Winning matches

Different activities will reward different amounts of XP to prevent farming and encourage varied gameplay.

---

## Leveling Rules
- XP is **only gained**, never lost
- XP required to level up **increases as level increases**
- Early levels require much less XP than late-game levels
  - Example:  
    - Level 1 → ~150 XP  
    - Level 99 → ~15,000 XP
- As players progress, they earn XP **more easily**, but leveling still becomes harder overall

This ensures progression never stops, but slows down naturally over time.

---

## Ranks & Milestones
- Levels range from **1 to 100**
- Every **10 levels**, the player reaches a new rank title
- Normal level-ups do **not** grant rewards

### Rank Rewards (Every 10 Levels)
When a new rank is reached, players unlock:
- New weapons
- Additional quest tiers
- Slight permanent buffs
- A new rank title

---

## Rank Titles
- Rank 1–10: **Static Recruit**
- Rank 11–20: **Kinetic Specialist**
- Rank 21–30: **Orbital Sentinel**
- Rank 31–40: **Plasma Captain**
- Rank 41–50: **Nova Commander**
- Rank 51–60: **Stellar Warden**
- Rank 61–70: **Zenith Striker**
- Rank 71–80: **Celestial Vanguard**
- Rank 81–90: **Overdrive Archon**
- Rank 91–100: **Protocol Master**

All ranks are color-coded for UI clarity.

---

## Leaderstats & Economy (Planned)
- Wins
- Plasma (currency)
  - Used to buy weapons or melee items

These stats will be integrated later but are acknowledged in this system design.

---

## Out of Scope (For Now)
The following are intentionally excluded from the first implementation:
- UI
- DataStore saving
- Weapon logic
- Combat balancing

---

## Success Criteria
This system is considered complete when:
- XP can be earned from multiple sources
- Levels increase correctly based on XP
- Rank titles update at correct milestones
- The system can later support saving without redesign
