### File Creation Instructions for Rune Scribing Table Recipe

1. **Create the Recipe File**:
   - Go to `config/Rituals_of_the_wilds/rune_scribing_table/`.
   - Create a new JSON file named `1_1runescribingtablerecipe.json` (or increment the number if you already have other recipes in that folder).
        - The number **must be 500 or lower**.  
        - The number **must be the next available number** (e.g., if the highest number is `1_1runescribingtablerecipe.json`, name your file `2_1runescribingtablerecipe.json`).  
2. **File Structure**:
   The contents of the `1_1runescribingtablerecipe.json` file should look like this:

#### Contents of the File:
```json
{
  "Needed Item ID Or Tag": "rituals_of_the_wilds:wooden_rune_base",
  "Result slot 1 item ID": "rituals_of_the_wilds:wooden_rune_m",
  "Result slot 2 item ID": "rituals_of_the_wilds:wooden_rune_c",
  "Result slot 3 item ID": "rituals_of_the_wilds:wooden_rune_a",
  "Result slot 4 item ID": "rituals_of_the_wilds:wooden_rune_r",
  "Result slot 5 item ID": "rituals_of_the_wilds:wooden_rune_n",
  "Result slot 6 item ID": "rituals_of_the_wilds:wooden_rune_k",
  "Result slot 7 item ID": "rituals_of_the_wilds:wooden_rune_t",
  "Result slot 8 item ID": "rituals_of_the_wilds:wooden_rune_s",
  "Result slot 9 item ID": "rituals_of_the_wilds:wooden_rune_v",
  "Result slot 10 item ID": "rituals_of_the_wilds:wooden_rune_b",
  "Result slot 11 item ID": "rituals_of_the_wilds:wooden_rune_u",
  "Result slot 12 item ID": "rituals_of_the_wilds:wooden_rune_l"
}
```
or you can use this [template](../config/Rituals_of_the_wilds/rune_scribing_table/1_1runescribingtablerecipe.json)

### Key Fields Breakdown:
- `"Needed Item ID Or Tag"` → Specifies the **item** that is required to craft the rune set. In this case, it is `rituals_of_the_wilds:wooden_rune_base`.
- `"Result slot X item ID"` → Defines the **item** that will appear in each result slot when the recipe is crafted. In this example, the slots are populated with different types of runes like `wooden_rune_m`, `wooden_rune_c`, etc.
- **Page System**: Each recipe has a maximum of 10 pages, and each page can hold up to 12 result slots. For example:
  - `1_1runescribingtablerecipe.json` contains 12 items (from slot 1 to slot 12).
  - `1_2runescribingtablerecipe.json` would contain the next 12 items, and so on.

### Example of Naming Convention for Pages:
- Recipe 1 has 10 pages, so you would have files named:
  - `1_1runescribingtablerecipe.json`
  - `1_2runescribingtablerecipe.json`
  - `1_3runescribingtablerecipe.json`
  - ...
  - `1_10runescribingtablerecipe.json`

### Explanation of the Page System:
Each recipe (e.g., Recipe 1) is divided across multiple files (pages). Each page contains 12 result slots (items). If you have more than 12 result items for a recipe, you would need to create additional pages, keeping in mind that no page can exceed 12 result slots. 

If you reach page `1_10`, you cannot create a `1_11` because each recipe is limited to a maximum of 10 pages.

### Final Notes:
- You can repeat this structure for additional recipes (e.g., Recipe 2, Recipe 3, etc.) by adjusting the recipe number in the file name and item IDs.
- Make sure you don't go beyond 10 pages for each recipe, as the system limits each recipe to 10 pages.
