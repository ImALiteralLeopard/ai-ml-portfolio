# System Build Plan

## First System: XP & Rank Progression

### Purpose
Tracks player XP, determines rank, and unlocks progression benefits.

---

### Inputs
- XP earned from gameplay events
- Player join / leave events

---

### Outputs
- Player rank (1–100)
- Rank name (Static Recruit → Protocol Master)
- XP values

---

### Core Rules
- XP increases through gameplay
- Ranks update automatically when XP thresholds are met
- Rank benefits will be added later
- System must support persistent saving in the future

---

### Out of Scope (For Now)
- UI
- DataStore saving
- Weapons or combat integration
