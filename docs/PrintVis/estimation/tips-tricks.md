# Estimation Tips & Tricks

This article consolidates practical tips and tricks for working with PrintVis estimation, including common scenarios and solutions that are frequently needed.

## Usage

### Maintain and Update Templates

When job requirements change (new speeds, new machines, new pricing), existing templates should be updated to reflect current conditions.

**To update a template:**
1. Open the template case/job directly.
2. Make the necessary changes to calculation units, speeds, or materials.
3. The changes automatically apply to all new cases using this template (but do not affect existing open cases).

!!! warning
    Avoid deleting and recreating templates. Update them in place to preserve any case history linked to the template.

### Specify the PrintVis Quote Report

The default quote report can be changed per case, order type, or system-wide. To specify which quote report is used:
1. In General Setup → **Default Order Document** — sets the system-wide default.
2. On individual Order Types → **Default Document** — overrides for that order type.
3. On the Case Card → **Quote Report** field (if visible) — overrides for that specific case.

### Mixed Configuration for Printing and Finishing

When a job has both printing and finishing on the same sheet (e.g., a press with integrated fold), set up the cost center with multiple operations in a single calculation unit that covers both the print and finish in sequence.

### Avoid Extra Surcharge Popups

If a surcharge (Additional Rate) is automatic but not always applicable, and the popup is creating unnecessary interruptions:
1. Open the Additional Rate setup.
2. Change the trigger from "Popup" to "Automatic" if the surcharge should always apply without confirmation.
3. Or set it to "Manual" if it should only be applied when deliberately selected.

### How PrintVis Creates Sheet Layout and Residual Sheets

PrintVis calculates how many job items (pages/products) fit on a press sheet based on the format code, imposition type, and page count. When the last sheet in a book has fewer items than a full sheet, PrintVis creates a "residual sheet" for the remaining pages.

Residual sheets can have different:
- Speeds (fewer pages may run faster)
- Make-ready times (same setup as full sheets)
- Paper specifications (same stock but different quantity)

### Getting the Right Make-Ready on Residual Sheets

To ensure correct make-ready calculation for residual sheets:
- Set up a separate Calculation Unit for residual sheets if the make-ready is different.
- Or use a formula that calculates make-ready based on whether it's a residual sheet.

### Using More than One Printing Process for a Sheet

A single sheet can go through multiple printing processes (e.g., CMYK on one pass, then a spot varnish on a second pass). To set this up:
1. On the Job Card, the sheet has multiple lines in the printing section.
2. Each line references a different List of Units (machine/process).
3. Each gets its own calculation units for make-ready and run.

### Setup Minimum Hours for an Operation

To ensure that very short jobs are charged a minimum time:
1. In the Calculation Unit for the operation, add a line with:
   - Minimum value = the minimum hours/minutes to charge
2. The system uses the higher of: calculated time OR the minimum.

Alternatively, configure this in the **Additional Rate** as a minimum charge.

### Speed Table Reduction

To reduce machine speed for specific conditions (heavy stock, special inks, quality requirements):
1. Open the Speed Table for the relevant cost center.
2. Add a line for the specific condition.
3. Set the speed to the reduced value.

Or set up a **speed reduction percentage** that applies automatically when certain conditions are met.

### Custom Formulas with Additional Quantities

For jobs where an extra quantity is needed beyond the standard ordered quantity (e.g., 10% overrun for packaging waste):
1. Create a Calculation Formula that adds the additional quantity.
2. Reference the formula from the relevant Calculation Unit line.
3. The formula reads the "Additional Quantity" field from the job and incorporates it.

### Custom Formula on a Speed Table

If speed varies based on a combination of format AND another variable (e.g., number of colors):
1. Create a Custom Formula that selects the appropriate speed from the speed table based on the job parameters.
2. Reference this formula from the calculation unit instead of referencing the speed table directly.

### Material Counted in Pieces but Calculated in Weight

For heavy materials (metal plates, thick cardboard) where the supplier prices by weight but you count pieces:
1. Set up the item with Unit of Measure = PCS for ordering/counting.
2. Set up a conversion factor (weight per piece) in the Unit of Measure setup.
3. In the Calculation Unit, calculate consumption in PCS but the system converts to weight for cost calculation.

### Consuming More Than One Paper in a Sheet

Some jobs use different papers for different sections of the same sheet (e.g., a self-cover brochure where the outer pages use a heavier stock). To handle this:
1. Create separate job items for the different paper stocks.
2. Each item gets its own calculation unit with its own paper line.

### Assigning Inks to Two or More Print Processes

When a job goes through two different print processes (e.g., offset then digital), each process gets its own ink specification:
1. On the Job Card, create a separate printing section line for each process.
2. Assign the appropriate colors to each process separately.

### Calculating Setup/Cleanup for Special Inks

Special inks (Pantone, UV, metallic) often require extra setup and cleanup time:
1. Add a separate Calculation Unit line for special ink setup.
2. Link it to an operation code for "special ink setup" with the appropriate time.
3. The line is automatically added when special inks are specified.

## Setup

!!! warning "Missing Content"
    Each tip above may require specific setup changes. Detailed step-by-step setup instructions for each tip are in the individual legacy documentation articles referenced below.

## Examples

The tips above include embedded examples within each section. For more detailed worked examples, refer to the legacy Estimation Tips & Tricks documentation.

## See Also

- [Calculation Units](calculation-units.md)
- [Speed Tables](speed-tables.md)
- [Additional Rates](additional-rates.md)
- [Calculation Formulas](calculation-formulas.md)
- [Special Scenarios](special-scenarios.md)
