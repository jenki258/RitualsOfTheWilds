# 🧭 Quest System - Rituals Of The Wilds

This document describes how to configure **Quest JSON files** for the *Rituals of the Wilds* mod. Quests are used to create task-based progression, including item delivery, entity interactions, and combat challenges.

---

## 📁 File Location

Quest files must be placed in:

```

/config/Rituals_of_the_wilds/quests/eng/

````

> ✅ **Important:** Use **long and unique filenames**. Short names may conflict (e.g., `"long.json"` and `"on.json"`), causing false-positive completions.

---

## 🧩 Supported Quest Types

| Type | Description                          |
|------|--------------------------------------|
| `1`  | **Give item to quest giver**         |
| `2`  | **Deliver item to another entity**   |
| `3`  | **Kill a specific entity**           |

> ❗ **Never modify the `Quest Type` after creation** — doing so will crash the game.

---

## 📄 General Structure

Each quest JSON shares many common fields. Depending on the quest type, some fields are required and others are ignored.

### 🔤 Common Fields (All Types)

| Field | Description |
|-------|-------------|
| `"Quest name"` | Displayed quest title. Supports `<playername>` |
| `"Text Line"` | Quest description (max 148 characters). Supports `<playername>` |
| `"Quest After Finishing Text"` | Message sent on completion: `"<entityname>: <text>"` |
| `"Quest Finishing Sound"` | A command (e.g. `/playsound`) executed **as the player** |
| `"Quest Reward Item ID"` | Item given as reward |
| `"Quest Reward Min Give Amount"` | Min item reward quantity |
| `"Quest Reward Max Give Amount"` | Max item reward quantity |
| `"Quest Reward Command"` | Command executed upon completion |
| `"Quest Reward Command Execution Type"` | `0` = world, `1` = player, `2` = quest entity |
| `"Quest Reward Min Command Execution"` | Min times to run command |
| `"Quest Reward Max Command Execution"` | Max times to run command |
| `"Quest Reputation Reward"` | How much reputation to give/take |
| `"Quest Reputation Source"` | `0` = completion entity, `1` = previous quest giver, `2` = original quest giver |
| `"Next Quest ID"` | ID of next quest to auto-give after completion |
| `"Next Quest Giver"` | From whom next quest will be received (`0`, `1`, or `2` as above) |

---

## 📦 Type 1 – Give Item to Quest Giver

```json
{
  "Quest Type": 1,
  "Quest Item ID or Tag": "minecraft:apple",
  "Quest Item Count": 5
}
````

Deliver the required number of items **directly** to the quest-giving entity.

---

## ✉️ Type 2 – Deliver to Another Entity

```json
{
  "Quest Type": 2,
  "Delivery Target Entity ID or Tag": "villager",
  "Quest Item ID or Tag": "minecraft:book",
  "Quest Item Count": 1
}
```

Deliver items to a **different target entity**, identified by ID or tag.

---

## ☠️ Type 3 – Kill a Target Entity

```json
{
  "Quest Type": 3,
  "Kill Target Entity ID or Tag": "zombie",
  "Kill count": 10
}
```

Kill a number of specific entities to complete the quest.

---

## 🧪 Example Full Quest Files

[Type 1](../config/Rituals_of_the_wilds/quests/eng/quest_give)

[Type 2](../config/Rituals_of_the_wilds/quests/eng/quest_delivery)

[Type 3](../config/Rituals_of_the_wilds/quests/eng/quest_kill)

---

## ⚠️ Tips & Warnings

* 🎯 Do **not** change the `Quest Type` once the file is created.
* 🧾 Use consistent and descriptive filenames to prevent cross-reference bugs.
* 💬 Messages, rewards, and transitions allow immersive and flexible progression chains.

---

📣 For support or sharing your creations, join the [JenkiMods Discord](https://discord.gg/bJWbUsWAWk).
