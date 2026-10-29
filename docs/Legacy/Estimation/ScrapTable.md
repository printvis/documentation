# Scrap Table Setup


## Summary

Scrap calculation in PrintVis is managed through tables attached to a cost center's configuration. Scrap tables are vital for accurately calculating scrap in processes such as printing, finishing, and other operations.

## Setup

![Scrap Table Setup 1.jpg](./assets/Scrap Table Setup 1.jpg)

 Accessing Scrap Tables

- Search for "Scrap Tables" and select "PrintVis Scrap Tables" to set up or modify scrap tables.


 Parameters

- **Scrap Group**: Defines the parameters for scrap calculation.

 Header Fields

| **Field Caption**     | **Description**                                                                                                                                                                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Code**              | Enter a code for this scrap table. This can be selected in a cost center configuration.                                                                                                                                                            |
| **Description**       | Enter a description for this scrap table.                                                                                                                                                                                                           |
| **Format Type**       | Select the format type for the format entered in the scrap table lines. **Available options include:**<br>- **Blank**: No format required.<br>- **Job Item Format**: Reads format from the job line (e.g., A formats), commonly for finishing processes.<br>- **Printed Sheet Format**: Reads the printed sheet format, used for printing machines. The format is read for each process line in the job.<br>- **Paper Sheet Format**: Reads the raw sheet format, typically for printing machines.<br>- **Plates**: Reads from the individual printing process line (rarely used).<br>- **Film**: Reads from the printing process line if films are attached to the sheet. |
| **Weight Unit**       | Used for **Imperial paper weights** only. Select the weight unit for the weight entered into the table lines. Leave blank for **M-Weight**.                                                                                                         |
| **Formula 1/2**       | Add up to two formulas if additional values or parameters are required. This is configured via the **Formula Principle** field.                                                                                                                     |
| **Formula Principle** | Determines how formulas are applied. **Options include:**<br>- **Parameter**: Adds the formula's value as scrap quantity, allowing you to define custom scrap values. If parameter is selected, then formula No. must be added to the PV Cost Center Configuration Calculation section in fields “Formula Misc. 1 to 3. And only one line in Scrap Table. See examples below.<br>- **Read from**: Uses the formula value to determine which line to use, such as "Quantity From" or "Scrap Group." |


 Fields in Scrap Table

| **Field**                    | **Description**                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Product Group**            | Read from the job line. Use this if product groups impact scrap calculation, e.g., for rotary machines or finishing processes. Create a blank section for cases where no specific product group applies.                                                                 |
| **Scrap Group**              | Contains predefined groups like "easy," "medium" (blank), and "difficult." Use these groups to grade the scrap table.                                                                                                                                                   |
| **Format Code**              | Uses sliding format lookup, reading the nearest value. Create a blank section to handle unexpected formats.                                                                                                                                                              |
| **Weight**                   | Works as intervals. For sheet-dependent processes (e.g., printed sheets), the system reads the paper weight. For processes across sheets (e.g., stapling), it reads the job line weight.                                                                                 |
| **From Signature Quantity**  | Reads the number of sections in a printing process from the job item table as intervals.                                                                                                                                                                                |
| **No. of Runs**              | Functions as an interval. Reads the number of runs for the individual printing process from the value on the line up to the next.                                                                                                                                       |
| **Formula 1 / 2**            | Defines scrap calculation for selected formulas. Example: Formula 2 (number of colors) with a value of 25 calculates 100 scrap units for a 4+4 job (4 x 25). Use "read from" mode to return the formula's calculated quantity instead.                                      |
| **From Quantity**            | Indicates the net printing sheet quantity. Scrap is calculated for one sheet set by default. To calculate for all sheet sets, use a formula.                                                                                                                           |
| **Per Sheet/Section Scrap**  | Quantity of scrap sheets assessed per printed sheet (e.g., start scrap).                                                                                                                                                                                                |
| **Sheet/Section Following Scrap** | Adds scrap for subsequent sheets, influencing only the first sheet of the process.                                                                                                                                                                                       |
| **Scrap % Running**          | Fixed percentage of scrap used for control purposes or machine operations. Added to other defined scrap.                                                                                                                                                               |
| **Per Plate Scrap**          | Layout scrap based on the number of plates used in the printing process.                                                                                                                                                                                               |
| **Plate Following Scrap**    | Scrap for additional plates, influencing only the first plate. Adds values for subsequent plates.                                                                                                                                                                       |
| **Per Processing Scrap**     | Scrap generated when the machine starts a run. Number of runs depends on colors and rolls/towers. For example, 4 colors on a 2-color machine require 4 runs, increasing scrap.                                                                                         |
| **Per Shift Scrap**          | Scrap caused by machine stops for plate shifts, such as changing languages. Calculated if specified in the sheet settings.                                                                                                                                              |
| **Per Plate in Shift Scrap** | Scrap for additional plates during shifts.                                                                                                                                                                                                                             |

## How PrintVis Calculates Scrap

- **From Quantity**: Actual quantity indication in the scrap table.
- **Per Sheet/Section Scrap**: Scrap quantity per printed sheet.
- **Sheet/Section Following Scrap**: Scrap for additional sheets.
- **Scrap % Running**: Fixed percentage of scrap during running.
- **Per Plate Scrap**: Scrap based on the number of plates used.
- **Plate Following Scrap**: Scrap for additional plates.
- **Per Processing Scrap**: Scrap expected at the start of a run.
- **Per Shift Scrap**: Scrap for machine stops during a shift.
- **Per Plate in Shift Scrap**: Scrap for additional shift plates.

![Scrap Table Setup 2.jpg](./assets/Scrap Table Setup 2.jpg)

![Scrap Table Setup 3.jpg](./assets/Scrap Table Setup 3.jpg)



- For finishing operations, use "Per Processing" rather than "Per Sheet" to calculate scrap for the entire job.
- Scrap is calculated for each process and totaled backward from the last to the first process.

### Calculation of the "Quantity From" Field

- **Formula Principle = "Read From"**
- **Formula 1 = 62**: Determines fixed scrap based on the number of colors.
- **Formula 2 = 221**: Determines total net rotations for the sheet.

If a job has:
- 1 sheet set of 100,000 rotations for a 4-color job: Line 1 applies (4000 fix + 20% running scrap).
- 2 sheet sets of 100,000 rotations: Line 2 applies (4000 fix + 18% running scrap).

For different quantities, the "From Quantity" remains as per the formula used.

![Scrap Table Setup 4](./assets/Scrap-Table-Setup-4-9a4a9305-3b0a-4437-9391-e823c3127075.png)

•   **Formula Principle = "Parameter”**
If using Parameter, then formula setup must be inserted in PrintVis Cost Center Configuration Calculation section in fields Formula Misc. 1 to 3.

![Scrap Table Setup 5](./assets/Scrap-Table-Setup-5-a5a57b99-f476-4a0e-81e9-2ea4a6b0a528.png)

Based on the formula entered here, the value entered on the scrap table in Formula 1 field will be multiplied by the value on the Formula Misc 1 gathers. This is only the case when the option "Parameter" is selected on the scrap table.

For your example, you would put formula 90 in Formula Misc 1 on the configuration. Based on the number of versions calculated for the job, it would be multiplied by the value entered in Formula 1 on the scrap table.

This will only work if a single scrap table line is entered on the scrap table. If more than 1 scrap table line is filled out, then the last scrap table line will be used. It can also be combined with Scrap Group to be used and selected on the estimation page.

![Scrap Table Setup 6](./assets/Scrap-Table-Setup-6-42baa2bb-8f7a-422b-80c9-7b2522fa3668.png)




