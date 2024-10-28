# Using Tools

PrintVis Tools can be used for any kind of tool that is required for the production.

For PrintVis Tools there are different settings that can be made to define dependencies between different tools and cost centers the tools can be used on. A tool could contain a layout for the print operation, which defines the minimum area for the print section, the number of ups/items in the width and length of the print section, distances between different ups and margins.

Tools are typically used for the following productions:

- Narrow web label
- Cut-and-Stack label
- Flexible packaging
- Folding carton
- Die cutting
- Embossing
- etc.

A tool could be a:

- Die cylinder
- Die plate
- Flatbed die
- Tool for embossing
- Print cylinder
- Any kind of tool relevant for production

## Setting up a Tool

### General Tab

To create a new tool hit **New** on the Calculation Units list or the **+** sign. The **Code** could be set by a number series or manually, depending on the current setup. Enter a **Description** and if require a **Description 2** to identify the new tool.

### Format Tab

Please note: Several fields in this section could have a custom caption. Please contact you BC/PrintVis Administrator, of you are in doubt which field to use.

Enter **Format 1** and **Format 2** as final product size and the no. of items in the **Width** and L**ength** of the print section.

By selecting the **Group** several settings are predefined, and some fields will now be automatically calculated based on the product size, number of ups and margins. Those fields might appear as not editable and just show the calculated values.

The **Teeth Code** is set by the selection of the Group and defines with teeth and gears are available for that **Group**. The **Distance across** / **around** fields are defining the gap between each product in the width and length of the tool. The **Step around** / **across** display the format/size + distance values **around** / **across**. The value step around could be a given value calculated from the number of **Teeth**. If a Teeth Code is existing PrintVis will find the next possible Teeth value from the **Step** and **Repeat Around**. It is possible to select the higher number of **Teeth** which will result in a bigger **Cut-Off** / **Optimal Hight**.

The terms **around** / **across** are meant for cylinders: **Around** = in the circumference and **Across** = in the width of the cylinder. They are equivalent to a width and length in case of a flatbed tool.

The fields **Corner Radius**, **Inner Height/Width/Length** can be used to enter the related values to filter / find the required tool in an estimate as well as the parameters for **Shape**, **Hardness** and **Status**.

Select **Shelf/Bin No.** if available to define where the tool is typically stored.

The field **Max. Number of Colors** is only in use, if there are multiple tools of the same **Code** available. The usage is typically for print cylinders and the user is only able to select a print cylinder **Code** if the number is equal or is higher than the number of colors from the current sheet / job item.

### Information Tab

The **Information** tab displays fields about creation and modification dates/users. If PrintVis Integrated field are setup, they will be displayed here as well.

# Imposition Type connected to a Tool

After the tool is setup correctly and if the layout must be used for estimates, please hit the action **Create Imposition** to create an imposition for this tool. An **Imposition Type** with all sizes, ups and margins is being created with the same code as the tool. This Imposition Code is displayed in the lookup field **Imposition Type** and the major fields are now maintained by the fields on the **Format** tab from the current tool.

**Imposition types** can be selected manually for each Sheet/Job Item but they can be also added because of the selection for a tool. If a Sheet/Job Item contains an imposition type, the values for no. of ups in the print section, print section size are set to a fix value and cannot be changed unless the imposition type is removed again from the sheet.

- Fix Layout for Print Section
  - Definition for no. of ups on print section
  - Definition of margins
  - Overrule the imposition calculation of PrintVis
- Can be connected to a Tool / Die
  - Which has a fix layout
- Required for Folding Carton industry if layout is nested because an external CAD solution is required to define the nested layout.
- Can show product picture instead of imposition drawing
- Connected to JDF Folding Catalog for Commercial Printer
  - Mandatory for JDF Based Workflows

## Further Page Actions

The action **Tool Usage** can be used, in case a Product Group required a 1:1 relationship between tools. This is rarely used and should be only set if you are sure this setup is required for your system setup. Otherwise, it might impact the selection for tool unexpectedly.

## See Also

- <a href="../pvsproductgroups/" target="_self">Product Groups</a>
- Tool Codes
- Machine Tool Usage
- Tool Combination Usage
- <a href="../pvscostcenter/" target="_self">Cost Center</a>
- Configuration
- Integrated Fields