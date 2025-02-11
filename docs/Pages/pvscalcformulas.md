# Using Calculation Formulas

The PrintVis calculation formulas are made to calculate quantities/numbers from various values which can be used in different places. It is a strong tool and if a definition is possible, it can also be calculated. It is very helpful to spend a couple of hours learning where formulas can be used, which formulas exist, and how to set up a custom formula.

The formulas are numbered instead of an alphanumeric code. Numbers 1 to 999 are system formulas, whereas formulas with a number from 1000 are customizable or formulas created by/for a customer.

When creating a setup by using the PrintVis assisted setup, a set of useful formulas will be imported. These are formulas that will be used often but are not generic enough to be a system formula.

**Please note:** If formulas are missing (System formulas between 1-999) in a new company setup or if new calculation formulas are added in a PrintVis feature release, please click the actions Rebuild All System Formulas. This will recreate/add all system formulas. Formulas >=1000 are not changed by this function.

## Where to Use Formulas?

The typical places are the operations and material lines in the setup of calculation units and cost center configurations.

### FastTab "Calculation" on Cost Center Configurations

These are mandatory to calculate setup production quantities for each Calculation Unit.

To understand the logic, look at an existing setup to see which formulas are used when.

- Operation lines in Cost Center Configurations and Calculation Units
- Item lines in Calculation Units

As parameters in:

- Speed tables
- Scrap tables
- Price Lists

## Creating Formulas

PrintVis calculates the formulas in the sequence of the numbering. If formulas are dependent on values that are calculated in the estimating page by other formulas, make sure the formula number for a formula that must lookup other formula values has a higher formula number than the formula a value is read from.

Formula numbers must be entered manually, and the number must be >=1000. It is recommended to group formulas. For example, formulas from 10000-19999 could be used for prepress values, 30000-39999 for formulas used in the print department, and 60000-69999 for finishing formulas. Keep spaces in the numbering in case more formulas might be required for the same area.

Hit New to create a new formula and enter a number that is available. Enter a Name that helps to identify the value for the formula. Make sure to use a Unit that fits the unit of a related speed table or price list.

## User Formula Types

Depending on how the formula is being built, there are different formula types available. If a user-created formula gets too complex or is not supported by the formula editor, formulas can also be created by custom code that is stored in the object types of Report or Codeunit.

With this selection, the formula type can be set, which will change the tabs/fields displayed for the formula setup.

### Combination

The type of Combination provides operations like +, -, x, / together with existing formulas and/or constant values to be calculated/combined. This type can also be used to set constant values to be used as fixed parameters in other formulas.

For example, to calculate the area of a paper sheet, you need to use the formulas that hold the length and width of the sheet (these are formulas 59 and 60 for the raw material sheet size and formulas 57 and 58 for the print sheet size, if it is cut down).

- Insert Formulas No. 59 and hit Enter
- Then click the multiply sign X
- Insert Formulas No. 60 and hit Enter
- Then click the division sign /
- Insert Constant 1000000 or 144 (1000000 for mm² into m², or 144 for in² into ft²)

While entering the data you’ll see the Formula and Internal Formula field values growing. After the formula is completed, the fields are displaying the following:

- **Formula:** Length Full Sheet Format x Width Full Sheet Format / 144
- **Internal Formula:** 59;*;60;/;K144;

The field Internal Formula helps to see which formulas have been combined in the current formula and a constant value is indexed with the letter K.

The result is the value for the current printing sheet area in ft² (or m²). If the formula must be extended to calculate the total print area for a sheet, just add a multiplication with formula 150 (Number of printed sheets incl. scrap) etc.

Use Insert Formula No. to link to an existing formula instead of Copy Formula No. If a formula is being corrected when it was wrong, all formulas linking to this formula are now using the corrected value. All formulas where Copy Formula No. was used must be corrected manually. Copy Formula No. only affects formulas >=1000.

Make sure to check the Formula description which contains tips where the data is read from. For example, the current job, or sheet, or the first sheet, etc.

### LookUp

LookUp formulas can be used to read values from different areas of a case selected by the Source field. This is used to read values from various places in job-related values. If you select the Look-up formula type, the bottom part of the window changes so the fields which must be filled in become visible. Common for all LookUps is that the result is based on a Formula Class Filter defined in the calculation unit setup.

### UserFields

With this type, values can be "read" from user fields. Make sure these user fields are of type "Number," otherwise the result of this formula type will be 0 (zero).

### Conditional

Conditional formulas are formulas where the result depends on the result of another formula. It is kind of an “If…Then…Else” option and it is possible to build complex conditions.

**Example:**

For a printing process where you only want to calculate drying time for turning or tumbling, if the net quantity is less than 5000 printed sheets, you may select formula 11 (quantity net printed sheets) as the condition. The further build-up is as outlined below.

- **Conditional Formula:** Select formula code 11 (quantity net printed sheets).
- **From Quantity 1:** Enter the value 0.00 and don’t choose a formula in field Formula 1.
  - **Result:** If the result for the Conditional Formula is =0, the result of the current formula =0.
- **From Quantity 2:** Enter the value 1.00 and choose a formula code 27 (Work-and-Turn or Work-and-Tumble) in field Formula 1.
  - **Result:** If formula 27 “net printed sheets” (Conditional Formula) is between 2 and 4999, the result of the current formula =1.
- **From Quantity 3:** Enter the value 5000.00 (below this quantity, extra drying should be calculated) and don’t choose a formula in field Formula 3.
  - **Result:** If the result for the Conditional Formula is >=5000, the result of the current formula =0.

Use the example formula in an operation with a speed setup that gives the drying time. For example, speed = 2/h calculated with quantity =1 (From Quantity 2 condition) gives 1/2h of drying time.

Naturally, the build-up of conditions and results varies depending on which result is desired. The above is only one of many examples.

### Report

If the desired result is difficult to calculate or requires many formula steps (many formulas combined to a result may impact system performance), it is better to use a Report with some coding that gives the result. Typically, a formula of type Codeunit is used instead of type Report.

### Any Field

This type gives access to all fields of the Any Field Table options. After choosing the table, please choose the field in Any Field Field No.

**Please note:** This type of formula requires experience with the PrintVis data structure. If, for example, a field from the item table is chosen but the calculation details have no relation to an item, the formula values will be = 0.

### Codeunit

If the desired result is difficult to calculate or requires many formula steps (system performance) it is easier to use a Codeunit with some coding that gives the result.

## Other Parameters

### Precision

If a formula result should be rounded, the Precision field can be used. Enter the precision for the calculated value.

**Example:**

The calculated value is: 12.12345

The options -> results are:

- 1.00 -> 12.00
- 0.10 -> 12.10
- 0.01 -> 12.12
- 0.00 -> 12.12345

### Rounding Type

Choose if the value should be rounded Up or Down. When choosing Nearest, the value is rounded to the nearest value by keeping the precision.

### Min. Value / Max. Value

To limit the result of the formula value, it is possible to set max. or min. values. Value =0 or an empty field is ignored.

### Simple Custom Formula

This field has only effect on User Formula Types = Report or Codeunit. If this field is disabled (default), all job data (Tables: Calculation Unit/Calculation Detail/Process/Sheet) will be buffered in the cache and the code in the report or codeunit is able to use this data. If the code is not using the job tables, this field can be enabled which will increase the performance.

### Insert Item No.

If the current formula is being used in calculation detail lines and it is required that the line contains an item no. for the print substrate (to calculate the paper consumption), it is possible to form the available option where to get the substrate item no. from.

## Formulas Used in Speed Tables

Calculation formulas can be used in speed tables. For example, if you want to calculate the time for the setup of pockets on a saddle stitcher, you can use formula 109, which gives the number of sheets in the current job. Typically, each sheet requires a pocket on a saddle stitcher.

## Formulas Used in Price Lists

Calculation formulas can be used in price lists. For example, if you want to calculate click cost/prices based on the number of colors front/back. Different prices are typical for 1/0, 1/1, 4/0, and 4/4 colors. You can use formulas 62 for colors front and 63 for colors back as parameters in the price list.

## Formulas Used in Scrap Tables

Calculation formulas can be used in scrap tables, like the examples for speed tables and price lists.

## See Also

- <a href="../pvscostcenterconfig/" target="_self">Cost Center Configuration</a>
- <a href="../pvscalculationunits/" target="_self">Calculation Units</a>
- Speed Table
- Scrap Table
- <a href="../pvspricelists/" target="_self">Price Lists</a>