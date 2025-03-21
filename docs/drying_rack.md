### File Creation Instructions for Drying Rack Recipe

1. **Create the Recipe File**:
   - Navigate to the folder: `config/Rituals_of_the_wilds/Drying_Rack/`.
   - Create a new JSON file named `15dryingrecipe.json`.
        - The number **must be 500 or lower**.  
        - The number **must be the next available number** (e.g., if the highest number is `15dryingrecipe.json`, name your file `16dryingrecipe.json`).  

2. **File Structure**:
   The contents of the `15dryingrecipe.json` file should look like this:

```json
{
  "Needed Item ID or Tag": "rituals_of_the_wilds:blood_fern",
  "Drying Result Item ID": "rituals_of_the_wilds:dried_blood_fern"
}
```
or you can use this [template](../config/Rituals_of_the_wilds/Drying_Rack/1distilationflaskrecipe.json)

---

## !!**Also when you are adding new item ingredient to the recipes and it's not in ingredient's for drying rack just add it in there and make them unregeneratable here how to do it **[Interactive Crafting Guide](docs/interactive_crafting.md)**.**!!

---

### Description of Fields:
- `"Needed Item ID or Tag"` → Specifies the **item or tag** that will be placed on the Drying Rack for processing. In this case, it's `rituals_of_the_wilds:blood_fern`.
- `"Drying Result Item ID"` → Defines the **resulting item** that will be produced after the drying process. For example, `rituals_of_the_wilds:dried_blood_fern` will be the result after drying the `blood_fern`.

### Important Configuration Setting:
- **Auto Regenerate Drying Rack Recipes**: To prevent the game from overwriting your custom Drying Rack recipes, disable the `"Auto Regenerate Drying Rack recipes"` option in the `config/Rituals_of_the_Wilds.toml` file.
  - Set it to `false`:
  ```toml
  Auto Regenerate Drying Rack recipes = false
  ```
  This ensures that your custom recipes won't be automatically reset when the game reloads.

### Where to Find This Setting:
- Open `config/Rituals_of_the_wilds.toml`.
- Search for the setting:
  ```toml
  Auto Regenerate Drying Rack recipes = true
  ```
- Change it to:
  ```toml
  Auto Regenerate Drying Rack recipes = false
  ```

### Example Process for Recipe Setup:

1. **Locate the Folder**: `config/Rituals_of_the_wilds/Drying_Rack/`
2. **Create the File**: `15dryingrecipe.json`
3. **Paste Recipe Structure**:
   ```json
   {
     "Needed Item ID or Tag": "rituals_of_the_wilds:blood_fern",
     "Drying Result Item ID": "rituals_of_the_wilds:dried_blood_fern"
   }
   ```

4. **Adjust the Config**:  
   In `config/Rituals_of_the_wilds.toml`, set the following:
   ```toml
   Auto Regenerate Drying Rack recipes = false
   ```
   Also you can adjust time that all of recipes require in config:
   ```toml
   "Drying Rack Time to Dry Item" = 4800.0
   ```

Now you’ve successfully created a Drying Rack recipe. If you need to add more recipes, follow the same steps and increment the JSON file number (e.g., `16dryingrecipe.json`, `17dryingrecipe.json`, etc.).
