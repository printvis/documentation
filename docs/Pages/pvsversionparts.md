# Using Job Versions / Product Parts

In the **Job Product Part** section, it is possible to enter different product versions that can be produced with one or more job items.

In the **job items** section, it is possible to:

- Split these products into versions or variants,
- Combine the variants on sheets,
- Create plate changes for each sheet, or both.

PrintVis calls this functionality **Versioning**.

### Examples:

- **Newspapers** with different local versions. Some parts could be the same for all versions though.
- **Combinations of Cover and Matter/Text** in different languages/versions.
- **Different labels or folding carton boxes** using the same die shape and combined because only the design/colors differ.

After combining the different Job Parts, PrintVis automatically calculates the required plates and machine stops for each sheet. Based on the combination and plate changes entered, the print processes with plates, setup, and scrap are estimated.

## Example

A typical example of versioning is a brochure or newspaper with different parts in the Text part, different language versions, or parts that might not be for all versions.

**12,000 Brochures in 3 languages**:

- **4p Cover** + **24p Matter**
- Advert part: **4 pages** for **2 language versions only**

### Quantities:

- **Cover**:
  - English edition: 6,200 pcs.
  - Italian edition: 2,800 pcs.
  - German edition: 3,000 pcs.
- **Text/Matter**:
  - English edition: 6,200 pcs.
  - Italian edition: 2,800 pcs.
  - German edition: 3,000 pcs.
- **Adverts part**:
  - 4 pages for the English and German edition only.

## How to Set the Data for this Example?

### Product Versions

To begin the versioning process, the different **Product Versions/Parts** must be defined. This is done from the **Case Card**. In the **Jobs** section, use the **Product Versions** action where you simply enter Text and Quantity.

- **English Edition**, Quantity: 6,200
- **Italian Edition**, Quantity: 2,800
- **German Edition**, Quantity: 3,000

Instead of just entering the text description, a **Product or Finished Goods Item No.** can also be selected.

## Further Steps

The following steps are required, but not described in detail here. Refer to the specific documentation links for detailed instructions.

### Create Sheets / Job Items:

1. **Cover**:
   - 4 pages.
   - Format code/size: e.g., 20x28 cm or 8.5x11 in.
   - Select paper and press.

2. **Text**:
   - 24 pages.
   - Format code/size: e.g., 20x28 cm or 8.5x11 in.
   - Select paper and press. (Depending on the size, PrintVis might create a residual sheet.)

3. **Adverts**:
   - 4 pages.
   - Format code/size: e.g., 20x28 cm or 8.5x11 in.
   - Select paper and press.

### Create Variants:

- Use the **Versions/Variants** action on the **job items** subpage.
- Variants can be automated or manually amended.
- In this example, delete/do not add the variant for the adverts from the **Italian Edition**.

Refer to: **Create Variants**.

### Combine Sheets / Variants:

- Use the **Combine Variants** action on the **job items** subpage.
- Combine the variants on the sheet and/or create plate changes as needed.

Refer to: **Combine Variants**.

## See Also

- <a href="../pvscasemanagement/" target="_self">Case Management</a>
- Create Variants
- Combine Sheets / Variants