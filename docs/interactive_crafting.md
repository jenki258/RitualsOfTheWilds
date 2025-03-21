# Interactive Crafting & Jar Ingredients

In the `config/Rituals_of_the_wilds/` folder, there are several JSON files that define which ingredients can be used in different crafting blocks and jars. You can customize these lists by adding **item IDs** (e.g., `minecraft:carrot`) or **tags** (e.g., `forge:dyes`).  

However, **any changes you make will be reset** unless you disable the automatic regeneration settings in the main configuration file.  

---

## 📁 Ingredient Configuration Files  

Located in `config/Rituals_of_the_wilds/`:  

- `alchemy_cauldron_ingredients.json` → Defines allowed ingredients for the **Alchemy Cauldron**  
- `can_be_putted_in_jars.json` → Controls what items can be placed in **Jars**  
- `catalyst_grinder_ingredients.json` → Defines valid catalysts for the **Catalyst Grinder**  
- `distilation_ingredients.json` → Specifies items usable in the **Distillation Flask**  
- `drying_rack_ingredients.json` → Determines what can be dried on the **Drying Rack**  
- `fume_extractor_ingredients.json` → Lists materials for the **Fume Extractor**  

---

## ⚙️ Preventing Reset of Custom Changes  

By default, the game **automatically regenerates these ingredient files**, resetting any custom edits.  
To stop this, you need to **disable the auto-regeneration settings** in the `config/Rituals_Of_The_Wilds.toml` file.

### Steps:  
1. Open `config/Rituals_Of_The_Wilds.toml`  
2. Find the following settings:  
   - `"Auto Regenerate Ingredients possible to put in some blocks"`  
   - `"Regenerate Items that you can put in jars"`  
3. Change both values to `false`:  

No restart is required! These settings apply immediately while the game is running.

```toml
"Auto Regenerate Ingredients possible to put in some blocks" = false
"Regenerate Items that you can put in jars" = false
