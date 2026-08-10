---
title: "Week 5 Worklog"
date: 2026-07-20
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:

* **Item & Loot System:** Design detailed data models for game items (Weapon, Armor, Accessory, Consumable) grouped into 4 rarity tiers.
* **Loot Algorithms:** Implement a Weighted Random Algorithm for loot distribution and dynamic calculations of Gold/XP based on boss tiers.
* **Inventory Management Backend:** Develop AWS Lambda functions handling capacity checking rules (max 100 slots per character).
* **Equip/Unequip Logic:** Write backend logic for equipping items, modifying player statistics in real-time, and updating database values.

### Tasks to be carried out this week:

| Day | Task | Start Date | End Date | Reference Material |
| --- | --- | --- | --- | --- |
| 1 | - Design the class definitions for items (Weapon, Armor, Accessory, Consumable) in `GameShared` <br> - Add Rarity enums (Common, Rare, Epic, Legendary) | 20/07/2026 | 20/07/2026 | Game design object patterns |
| 2 | - Code the Weighted Random loot drop algorithm in C# <br> - Code dynamic Gold and XP scaling multipliers based on boss levels | 21/07/2026 | 21/07/2026 | Weighted Distribution Algorithms |
| 3 | - Build the Inventory management AWS Lambda endpoint in C# <br> - Implement the inventory capacity validation rule (maximum 100 items limit) | 22/07/2026 | 22/07/2026 | AWS Lambda C# Programming |
| 4 | - Write the Equip and Unequip Lambda functions <br> - Implement rules checking (ensure only one item can occupy an equipment slot) | 23/07/2026 | 23/07/2026 | State Machine design patterns |
| 5 | - Implement dynamic character statistics calculation (calculating final stats when items are equipped/unequipped) | 24/07/2026 | 24/07/2026 | Game stats calculation guidelines |
| 6 | - Integrate the inventory logic with Amazon DynamoDB transactions to update inventory arrays and player stats atomically | 25/07/2026 | 25/07/2026 | Amazon DynamoDB Transactions |

### Week 5 Achievements:

* **Comprehensive Item Data Models:** Designed and integrated clean item schemas supporting various item types and four rarity tiers. These models are packed into the shared library for client-backend parity.
* **Weighted Loot System:** Implemented a customizable Weighted Random Algorithm. Loot drops are calculated server-side based on probability matrices, and rewards (Gold/XP) adapt dynamically to the level of defeated bosses.
* **Capacity Limit Enforced:** Built API endpoints for inventory operations containing inventory limits check (max 100 items). Attempts to collect loot beyond capacity are blocked gracefully with client notifications.
* **Strict Equipment Logic:** Programmed backend logic enforcing unique equipment slots (Weapon, Armor, Accessory). Unequipping automatically handles moving items back to generic inventory slots.
* **Real-time Stat Synchronization:** Implemented character stat recalculations. Equipping a Rare/Epic item instantly applies stat buffs to the character profile, and updates are committed atomically to DynamoDB to prevent state desynchronization.
