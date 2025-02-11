# Using Cost Center Configurations

PrintVis Configurations describe the technical specification, operations, speed, and costing structure for the Cost Center. There's typically at least one configuration for each Cost Center, but there can be more. Each configuration can be set up with different costing and profit rates, a scrap table, different setup and production operations, and their speed tables and price lists.

The **Configuration Type** can be *Basic* or *Surcharge* and describes if it is the main machine (*Base*) that can run independently or if it is a *Surcharge* that can be switched on or off and used only if needed. A surcharge unit might impact the speed reduction for the Base Configuration if selected.

An example of a Cost Center with more than one Base Configuration would be:
- A 6-color press that runs with different costing/profit rates if running a 6-color job rather than a 1/1 color job.
- A folding machine that operates with different costing/profit rates for cross-fold jobs versus double-gate-fold jobs.

Examples of Surcharge Configurations:
- Varnishing unit on a press.
- Gluing unit on a folder.
- 3-knife trimmer on a saddle stitcher.

They can be selected if required but cannot run independently without a Base Configuration.

## Creating Configurations

### Importing Configurations

Several settings are required to create a Cost Center, Configuration(s), and Calculation Unit. PrintVis offers a reference database with well-known work centers/machines from the printing industry for import to streamline this process. If a desired machine does not exist, similar machines can be imported and adjusted. You can find the import function on the Cost Center list by using the **"Create from Reference Company"** action or **"Cost Centers"** in the PrintVis Assisted Setup.

### Creating Configurations Manually

Creating a new Configuration can be done from the list by entering the Configuration code, Name, and Configuration Type.

For the **Mixed Configuration Cost Center** type, it is necessary to select the Machine Type and Type. These selections can also be made on the Configuration card, but the page might need to be reopened to display the necessary setup fields.

- **Configuration Code**: Unique only in combination with the Cost Center code. Codes like B1, B2 (for Basic configurations) or S1, S2 (for Surcharge configurations) are useful but not mandatory.
- **Scrap Table**: Use the action **Scrap Table** to create or display a table. If none exists, one will be created with the Configuration code.

The **Speed Table** on the General tab is required only if impacted by a surcharge unit selection in the estimate. Otherwise, Speed Tables are set up for operations on the Operation tab.

### Setting Hourly Rates

Click on the **Rates** action to set up or edit the hourly rates for this Cost Center Configuration.

## Machine Tab

If the current Configuration is the Machine Type "Printing Machine," set the required parameters on the Machine tab. Empty or zero parameters (e.g., Max. Paper Weight = 0) are ignored.

For other Machine Types, the tab does not provide settings. Use Speed Table warnings to set machinery limitations.

## Calculation Tab

For a Basic Configuration, set formulas on the Calculation Tab (e.g., Formula No. Print = 22 for press configurations, 420 for finishing). If unsure, refer to similar Cost Center Configurations.

You can set up to 6 **Auto Colors** for default inks in estimates. For example:
- If a job has Colors Front = 1, only Auto Color 1 will be added.
- It's recommended to set Auto Color 1 as black for process inks.

## Operations Tab

On the Operations tab, setup and production operations must be configured.

- Enter an **Operation Code** and description.
- Select a **Unit of Measure** for cost mapping on the PrintVis Job Costing Report.
- Use either a fixed Quantity or a Formula Code for calculation.
- Enable fields like **Incl. in Re-run** and **Incl. in Add. Q. Price** if needed.
- Use **Price List Code** for specific costs (e.g., digital press click-cost).
- Enable **Sub Contracting** if the cost is for external subcontractors.

Use the **Speed Table** action to create or edit speed tables. Ensure units match the Calculation Formula's units.

Set different rates for the operation only if required, but generally, use the hourly rates set at the Cost Center Configuration level.

## Further Page Actions

- Create Calculation Units.
- Set up Machine Tool Usage.
- View related calculation units via the **Calculation Units** action.

## See Also

- <a href="../pvscostcenter/" target="_self">Cost Center</a>
- <a href="../pvscalculationunits/" target="_self">Calculation Units</a>
- <a href="../pvspricelists/" target="_self">Price Lists</a>
- <a href="../pvscalcformulas/" target="_self">Calculation Formulas</a>
- Scrap Table
- Speed Table