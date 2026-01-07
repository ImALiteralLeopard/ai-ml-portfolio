# System Build Plan

## System: XP & Rank Progression

---

## Purpose
Track player progression through XP and levels, and reward players at major rank milestones without overloading the system with constant unlocks.

This system is designed to be simple at first, scalable later, and compatible with persistent data saving.

---

## 1. Level Range
- Player levels range from **1 to 100**  
- Levels increase sequentially (no skipping levels)

---

## 2. XP Required Per Level
- XP required to level up **increases with level**  
- The progression follows a **quadratic curve**  
- Conceptual formula:  
  **XP Required = Base Value × (Current Level²)**  
- Early levels require relatively low XP  
- Late-game levels require significantly more XP, but remain achievable

---

## 3. Base XP Value
- A **base XP value** controls overall progression speed  
- Adjusting the base value allows **global tuning** without redesigning the system  
- Base value ensures:  
  - Fast early progression  
  - Slower, meaningful late-game progression

---

## 4. XP Gain Scaling
- XP earned from gameplay **increases as players progress**  
- XP rewards scale **slowly** (linear or near-linear growth)  
- XP gain scaling is **always slower than XP requirements**  
- Ensures:  
  - Progression never stops  
  - Leveling becomes harder over time, without being impossible

---

## 5. XP Sources
Players earn XP from multiple activities:

| Source        | XP Value |
|---------------|----------|
| Training      | Low      |
| Enemy Kills   | Medium   |
| Quests        | High     |
| Match Wins    | High     |
| Time Played   | Very Low |

> Each source has different weight to prevent farming and encourage varied gameplay

---

## 6. Level-Up Behavior
- XP is accumulated continuously  
- When XP ≥ required XP:  
  - Player level increases by **1**  
  - Excess XP carries over to next level  
- Normal level-ups do **not** grant rewards

---

## 7. Rank Milestones
- A new rank is reached **every 10 levels**  
- Rank milestones unlock:  
  - New weapons  
  - New quest tiers  
  - Minor permanent buffs  
  - New rank title  
- Rank rewards are **separate from standard level-ups**

---

## 8. Design Constraints
- XP is **never lost**  
- Must support **persistent saving** later  
- System must be **deterministic and testable** without UI

---

## Notes for Future Tuning
- Base XP value can be adjusted to tweak pacing  
- XP reward values can be balanced after playtesting  
- Rank milestone rewards can expand **without changing XP logic**

Rank milestone rewards can be expanded without changing XP logic
