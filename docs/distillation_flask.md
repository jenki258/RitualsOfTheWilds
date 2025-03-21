### File Creation Instructions for Distilation Flask Recipe

1. **Create the Recipe File**:
   - Go to `config/Rituals_of_the_wilds/distilation_flask/`.
   - Create a new JSON file named `2distilationflaskrecipe.json` (or increment the number if you already have other recipes in that folder).
        - The number **must be 500 or lower**.  
        - The number **must be the next available number** (e.g., if the highest number is `2distilationflaskrecipe.json`, name your file `3distilationflaskrecipe.json`).  
2. **File Structure**:
   The contents of the `2distilationflaskrecipe.json` file should look like this:

```json
{
  "Needed Item ID or Tag": "forge:dyes",
  "Needed Block ID or Tag under flask": "minecraft:blue_ice",
  "Result Item ID": "rituals_of_the_wilds:color_catalyst",
  "Distilation time(In ticks)": 80
}
```
or you can use this [template](../config/Rituals_of_the_wilds/distilation_flask/1distilationflaskrecipe.json)

### Description of Fields:
- `"Needed Item ID or Tag"` → Specifies the **item or tag** that is required to be used in the Distilation Flask (e.g., `forge:dyes` for any dye).
- `"Needed Block ID or Tag under flask"` → Specifies the **block** that must be placed **under** the flask for the recipe to work (e.g., `minecraft:blue_ice`).
- `"Result Item ID"` → Defines the **resulting item** that will be produced from the Distilation Flask (e.g., `rituals_of_the_wilds:color_catalyst`).
- `"Distilation time(In ticks)"` → This is the **time** (in ticks) it will take for the recipe to complete. For example, `80` ticks represent a small time duration for the distillation process.

---

## !!**Also when you are adding new item ingredient to the recipes and it's not in ingredient's for distilation flask just add it in there and make them unregeneratable here how to do it **[Interactive Crafting Guide](docs/interactive_crafting.md)**.**!!

---

### Important Configuration Setting:
- **Regenerating Recipes**: As with other recipes, to prevent the game from overwriting your custom Distilation Flask recipes, disable the `"Regenerate Distilation Flask recipes"` option in the `config/Rituals_of_the_wilds.toml` file.
  - Set it to `false`:
  ```toml
  Regenerate Distilation Flask recipes = false
  ```
  This ensures that any changes or custom recipes you make will not be automatically reset when the game reloads.

### Where to Find This Setting:
- Open `config/Rituals_of_the_wilds.toml`.
- Search for the setting:
  ```toml
  Regenerate Distilation Flask recipes = true
  ```
- Change it to:
  ```toml
  Regenerate Distilation Flask recipes = false
  ```

### Example Process for Recipe Setup:

1. **Locate the Folder**: `config/Rituals_of_the_wilds/distilation_flask/`
2. **Create the File**: `2distilationflaskrecipe.json`
3. **Paste Recipe Structure**:
   ```json
   {
     "Needed Item ID or Tag": "forge:dyes",
     "Needed Block ID or Tag under flask": "minecraft:blue_ice",
     "Result Item ID": "rituals_of_the_wilds:color_catalyst",
     "Distilation time(In ticks)": 80
   }
   ```

4. **Adjust the Config**:  
   In `config/Rituals_of_the_wilds.toml`, set the following:
   ```toml
   Regenerate Distilation Flask recipes = false
   ```

Now, you've successfully created and set up a Distillation Flask recipe! Make sure to follow the same process for adding additional recipes if needed.
