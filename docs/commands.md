# 🛠️ Rituals Of The Wilds - Command List

Below are the available commands for managing quests, reputation, rituals, and alchemy scrolls within the *Rituals Of The Wilds* mod. Use these commands to customize your gameplay experience or manage entities and quests in your world.

---

## ⚖️ Reputation Management

### `/reputationset <Reputation entity> <Player> <reputation_number>`
- **Description:** Sets the reputation of an entity for a specific player.
- **Arguments:**
  - `<Reputation entity>`: The entity whose reputation is being modified.
  - `<Player>`: The player whose reputation with the entity is being set.
  - `<reputation_number>`: The reputation value (e.g., -5, 0, 5).

### `/reputationadd <Reputation entity> <Player> <reputation_number>`
- **Description:** Adds a certain amount of reputation to an entity for a player.
- **Arguments:**
  - `<Reputation entity>`: The entity whose reputation is being added to.
  - `<Player>`: The player whose reputation with the entity will be increased.
  - `<reputation_number>`: The amount of reputation to add.

### `/reputationsdecrease <Reputation entity> <Player> <reputation_number>`
- **Description:** Decreases a certain amount of reputation from an entity for a player.
- **Arguments:**
  - `<Reputation entity>`: The entity whose reputation is being decreased.
  - `<Player>`: The player whose reputation with the entity will be decreased.
  - `<reputation_number>`: The amount of reputation to remove.

---

## 🎮 Quest Management

### `/rituals_of_the_wilds:givequest <given_by> <giving_to> <Quest_id>`
- **Description:** Gives a specific quest to a player or entity.
- **Arguments:**
  - `<given_by>`: The entity or NPC giving the quest.
  - `<giving_to>`: The player or entity receiving the quest.
  - `<Quest_id>`: The ID of the quest to be given.

### `/rituals_of_the_wilds:removequest <removing_from> <Quest_id>`
- **Description:** Removes a specific quest by its ID from a player or entity.
- **Arguments:**
  - `<removing_from>`: The entity or player from whom the quest is being removed.
  - `<Quest_id>`: The ID of the quest to remove.

### `/rituals_of_the_wilds:removequestbyslot <removing_from> <Quest Slot>`
- **Description:** Removes a quest by its slot from a player or entity.
- **Arguments:**
  - `<removing_from>`: The entity or player from whom the quest is being removed.
  - `<Quest Slot>`: The slot number of the quest to remove.

### `/rituals_of_the_wilds:removealldonequests <entity_removing_from>`
- **Description:** Removes all completed quests from the specified entity's done quest list.
- **Arguments:**
  - `<entity_removing_from>`: The entity or player from whom all completed quests are being removed.

### `/rituals_of_the_wilds:removedonequest <entity_removing_from> <Quest_ID>`
- **Description:** Removes a specific quest ID from the entity's list of completed quests.
- **Arguments:**
  - `<entity_removing_from>`: The entity or player from whom the quest is being removed.
  - `<Quest_ID>`: The ID of the quest to be removed.

### `/rituals_of_the_wilds:adddonequest <giving_to> <quest_id>`
- **Description:** Adds a quest to the done list of a player or entity (even if the quest is not in the quest folder).
- **Arguments:**
  - `<giving_to>`: The entity or player to whom the quest is being marked as completed.
  - `<quest_id>`: The ID of the quest to add to the done list.

---

## 🧙‍♂️ Ritual Scroll Management

### `/giveritualscroll <giving_to> <scroll_id>`
- **Description:** Gives a ritual scroll with a specific ID to an entity or player.
- **Arguments:**
  - `<giving_to>`: The entity or player to receive the ritual scroll.
  - `<scroll_id>`: The ID of the ritual scroll to give.

### `/rituals_of_the_wilds:removeallritualscrollsseen <removing_from>`
- **Description:** Removes all ritual scrolls from the "seen" list of an entity or player.
- **Arguments:**
  - `<removing_from>`: The entity or player from whom all ritual scrolls are being removed from the seen list.

### `/rituals_of_the_wilds:removeritualscrollseen <removing_from> <scroll_id>`
- **Description:** Removes a specific ritual scroll ID from the "seen" list of an entity or player.
- **Arguments:**
  - `<removing_from>`: The entity or player from whom the ritual scroll is being removed.
  - `<scroll_id>`: The ID of the ritual scroll to be removed.

---

## 🧪 Alchemy Scroll Management

### `/rituals_of_the_wilds:removeallalchemyscrollsseen <removing_from>`
- **Description:** Removes all alchemy scrolls from the "seen" list of an entity or player.
- **Arguments:**
  - `<removing_from>`: The entity or player from whom all alchemy scrolls are being removed from the seen list.

### `/rituals_of_the_wilds:removealchemyscrollseen <removes_from> <scroll_id>`
- **Description:** Removes a specific alchemy scroll ID from the "seen" list of an entity or player.
- **Arguments:**
  - `<removes_from>`: The entity or player from whom the alchemy scroll is being removed.
  - `<scroll_id>`: The ID of the alchemy scroll to be removed.

### `/givealchemyscroll <giving_to> <scroll_id>`
- **Description:** Gives an alchemy scroll with a specific ID to an entity or player.
- **Arguments:**
  - `<giving_to>`: The entity or player to receive the alchemy scroll.
  - `<scroll_id>`: The ID of the alchemy scroll to give.

---

🎮 **Tip:** These commands can be useful for server administrators, modders, and anyone wanting to modify or customize the quest and ritual systems dynamically.

For more help, feel free to join the [JenkiMods Discord](https://discord.gg/bJWbUsWAWk).

