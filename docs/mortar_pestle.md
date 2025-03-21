### File Creation Instructions for Mortar and Pestle Recipe

1. **Create the Recipe File**:
   - Navigate to the folder: `config/Rituals_of_the_Wilds/Mortar_and_Pestle/`.
   - Create a new JSON file named `6mortarrecipe.json`.
        - The number **must be 500 or lower**.  
        - The number **must be the next available number** (e.g., if the highest number is `6mortarrecipe.json`, name your file `7mortarrecipe.json`).  
2. **File Structure**:
   The contents of the `6mortarrecipe.json` file should look like this:

```json
{
  "Needed Item ID or Tag": "rituals_of_the_wilds:cryorite_gem",
  "Result Item ID": "rituals_of_the_wilds:cryorite_powder",
  "Give Fixed Amount": true,
  "Min/Fixed Give amount": 1,
  "Max Give amount": 1
}
```
or you can use this [template](../config/Rituals_of_the_wilds/Mortar_and_Pestle/1mortarrecipe.json)

### Description of Fields:
- `"Needed Item ID or Tag"` → Specifies the **item** that will be processed in the mortar and pestle. In this case, `rituals_of_the_wilds:cryorite_gem` is required to be placed into the mortar.
- `"Result Item ID"` → Defines the **resulting item** after processing. In this case, `rituals_of_the_wilds:cryorite_powder` will be the resulting item.
- `"Give Fixed Amount"` → If `true`, the **amount of the result** is fixed. In this case, it will always give 1 item.
- `"Min/Fixed Give amount"` & `"Max Give amount"` → The exact number of result items given when the recipe is used. Since the recipe gives a fixed amount, both values will be set to `1`.

### Configuration Settings:

To manage whether the recipe should regenerate automatically when the game starts, you'll need to modify the `"Regenerate Mortar and Pestle recipes"` configuration setting.

- **Auto Regenerate Mortar and Pestle Recipes**: To disable the automatic regeneration of recipes, open `config/Rituals_of_the_Wilds.toml` and find the setting:
  ```toml
  Regenerate Mortar and Pestle recipes = true
  ```
- Change it to:
  ```toml
  Regenerate Mortar and Pestle recipes = false
  ```
  This ensures that custom recipes will not be overwritten by default.

### Full Setup Process:

1. **Navigate to the Folder**: `config/Rituals_of_the_Wilds/Mortar_and_Pestle/`
2. **Create the Recipe File**: `6mortarrecipe.json`
3. **Recipe Content**:
   ```json
   {
     "Needed Item ID or Tag": "rituals_of_the_wilds:cryorite_gem",
     "Result Item ID": "rituals_of_the_wilds:cryorite_powder",
     "Give Fixed Amount": true,
     "Min/Fixed Give amount": 1,
     "Max Give amount": 1
   }
   ```

4. **Update Config**:
   Open `config/Rituals_of_the_Wilds.toml`, find:
   ```toml
   Regenerate Mortar and Pestle recipes = true
   ```
   Change it to:
   ```toml
   Regenerate Mortar and Pestle recipes = false
   ```

### Final Notes:
- With `"Give Fixed Amount": true`, the result amount is always fixed, ensuring that players receive a consistent number of result items.
- You can adjust the `"Min/Fixed Give amount"` and `"Max Give amount"` if you later want to change the amount given per recipe execution.

This setup will successfully add your custom Mortar and Pestle recipe while preventing auto-regeneration from overriding it.
