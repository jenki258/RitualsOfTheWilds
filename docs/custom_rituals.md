### File Creation Instructions for Rituals

1. **Create the Recipe File**:
   - Go to `config/Rituals_of_the_wilds/Rituals/eng/`.
   - Create a new JSON file named `29ritual.json` (or increment the number if you already have other recipes in that folder).
        - The number **must be 500 or lower**.  
        - The number **must be the next available number** (e.g., if the highest number is `1ritual.json`, name your file `2ritual.json`).  

2. **Ritual Levels:**
   - There are four levels for each ritual (1 to 4), and each level follows the same general structure but with slight modifications for complexity.
   - The ritual file will include the following key elements:
     - `Ritual Name`: A descriptive title of the ritual (shown in the scroll description).
     - `May Spawn In Ritual Scroll`: Can spawn naturally in ritual scrolls
     - `Must Read Scroll First`: Needs ritual scroll to be readed first to make it executable
     - `Ritual Type`: Defines the ritual as either a "Recipe" or "Command". **(DON'T CHANGE IT!)**
     - `Moon Stage Needed`: Boolean flag indicating if a specific moon phase is required.
     - `Sacrifices needed`: The number of sacrifices required.
     - `Entity Near needed`: Boolean flag indicating if there must be a certain entity nearby.
     - `Ritual Difficulty Level`: The difficulty of the ritual (ranges from 0 to 3).
     - `Info about result`: It will be item that will description with what writen here(Only for command rituals).

3. **File Structure Example (Ritual Type and Difficulty Levels):**
   You have both **Item Rituals** and **Command Rituals**, each having their own file structure.
## Item Rituals

### Example of Item Ritual (Level 0): [template](../config/Rituals_of_the_wilds/Rituals/1ritual.json)

### Example of Item Ritual (Level 1): [template](../config/Rituals_of_the_wilds/Rituals/2ritual.json)

### Example of Item Ritual (Level 2): [template](../config/Rituals_of_the_wilds/Rituals/3ritual.json)

### Example of Item Ritual (Level 3): [template](../config/Rituals_of_the_wilds/Rituals/4ritual.json)

## Command Rituals

### Example of Command Ritual (Level 0): [template](../config/Rituals_of_the_wilds/Rituals/5ritual.json)

### Example of Command Ritual (Level 1): [template](../config/Rituals_of_the_wilds/Rituals/6ritual.json)

### Example of Command Ritual (Level 2): [template](../config/Rituals_of_the_wilds/Rituals/7ritual.json)

### Example of Command Ritual (Level 3): [template](../config/Rituals_of_the_wilds/Rituals/8ritual.json)

4. **Important Fields to Note:**
   - **Central Block ID or Tag**: The block that will be at the center of the ritual.(And this one will be the one you need to click with amethyst powder)
   - **Offhand Item ID or Tag**: Item placed in the offhand during the ritual.
   - **Weather Type Needed**: Defines which weather conditions must be active (e.g., 0 for clear, 2 for storm).
   - **Block Replacement Types**: Defines type of replacment(e.g., 1 is do nothing to them, 2 is make all air, 3 is make it into replacment blocks)
   - **Ritual Difficulty Level**: The level of difficulty that affects the type and complexity of the ritual.**(DON'T CHANGE IT!)**
   - **Result Item or Command**: Defines what the ritual produces (either an item or a command).

5. **Naming and Saving Ritual Files:**
   - Save ritual with the filename `29ritual.json`.
   - Carefully copy and paste the full structure into your `29ritual.json` file, ensuring no keys or values are missed or altered.

### Editing existing rituals
   In `config/Rituals_of_the_wilds.toml`, set the following:
   ```toml
   Regenerate Rituals = false
   ```
Then you can edit rituals and don't be afraid that they will regenerate after rejoining world

### Troubleshooting:
- **Missing or Incorrect Keys**: If you delete a required field or change a key, the game may crash. Always cross-check with the template.
- **Consistency**: Make sure that block IDs and item IDs are correctly referenced and match their in-game counterparts.

If you follow the structure as shown and ensure all necessary fields are included, the ritual should work without errors.
