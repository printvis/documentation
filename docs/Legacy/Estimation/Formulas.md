# Calculation Formula setup


PrintVis Calculation Formulas are powerful tools for calculating quantities and numbers from various values, which can be used across different areas in PrintVis. Learning how to use and set up these formulas can significantly enhance your ability to manage calculations within the system.

## Formula Types

- **System Formulas (1-999)**: These are predefined formulas that cannot be edited.
- **Custom Formulas (1000 and above)**: These formulas can be customized or created from scratch. To create a new formula, use a number >= 1000.

To restore missing system formulas (1-999), use the **Rebuild All System Formulas** button in the menu.

## Where to Use Formulas

Formulas can be used in several places, including:

- **Operations and Material Lines** in the setup of Calculation Units and Cost Center Configurations.
- **FastTab "Calculation"** on Cost Center Configurations.
- **Speed Tables**
- **Scrap Tables**
- **Price Lists**

## Formula Numbers / Codes

![Calculation Formula setup 1.jpg](./assets/Calculation Formula setup 1.jpg)

- **Formula 1**: System formula providing the quantity from the job.

![Calculation Formula setup 2.jpg](./assets/Calculation Formula setup 2.jpg)

- **Formula 1012**: Custom formula used to calculate product weight by adding 5% to the paper weight.



## Setup Fields

| **Field**                    | **Description**                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Code                         | Code is a system primary key for the Formula Setup.<br>1-999 = System Formulas (cannot be edited)<br>1000..= Custom formulas                                                                                                                                                                                                                                                             |
| Name                         | Enter a Name/Description for the formula.<br>Ensure the name clearly describes the formula's function for easy identification.                                                                                                                                                                                                                                                          |
| Precision                    | Enter the precision for the calculated value.<br>Example:<br>The calculated value is: 12.12345<br>Options -> Results:<br>1.00 -> 12.00<br>0.10 -> 12.10<br>0.01 -> 12.12<br>0.00 -> 12.12345                                                                                                                                                                                                |
| Formula Internal             | Stores the formula in a system-readable form.<br>Example (Combination type):<br>Internal Formula: `K1;+;(;22300;/;K0,5;);*;K5;`<br>Formula in words: Constant Value 1 + (Value of Formula 22300 / Constant Value 0.5) x Constant Value 5<br>Example (non-Combination):<br>Internal Formula: `22300;`<br>Formula in words: This value is just the formula number. |
| Formula                      | Displays the formula in a readable form. If an existing formula is used in this formula, its name is displayed instead of the formula number.                                                                                                                                                                                                                                          |
| Constant                     | Enter a constant value to be added to the formula. The value will be added to the existing formula once the cursor leaves the field.                                                                                                                                                                                                                                                    |
| Rounding Type                | Options for rounding the calculated value:<br>**Up**: Rounds up to the given precision<br>**Nearest**: Rounds to the nearest value for the precision<br>Example:<br>Precision = 0.1<br>1.44 -> 1.4<br>1.45 -> 1.5<br>**Down**: Rounds down to the given precision                                                                                                                              |
| Min. Value                   | Enter the minimum value if the calculated value must be limited.                                                                                                                                                                                                                                                                                                                        |
| Max. Value                   | Enter the maximum value if the calculated value must be limited.                                                                                                                                                                                                                                                                                                                        |
| Simple Custom Formula        | Applicable to "User Formula Types" (e.g., "Report" or "CodeUnit"). If set to "No," job data is buffered for use by the report/codeunit. If not needed, set to "Yes" for better performance.                                                                                                                                                                                              |
| Insert Substrate No.         | Determines how substrate details are handled:<br>**Substrate from Sheet**: Pulls paper item no. from the sheet and applies it to the Calculation Details.<br>**Item from Job**: Pulls item no. from the job for use in the Calculation Details.                                                                                                                                           |
| Unit                         | Enter the unit for the formula's result (e.g., pcs, lbs, sqm). This unit must match the unit on the price list or item for proper cost/price calculation.                                                                                                                                                                                                                                |
| Add. Quantity Calculation    | Defines additional quantity calculation behavior:<br>**Normal**: Based on the first formula in the structure.<br>**None**: No additional quantity calculation.<br>**Proportional**: Proportional to the total formula calculation.<br>**Vary single link**: Specifies a term in the formula to vary.<br>**Special formula**: Uses a specific formula for calculation.<br>**As mainline**: Same as the main line. |
| Add. Quantity Factor/Formula | Specifies the term or formula for additional quantity calculation when "Vary single link" or "Special formula" is selected.                                                                                                                                                                                                                                                              |
| External Object              | Visible when "User Formula Type" is "Report" or "CodeUnit." Allows selection of the object number for the specified type.                                                                                                                                                                                                                                                                |
| User Formula Type            | Defines the formula type, determining available tabs/fields:<br>**Combination**: Operations like +, -, ×, ÷ with constants/formulas.<br>**LookUp**: Reads values from other tables.<br>**Conditional**: Depends on another formula's result.<br>**Report**: Custom coding via reports.<br>**Codeunit**: Custom coding via codeunits.<br>**Any Field**: Accesses all fields of selected tables. |

## Example for a calculation Formula of type Look Up

![Calculation Formula setup 3.jpg](./assets/Calculation Formula setup 3.jpg)

In this example the user has to key in how many labels will fit into a box. The formula will filter on the formula class filter "#PERBOX" find the line and come back with the total of the quantity field. This value can be used to calculate the # of boxed needed.

![Calculation Formula setup 4.jpg](./assets/Calculation Formula setup 4.jpg)

## Formulas Used in Speed tables

![Calculation Formula setup 5.jpg](./assets/Calculation Formula setup 5.jpg)

For a saddle stitcher, the speed depends on the number of feeders/pockets:
- **0-3 feeders/pockets**: Speed = 7000 sheets/hour
- **4-5 feeders/pockets**: Speed = 6500 sheets/hour
- **6-7 feeders/pockets**: Speed = 6000 sheets/hour
- **>7 feeders/pockets**: Speed = 0 sheets/hour, with a warning message

![Calculation Formula setup 6.jpg](./assets/Calculation Formula setup 6.jpg)

## Formulas Used in Price lists

In a price list for click costs, the price depends on:
- **Number of colors** on the front and back pages.
- **Printing mode**: simplex or duplex.

Formulas used:
- **Formula 62**: Number of colors on the front page.
- **Formula 63**: Number of colors on the back page.

**Price List Examples**:
- B/W job printed simplex
- B/W job printed duplex
- Color job (more than 1 color) printed simplex
- Color job (more than 1 color) printed duplex

![Calculation Formula setup 7.jpg](./assets/Calculation Formula setup 7.jpg)

