# Using the Tools Selection

PrintVis works as a guide for displaying possible combinations of:

- Machines (printing machines),
- Print cylinders, and
- Dies

…which meet specific product parameters.

This functionality is often made for PrintVis customers in the narrow web label production industry.

For example, the **PrintVis Tools Selection** supports the sales department for inquiries by locating existing print cylinders and dies for a quote requested from a customer or prospect. With this information, it is possible to define a delivery time frame which might be longer and provoke extra cost if no die tool is available.

If no die is available for certain specific product parameters, the page will display which print cylinders are available, and on which printing machine the product with the given parameters fits. The calculation of potentially usable cylinders is made by using default gaps/distances between the labels in the print section/step-and-repeat layout, that are common/required for the product. **Gaps/distances and other defaults** can be set up in the Job Item Format Setup and selected for each component type. Min. and max. distance can also be entered manually on each selection.

The user can select one of the displayed combinations that will be used on the actual job item. The data will be filled into the calculation, the Job Item Fields List of Units (selected machine), Tool (selected die), and Tool 2 (selected print cylinder) will be filled with the selected combination.

## Filters and Apply Filters

The filters are used to find the possible combinations of:

- Printing machine,
- Print cylinders, and
- Dies.

The fields **Min. Label Distance Front** and **Max. Label Distance Front** are used to define the given gaps around (circumference) the cylinders, and it is mandatory that the **Max. Label Distance Front** is a higher value than the **Min. Label Distance Front**. An empty field is handled as `value = 0`.

When hitting **Apply Filters**, all possible combinations will be found within the given Min. / Max distance and number of colors for the print cylinders.

All other fields can be used to reduce the list of combinations. The field, **Max. No. of Labels in Width**, can be used for smaller print runs. That way, combinations for wider machines are not displayed to get the best possible relation between setup and printing time.

**Distance Across**, **Corner Radius**, and **Shape** affect the available dies.

## Selecting the Desired Combination from the List

The list shows from left the possible printing machine, the available print cylinders tools, and available dies to the right, if there are possible combinations with existing die tools.

## See Also

- <a href="../pvscostcenter/" target="_self">Cost Center</a>
- <a href="../pvscostcenterconfig/" target="_self">Cost Center Configuration</a>
- Price List
- Calculation Formulas
- Scrap Table
- Speed Table