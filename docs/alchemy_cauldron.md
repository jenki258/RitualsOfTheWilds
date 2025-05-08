# 🧪 Alchemy Cauldron - Custom Recipes

The Alchemy Cauldron in **Rituals Of The Wilds** allows you to create powerful items or execute commands through custom recipes. There are **two types** of Alchemy Cauldron recipes:  
1. **Item-Giving Recipes** – Produces an item as a result.  
2. **Command-Execution Recipes** – Runs a command instead of giving an item.  

---

## ⚠️ Important: Avoiding Game Crashes  

**Incorrect settings can cause the game to crash!**  
Make sure that when `"Execute Command Insted of Giving Item"` is set to `true`, all necessary command-related values are properly set.  

🚨 **Game will crash if:**  
❌ `"Execute Command Insted of Giving Item": true` but **values like `"Fixed or Random Amount"` are still used (which are for items only).**

❌ Somewhere was missed "," sign

❌ Somewhere was missed line of the template json(Even if it's an empty thing)

✅ **How to prevent crashes:**  
- If **giving an item**, set:  
  ```json
  "Execute Command Insted of Giving Item": false,
  "Fixed or Random Amount": false,
  "Result item ID": "minecraft:golden_apple",
  "Min/Fixed result item give count": 1,
  "Max result item give count": 2
  ```
- If **executing a command**, set:  
  ```json
  "Execute Command Insted of Giving Item": true,
  "Result Command": "execute at @p run say Hello!",
  "Fixed or Random Execution": false,
  "Execute as player": false,
  "Min/Fixed result execution count": 1,
  "Max result execution count": 2
  ```

---

## !!**Also when you are adding new item ingredient to the recipes and it's not in ingredient's for cauldron just add it in there and make them unregeneratable here how to do it **[Interactive Crafting Guide](docs/interactive_crafting.md)**.**!!

---

## 📂 Editing Existing Recipes  

By default, all recipes are stored in:  
📁 `config/Rituals_of_the_wilds/Alchemy_Cauldron/eng/`  

### ⚠️ Preventing Recipe Reset  
If you modify an existing recipe but don't want it to reset back to default, you must **disable auto-regeneration** in the main config file:  

1. Open `config/Rituals_Of_The_Wilds.toml`  
2. Find this setting:  
   ```toml
   "Auto Regenerate Alchemy Cauldron recipes" = true
   ```  
3. Change it to `false`:  
   ```toml
   "Auto Regenerate Alchemy Cauldron recipes" = false
   ```
4. **No restart is needed!** The setting takes effect immediately.

---

## 📜 Creating a New Recipe  

To add a new Alchemy Cauldron recipe:  

1. Go to **`config/Rituals_of_the_wilds/Alchemy_Cauldron/eng/`**  
2. Create a new file with a **numbered filename** (e.g., `4alchemyrecipe.json`).  
   - The number **must be 500 or lower**.  
   - The number **must be the next available number** (e.g., if the highest number is `3alchemyrecipe.json`, name your file `4alchemyrecipe.json`).  

---

## 🔹 Item-Giving Recipe Format  

An **Item-Giving Recipe** will return an item when the correct ingredients are used.  

### 📝 Example [Item-Giving Recipe](../config/Rituals_of_the_wilds/Alchemy_Cauldron/1alchemyrecipe.json)

---

## 🔹 Command-Execution Recipe Format  

Instead of giving an item, this recipe **executes a command** when the correct ingredients are used.  

### 📝 Example [Command-Execution Recipe](../config/Rituals_of_the_wilds/Alchemy_Cauldron/2alchemyrecipe.json)

---

### **Summary of Key Fields**

---

- **`"Moon Stage Needed": false`** → **Whether a specific moon stage is required** for the ritual. If `true`, the ritual only works on certain moon phases.
  
- **`"Moon Stage": 0`** → **Specifies which moon phase is required** (0 represents the full moon, following the exact Minecraft moon phases without the +1 offset).

- **`"Runes on cauldron needed": false`** → **Checks if the cauldron has special runes applied to it**, marking it as a "coated" cauldron. If `true`, the ritual requires the cauldron to be in this special state.

- **`"Cauldron Fill Type": 0`** → Defines the **type of filling in the cauldron**:
  - `0`: Empty
  - `1`: Water
  - `2`: Lava
  
- **`"Check for blocks around": false`** → **Checks the surrounding blocks** to see if specific conditions are met (e.g., special structures, runes, etc.) in the area around the cauldron.

- **`"Remove blocks when used": false`** → **Determines whether blocks should be removed** when the ritual is performed. 
  - If `true`, the blocks are replaced or cleared according to the block replacement rules.

- **`"Block X-3 ID Or Tag": ""`** → **Defines a block ID or tag** at the relative position X-3 that must be present for the ritual to succeed.

- **`"Block X+3 ID Or Tag": ""`** → Similar to the previous block, but checks at position X+3. Used to verify specific blocks in the surrounding area.

- **`"Replacement Block X-3 ID": ""`** → **Specifies the block** that will replace the one at position X-3 if the ritual condition is met.

- **`"Ingredient ID or Tag 1" to "Ingredient ID or Tag 10"`** → **Lists the required ingredients** for the ritual, in a specific order. The ingredients **must be placed in the exact order** with no gaps, from 1 to 10.

- **`"Execute Command Instead of Giving Item": true`** → **Ensures the cauldron runs a command** instead of returning an item. If `true`, the ritual will trigger a command execution instead of giving the player a result item.

- **`"Execute as player"`** → If `true`, the command will execute **as the player**, allowing player-specific coordinates and actions. If `false`, the command will execute at the block or world level (not as a player).

- **`"Result Command"`** → **Specifies the command** that will run when the recipe is used. For example, this could be something like `summon lightning` or any other command.

- **`"Min/Fixed result execution count"` & `"Max result execution count"`** → **Defines how many times the command will execute**. The count can range from a fixed value to a random amount, depending on the settings.

- **`"Check for Blocks +2Y(Only works with Check for blocks around true)": false`** → If `true`, checks for blocks **2 blocks above the cauldron** (Y+2) in addition to the standard checks around the cauldron. Only works if `Check for blocks around` is `true`.

- **`"Remove upper blocks when used": false`** → If `true`, it removes blocks **above the cauldron** when the ritual is executed (similar to how the "Remove blocks when used" works).

- **`"Block X-3 Y+2 ID Or Tag" to "Replacement Block X-2 Y+2 Z-2 ID"`** → These fields allow checking and replacing **upper blocks** (Y+2), which are positioned above the cauldron, based on their IDs or tags.

- **`"Min/Fixed result item give count"` & `"Max result item give count"`** → **Defines the number of items** the ritual will return (between the minimum and maximum values).

---

## ✅ Summary  

- **To modify an existing recipe**, edit the JSON files inside `config/Rituals_of_the_wilds/Alchemy_Cauldron/eng/`.  
- **To prevent recipe resets**, turn off `"Auto Regenerate Alchemy Cauldron recipes"` in the `toml` config file.  
- **To add a new recipe**, create a new numbered JSON file (`Xalchemyrecipe.json`).  
- **Choose between giving an item or executing a command** by setting `"Execute Command Insted of Giving Item"` to `true` or `false`.  
- **Check settings carefully** to avoid crashes when making command-based recipes!  

🚀 **Now you’re ready to customize the Alchemy Cauldron to your liking!**  
