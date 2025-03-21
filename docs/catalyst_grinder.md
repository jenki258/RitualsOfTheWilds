### File Creation Instructions for Catalyst Grinder

To create and configure a new Catalyst Grinder recipe, follow these steps:

1. **Create the Recipe File**:
   - Go to `config/Rituals_of_the_wilds/catalyst_grinder/`.
   - Create a new JSON file named `4catalystgrinderrecipe.json`.
        - The number **must be 500 or lower**.  
        - The number **must be the next available number** (e.g., if the highest number is `3catalystgrinderrecipe.json`, name your file `4catalystgrinderrecipe.json`).  
   
2. **File Structure**:
   The contents of the `3catalystgrinderrecipe.json` file should look like this:

```json
{
  "Needed Item ID or Tag": "minecraft:ender_pearl",
  "Result Item ID": "rituals_of_the_wilds:ender_catalyst",
  "Clicks Needed": 5
}
```
or you can use this template

### Description of Fields:
- `"Needed Item ID or Tag"` → This specifies the **item or tag** that you need to provide to the Catalyst Grinder to begin the process (e.g., `minecraft:ender_pearl`).
- `"Result Item ID"` → This defines the **resulting item** from the Catalyst Grinder (e.g., `rituals_of_the_wilds:ender_catalyst`).
- `"Clicks Needed"` → This specifies the number of **clicks** required on the Catalyst Grinder for the recipe to complete (e.g., `5` clicks).

### Important Configuration Setting:
- **Regenerating Recipes**: If you have **already modified** the Catalyst Grinder recipe files and **don't want them to reset** when the game reloads, you **must** disable the `Regenerate Catalyst Grinder recipes` option in the `config/Rituals_of_the_wilds.toml` file.
  - Set the line `"Regenerate Catalyst Grinder recipes" = false` in the `.toml` file.
  - This ensures that the recipes you add or modify will **not be overwritten** by default recipes when the game restarts.

### Where to Find This Setting:
- Open `config/Rituals_of_the_wilds.toml`.
- Search for the setting: 
  ```toml
  Regenerate Catalyst Grinder recipes = true
  ```
- Change it to:
  ```toml
  Regenerate Catalyst Grinder recipes = false
  ```
- This will prevent the game from automatically regenerating the recipes back to their default state.

### Example Process for Recipe Setup:

1. **Locate the Folder**: `config/Rituals_of_the_wilds/catalyst_grinder/`
2. **Create the File**: `4catalystgrinderrecipe.json`
3. **Paste Recipe Structure**:
   ```json
   {
     "Needed Item ID or Tag": "minecraft:ender_pearl",
     "Result Item ID": "rituals_of_the_wilds:ender_catalyst",
     "Clicks Needed": 5
   }
   ```

4. **Adjust the Config**:  
   In `config/Rituals_of_the_wilds.toml`, set the following:
   ```toml
   Regenerate Catalyst Grinder recipes = false
   ```
