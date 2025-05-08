# 📜 Dialogue System - Rituals Of The Wilds

This document explains the structure and usage of dialogue JSON files used by the **Rituals of the Wilds** mod. These files define interactions between players and entities (like NPCs), including branching dialogues, quests, and in-game commands.

In `config/Rituals_of_the_wilds.toml`, set the following:
   ```toml
   Regenerate Dialogues = false
   ```

---

## 📁 File Naming Convention and placement where

Dialogue file needs to be placed in `/config/Rituals_of_the_wilds/dialogues/eng/`

Each dialogue file should follow this format:

```

modid_entityid_dialogueid.json

```

**Example:**
```

rituals_of_the_wilds_chernobog_1.json

````

---

## 🗨️ Dialogue File Structure

### 🔁 First Dialogue Based with Reputation

- **Type:** `boolean`
- **Description:**  
  - If `true`, the dialogue system will use the player’s **reputation** with the entity to choose which dialogue file to load (e.g., ending in `_1` to `_5`).
  - If `false`, it directly uses the `_1` file without reputation check.

---

### 📊 Reputation Fields

Only relevant if `"First dialogue Based with reputation"` is `true`. These fields define fallback dialogues for each reputation tier:

- `"Bad Reputation"` - `_1`
- `"Neutral Reputation"` - `_2`
- `"Normal Reputation"` - `_3`
- `"Good Reputation"` - `_4`
- `"High Reputation"` - `_5`

---

### 📝 Text Line

- **Type:** `string`
- **Max length:** `750 characters`
- **Description:**  
  The main text displayed in the dialogue window.  
  Supports tags:
  - `<playername>` → Replaced with the player's name
  - `<entityname>` → Replaced with the name of the entity being interacted with

---

### 🎯 Answer Sections

There are four possible answer slots: **First**, **Second**, **Third**, **Fourth**

Each answer contains the following properties:

#### ✅ Answer Text Line
- **Type:** `string`
- **Max length:** Unlimited (note: long text may go off-screen)
- **Tags supported:** `<playername>`, `<entityname>`

#### 🎒 Answer Quest Requirement
- **Type:** `string` (Quest ID)
- **Description:**  
  Quest required for this answer to be shown or hidden.

#### 📌 Answer Requirement State
- **Type:** `integer` (0–5)
- **Values:**
  - `0` → Show if quest is **done**
  - `1` → Hide if quest is **done**
  - `2` → Show if quest is **done or in progress**
  - `3` → Hide if quest is **done or in progress**
  - `4` → Show if quest is **in progress**
  - `5` → Hide if quest is **in progress**

#### 🔀 Answer Result Dialogue Number
- **Type:** `integer`
- **Description:**  
  The ID of the dialogue file to go to after this answer is selected.  
  - `0` means the dialogue will **close**.

#### 💻 Answer Result Command
- **Type:** `string`
- **Description:**  
  Command to be executed after selecting this answer.  
  Supports:
  - `<player_id>` → Replaced with player's UUID
  - `<entity_id>` → Replaced with NPC's entity ID

#### 🧠 Result Command Executor
- **Type:** `integer`
- **Values:**
  - `0` → Player executes the command
  - `1` → Command runs at the world position (no executor)
  - `2` → Entity (NPC) executes the command

#### 🎁 Answer Result Quest Give ID
- **Type:** `string` (Quest ID)
- **Description:**  
  Quest to be given upon selecting this answer.

#### 🔊 Answer Sound
- **Type:** `string` (Command format)
- **Description:**  
  Sound command always executed **as player**.  
  Does not support `<player_id>` or `<entity_id>`.

---

## 📂 Example Dialogue File

```json
{
  "First dialogue Based with reputation": false,
  "Bad Reputation": 0,
  "Neutral Reputation": 0,
  "Normal Reputation": 0,
  "Good Reputation": 0,
  "High Reputation": 0,
  "Text Line": "",
  "First Answer Text Line": "》Hi",
  "First Answer Quest Requirement": "",
  "First Answer Quest Requirement State": 1,
  "First Answer Result Dialogue Number": 2,
  "First Answer Result Command": "",
  "First Answer Result Command Player, World or Entity Executed": 0,
  "First Answer Result Quest Give ID": "",
  "First Answer Sound": "",
  "Second Answer Text Line": "》Bye",
  "Second Answer Quest Requirement": "",
  "Second Answer Quest Requirement State": 1,
  "Second Answer Result Dialogue Number": 0,
  "Second Answer Result Command": "",
  "Second Answer Result Command Player, World or Entity Executed": 0,
  "Second Answer Result Quest Give ID": "",
  "Second Answer Sound": "",
  "Third Answer Text Line": "》 ",
  "Third Answer Quest Requirement": "",
  "Third Answer Quest Requirement State": 1,
  "Third Answer Result Dialogue Number": 0,
  "Third Answer Result Command": "",
  "Third Answer Result Command Player, World or Entity Executed": 0,
  "Third Answer Result Quest Give ID": "",
  "Third Answer Sound": "",
  "Fourth Answer Text Line": "",
  "Fourth Answer Quest Requirement": "",
  "Fourth Answer Quest Requirement State": 1,
  "Fourth Answer Result Dialogue Number": 0,
  "Fourth Answer Result Command": "",
  "Fourth Answer Result Command Player, World or Entity Executed": 0,
  "Fourth Answer Result Quest Give ID": "",
  "Fourth Answer Sound": ""
}
````

---

## ❗ Notes

* Commands must be valid for/in Minecraft.
* BE AWARE DO NOT DELETE ANY PARAMETER EVEN IF IT'S EMPTY! (It will just crash the game)
* All dialogue transitions must refer to valid, existing dialogue files.
* Use dialogue IDs consistently to avoid logic errors in branching.

---

🔧 For bug reports or feature suggestions, please visit [JenkiMods Discord](https://discord.gg/bJWbUsWAWk)
