# Using Combine Sheets / Variants

After creating product versions on the PrintVis job, creating the sheets and product variants (See also Job Versions / Product Parts / Product Variants), you can now create the desired combinations of variants for each sheet.

The screen is split into 2 parts:

## Combine Variants Matrix

The upper part displays details about each variant for the selected sheet. Each line is related to a variant code.

There are fields for the variants mapping:

- Quantity
- Max. no. of ups on the sheet

A matrix with columns for each no. of up and the quantity that results for the current variant, when choosing the specific no. of up(s) for this variant.

## The Plate Changes for the combined Variants

The lower part shows the list of plate changes, starting with the first run of the sheet as “Change no. 0”. Columns display information about how many ups are in use and remaining, as well as the input fields of how many plates and which colors are changed for the current plate change.

## Combining Variants

To combine variants, find a good combination of similar quantities for 1 or more variant(s), select the variant, and create a new plate change, if required.

To select a variant, click into the desired column for the no. of ups. A list pops up that displays the available plate changes (incl. Change 0) to be selected for the current variant. After selecting a plate change and hitting OK, the lower part shows how many ups are in use, how many remain, and the produced quantity. In the upper table, the selected variants quantity is now displayed bold with the color from the plate change it is attached to.

Proceed with other variant units until all available ups on the sheet are used.

## Example case

For the example that is mentioned on the product versions page (see also Job Versions / Product Parts), the 12,000 Brochures in 3 languages example can be set up as follows:

### The Cover Sheet

If there are 4 ups on the sheet, the following Matrix could be made:

- 2 up for the ENGLISH EDITION (6200 required, 6200 produced)
- 1 up for the ITALIAN EDITION (2800 required, 3100 produced)
- 1 up for the GERMAN EDITION (3000 required, 3100 produced)

Total produced quantity is 12,400 with overage of 300 for the ITALIAN EDITION and 100 for the GERMAN EDITION.

No plate changes required.

**Result:** The “Change 0” in the lower section displays in the description: 2 x ENGLISH EDITION, 1 x ITALIAN EDITION, 1 x GERMAN EDITION.

### The 16 pages Text Sheet

If there is 1 up on the sheet, the following Matrix could be made:

Create 2 plate changes. To do so, hit the actions +Add Plate Change in the lower section:

- 1 up for the ENGLISH EDITION, Select Change 0
- 1 up for the GERMAN EDITION, Select Change 1. All plates must be changed: Enter 4 into field Plate-/Colorchange Front. Click on the 3 dots in the field and select all colors. Do the same in field Plate-/Colorchange Back.
- 1 up for the ITALIAN EDITION, Select Change 2. Only the black plates must be changed: Enter 1 into field Plate-/Colorchange Front. Click on the 3 dots in the field and select the black colors. Do the same in field Plate-/Colorchange Back.

**Result:** There are 3 lines displayed in the lower section and the related variant is highlighted with the same color in the upper table.

Proceed in the same way with the remaining sheets.

## Divide in Forms

In case there are more print sheets on a PrintVis sheet / Job item, it is possible to split/divide this sheet into forms.

This could lead to more machine stops for the plate changes and to calculate the correct no. of extra plates.

### Example

There is a total of pages = 32 on a 16-page print sheet = 2 Sheets in Signature.

Hit the action Divide into forms, keep the displayed No. of Forms, and click Ok. PrintVis is creating every sheet in the signature with an extra variant line. This means, if there were 3 variants before, ENGLISH EDITION, ITALIAN EDITION, and GERMAN EDITION, then there will be variants for each edition and sheet (2x 16p sheets): ENGLISH EDITION (1), ENGLISH EDITION (2), ITALIAN EDITION (1), ITALIAN EDITION (2), GERMAN EDITION (1), and GERMAN EDITION (2).

In this example, there are 2 sheets for each language variant, and in this case the second sheet of the same variant could require the change of the 1 plate (black) only, e.g. a colored logo does not change, only the black text is changing. This would mean, for the next language variant, all 4 plates must be changed.

## See Also

- <a href="../pvscasemanagement/" target="_self">Case Management</a>
- <a href="../pvsversionparts/" target="_self">Job Version / Product Parts</a>
- <a href="../pvsvariants/" target="_self">Product Variants</a>