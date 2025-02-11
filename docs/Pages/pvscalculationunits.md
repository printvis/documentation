# Using Calculation Units

PrintVis Calculation Units are required for everything that should be a costing part in the estimation and contains settings for how the unit should appear in the estimation. The structural steps to estimate with a machine, workplace, subcontractors, or other costing parameters is to:

1. Create a Cost Center,
2. Create a Configuration linked to that Cost Center, and
3. Create a (or more) Calculation Unit(s) linked to the Configuration.

In most cases, there should be 1 Calculation Unit created for 1 Cost Center Configuration.

If the Calculation Unit is for a printing machine, most often there are 2-3 Calculation Units created. A printing machine requires a setup of a Calculation Unit and List of Calculation Units (setting / Boolean on the Calc Unit). The List of Units is required to select the machine on the Job Items and the list might contain an additional unit for the plate calculation.

## Creating Calculation Units

In most cases, the Calculation Unit is created by an import of a reference Cost Center, by using the action Create Calculation Unit on the Cost Center Configuration or by using the action Copy Calculation Unit to copy the current one.

### Creating Calculation Units Manually

Calculation Units can also be created manually. Hit New on the Calculation Units list or the + sign on the Calculation Units page and enter a Code and Text description. Please take special attention to the following fields:

- Select the Cost Center to which this Calculation Unit should be assigned.
- Select the Configuration to which this Calculation Unit should be assigned.
- The field Process Type will be set automatically based on the Cost Center Configuration Type. Make sure to do some proper testing if you do manual changes here which is not recommended!
- Do not enable the field Process Start on units that must be selected with a List of Units for a printing machine and doesn’t represent the operations for the printing machine like the calculation units for print substrate only and the Calculation Unit for the plates. A Process Start will create a new process number for all units with enabled Process Start field, but it is mandatory that the Calculation Unit for the plates gets the same process number as the Calculation Unit for the printing machine.
- Enable the field Hide if the Calculation Unit should not be visible in the Calculation Unit Lookup on the Estimation Page. This can be the case if you want this to be selected only in combination with a List of Units.
- Enable the field Cancel if the Calculation Unit should not be used anymore. This could be the case if a machine was sold and is no longer existing. It is not possible to delete a Calculation Unit that is used in estimates! A message will appear if you copy Cases / Jobs that contain a cancelled Calculation Unit.
- A Sorting Order on tab Show must be set for each Calculation Unit. The Sorting Order defines the default sequence for this Calculation Unit when it is used in Estimating. Example: A folding machine should have a higher sorting order number than a printing machine, because the folding comes in sequence after the printing process during production. The sorting order can be modified in each calculation if required, e.g. the guillotine cutter must be used before the folding or before the printing process. Best practice is to review the sorting order on the Calculation Units list. If the Edit List action is enabled, change the Sorting Order to get the desired default sequence of Calculation Units.
- Enable the field List of Units if the Calculation Unit should be selected as a list on the Job Items. This is only possible if no Detail lines exist. If List of Units is enabled, the Detail tab will disappear and the Units tab will be displayed. It is now possible to select the Calculation Units that must be added to the Estimation by selecting the List of Units.

## Details Tab

The Calculation Unit contains the operations linked to a configuration. Lines for material consumption can be added to the Details, such as the paper / print substrate and ink consumption. If the paper / print substrate cost / price should be displayed separately in the upper Estimating page, the lines of type Item for the material consumption or subcontracting cost must be added here manually. Formula codes for the paper / print substrates can be 14, 15, 240, 250, or 260, depending on the inventory / consumption unit of the items. For ink lines, please use the formula code 160, which is the calculation of the weight of ink based on the priced area.

## Further Page Actions

If User Fields are enabled for Calculation Units, the actions to Userfield 1/2/3 Calculation Units need to be set up with the related User Fields. By using the action Merge, the operations of the current Calculation Unit will be merged with the selected New Calculation Unit and the current Calculation Unit will be deleted.

## See Also

- <a href="../pvscostcenter/" target="_self">Cost Center</a>
- <a href="../pvscostcenterconfig/" target="_self">Cost Center Configuration</a>
- <a href="../pvspricelists/" target="_self">Price Lists</a>
- Calculation Formulas
- Scrap Table
- Speed Table