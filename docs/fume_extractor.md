To create a **Fume Extractor recipe** for the `Rituals_of_the_Wilds` mod, follow these steps to create the appropriate JSON file and adjust the configuration.

### File Creation Instructions for Fume Extractor Recipe

1. **Create the Recipe File**:
   - Navigate to the folder: `config/Rituals_of_the_wilds/fume_extractor/`.
   - Create a new JSON file named `4fumeextractorrecipe.json`.
        - The number **must be 500 or lower**.  
        - The number **must be the next available number** (e.g., if the highest number is `4fumeextractorrecipe.json`, name your file `5fumeextractorrecipe.json`).  

2. **File Structure**:
   The contents of the `4fumeextractorrecipe.json` file should look like this:

```json
{
  "Needed Item ID or Tag": "minecraft:poppy",
  "Needed Fuel ID or Tag": "rituals_of_the_wilds:fumes_bottle",
  "Result Item ID": "rituals_of_the_wilds:poppy_fumes",
  "Particles ID": "minecraft:falling_water",
  "Extracting time(In ticks)": 120
}
```
or you can use this [template](../config/Rituals_of_the_wilds/fume_extractor/1fumeextractorrecipe.json)

---

## !!**Also when you are adding new item ingredient or fuelt to the recipes and it's not in ingredient's for fume extractor just add it in there and make them unregeneratable here how to do it **[Interactive Crafting Guide](docs/interactive_crafting.md)**.**!!

---

### Description of Fields:
- `"Needed Item ID or Tag"` → Specifies the **item** that will be extracted for its fumes. In this case, the item is `minecraft:poppy`.
- `"Needed Fuel ID or Tag"` → Defines the **fuel** that is required to extract the fumes. For example, `rituals_of_the_wilds:fumes_bottle` will be used as fuel in this process.
- `"Result Item ID"` → Specifies the **resulting item** after the extraction. For this recipe, `rituals_of_the_wilds:poppy_fumes` will be produced.
- `"Particles ID"` → The **particle effect** displayed during the extraction process. In this case, `minecraft:falling_water` will be shown as the particles.
- `"Extracting time(In ticks)"` → Specifies the **time** in ticks (Minecraft's in-game time, where 1 tick = 1/20th of a second) it will take for the extraction to complete. For this recipe, it's 120 ticks.

### Important Configuration Setting:
- **Auto Regenerate Fume Extractor Recipes**: To prevent the game from overwriting your custom Fume Extractor recipes, disable the `"Auto Regenerate Fume Extractor recipes"` option in the `config/Rituals_of_the_Wilds.toml` file.
  - Set it to `false`:
  ```toml
  Auto Regenerate Fume Extractor recipes = false
  ```
  This ensures that your custom recipes won't be automatically reset when the game reloads.

### Where to Find This Setting:
- Open `config/Rituals_of_the_wilds.toml`.
- Search for the setting:
  ```toml
  Auto Regenerate Fume Extractor recipes = true
  ```
- Change it to:
  ```toml
  Auto Regenerate Fume Extractor recipes = false
  ```

### Example Process for Recipe Setup:

1. **Locate the Folder**: `config/Rituals_of_the_wilds/fume_extractor/`
2. **Create the File**: `4fumeextractorrecipe.json`
3. **Paste Recipe Structure**:
   ```json
   {
     "Needed Item ID or Tag": "minecraft:poppy",
     "Needed Fuel ID or Tag": "rituals_of_the_wilds:fumes_bottle",
     "Result Item ID": "rituals_of_the_wilds:poppy_fumes",
     "Particles ID": "minecraft:falling_water",
     "Extracting time(In ticks)": 120
   }
   ```

4. **Adjust the Config**:  
   In `config/Rituals_of_the_wilds.toml`, set the following:
   ```toml
   Auto Regenerate Fume Extractor recipes = false
   ```

### Notes:
- You can modify the `Particles ID` to a different effect if desired, using any available particle effect in Minecraft.
- Adjust the `"Extracting time(In ticks)"` to make the process faster or slower depending on your preference.
- You can continue to create additional Fume Extractor recipes by incrementing the file names (e.g., `5fumeextractorrecipe.json`, `6fumeextractorrecipe.json`, etc.) in the same folder.

By following this structure, you’ll have successfully set up the Fume Extractor recipe in your game!
