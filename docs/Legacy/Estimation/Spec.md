# Specification Page


## General Page Layout


- The page layout adapts based on the type of printing machine (sheet-fed, web-fed, continuous).

![Specification Page 1.jpg](./assets/Specification Page 1.jpg)

- The layout includes several FastTabs that display relevant fields for each type of machine.

- Access the specification page from various locations: case card job line, job card, estimating page.

---

## Sheet-Fed Machines

### Sheet Information

![Specification Page 2.jpg](./assets/Specification Page 2.jpg)

- Contains fields for raw material and printing sheet information.
- Use the "Show more fields" option if needed to view additional fields.

### Quantity
- Displays net and gross quantities for printing and raw material sheets.

![Specification Page 3.jpg](./assets/Specification Page 3.jpg)

---

## Web-Fed Machines

### Web Information

![Specification Page 4.jpg](./assets/Specification Page 4.jpg)

- Contains fields specific to web-fed printing.
- Units for area or length are configured in the setup; printing is shown in the selected unit (e.g., linear meters).

### Quantity

![Specification Page 5.jpg](./assets/Specification Page 5.jpg)

- Displays net and gross quantities for printing.
- PrintVis calculates based on rotations.

---

## Continuous Machines

### Continuous Information

![Specification Page 6.jpg](./assets/Specification Page 6.jpg)

- Specific fields for continuous machines.

### Quantity

![Specification Page 7.jpg](./assets/Specification Page 7.jpg)

- Displays net and gross quantities for printing.
- PrintVis calculates based on length (e.g., linear meters).

---

## General - For All Machines

### Job Items

![Specification Page 8.jpg](./assets/Specification Page 8.jpg)

- Shows data for job items on the selected sheet.
- To add job items:
  1. Create space using the "PartSheet…" fields.
  2. Press "Extra Job Item" to add another job item.
  3. Repeat as needed.
- Customizable columns and sorting options.

### Parameters

![Specification Page 9.jpg](./assets/Specification Page 9.jpg)

- Displays machine configuration parameters.
- Values can be adjusted to influence imposition (e.g., reducing gripper space if not needed).

### Imposition showing a picture

![Specification Page 10.jpg](./assets/Specification Page 10.jpg)


### Imposition showing the PrintVis imposition drawing

![Specification Page 11.jpg](./assets/Specification Page 11.jpg)


- Displays either PrintVis imposition drawing or a picture.
- Pictures can be CIP4 folding catalog types or manually added images (e.g., packaging layouts).
- Requires a designated folder in PrintVis Folder setup for imposition files.

![Specification Page 12.jpg](./assets/Specification Page 12.jpg)


### Special Job Items - Packaging

![Specification Page 13.jpg](./assets/Specification Page 13.jpg)


- For packaging companies needing CAD layouts.
- Fields are limited; typically only "Pages in Sheet" is needed.
- This FastTab is not shown by default but can be displayed by personalizing the page.
