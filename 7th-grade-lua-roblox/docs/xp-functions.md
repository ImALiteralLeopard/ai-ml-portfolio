# XP System — Function Plan

> This document breaks down the XP system into individual functions, defining responsibilities, inputs, outputs, and notes.  
> All functions are designed to be modular, testable, and easy to implement in Lua.

---

## 1. AddXP(player, amount)
**Purpose:**  
Add XP to a player and check for level-up.

**Inputs:**  
- `player` → the player object or data table  
- `amount` → the amount of XP to add  

**Outputs:**  
- Updated player XP  
- Trigger level-up if XP threshold is met  

**Notes:**  
- Handles XP overflow to the next level  
- Does **not** handle rank milestones directly (optional: call `UpdateRank` separately)

---

## 2. GetXPRequired(level)
**Purpose:**  
Calculate how much XP is required to reach the next level.

**Inputs:**  
- `level` → current player level  

**Outputs:**  
- XP required for the next level  

**Notes:**  
- Implements the quadratic formula from the design  
- Base value can be tweaked for balancing  

---

## 3. CheckLevelUp(player)
**Purpose:**  
Determine if the player has enough XP to level up.

**Inputs:**  
- `player` → the player object or data table  

**Outputs:**  
- Boolean: `true` if a level-up occurs  
- Updates player level if applicable  
- Handles XP carry-over  

**Notes:**  
- Can call `UpdateRank(player)` if a rank milestone is reached  

---

## 4. UpdateRank(player)
**Purpose:**  
Update player rank if a milestone level is reached.

**Inputs:**  
- `player` → the player object or data table  

**Outputs:**  
- Updated player rank  
- Triggers milestone rewards:
  - New weapons  
  - New quest tiers  
  - Minor permanent buffs  
  - Updated rank title  

**Notes:**  
- Only called every 10 levels  
- Rank titles are stored in a **rank table** with names and colors  

---

## 5. XPRewardForAction(actionType)
**Purpose:**  
Determine how much XP an action should award.

**Inputs:**  
- `actionType` → string describing the action (e.g., `"kill"`, `"quest"`, `"training"`)  

**Outputs:**  
- XP value (number)  

**Notes:**  
- Each XP source has a different weight (Training = low, Quests = high)  
- Allows for flexible balancing as the game progresses  

---

## 6. Implementation Notes
- All functions are modular and independent  
- System is **testable without UI**  
- Functions will later integrate with:
  - Player stats table  
  - Leaderstats  
  - Persistent data storage  
- Keeps Lua code clean, readable, and easy to expand  

---

## Repo Structure
