# Job Tickets

The Job Ticket is the primary production document in PrintVis. It provides production staff with all the information they need to produce a job, including specifications, quantities, materials, and process instructions.

## Usage

Job Tickets are used by:
- **Press operators** — For printing specifications (format, colors, stock)
- **Pre-press staff** — For file specifications and plate information
- **Finishing staff** — For binding, cutting, and finishing instructions
- **Warehouse** — For material requirements and shipping information

### Job Ticket Content

A Job Ticket typically includes:

- **Job header** — Customer, order number, job name, deadline
- **Quantities** — Ordered quantity, delivery quantity, additional quantity
- **Format and paper** — Format code, paper description, weight
- **Colors** — Colors front and back, special inks
- **Imposition** — Sheet layout, pages per sheet
- **Per-department instructions** — Each department section shows the relevant production data

The content and layout of the Job Ticket is controlled by:
- **General Setup** — Job Ticket layout (1 or 2 columns), text wrap widths
- **Departments** — Which departments are included, their order, and minimum lines
- **User Fields** — Custom fields per department
- **Job Ticket comments** — Internal comments linked to departments

### Printing the Job Ticket

Job Tickets can be:
- Printed from the Case Card (Print → Job Ticket)
- Printed from the Planning Board when a job is scheduled
- Automatically printed when a case changes to a specific Status Code
- Viewed on the Shop Floor as a digital document

## Setup

### Job Ticket Layout Configuration

1. Open **General Setup**.
2. In the Estimating section, configure:
   - **Job Ticket Layout** — 1 column or 2 columns
   - **Text Wrap Full Width** — Characters before wrapping external description (default 130)
   - **Text Wrap Comments** — Characters before wrapping job comments (default 130)
   - **Text Wrap User Fields** — Column width for user field input (default 90 for 2-column)
   - **Job Ticket Copies** — Number of copies to print

### Department Configuration for Job Ticket

For each department that should appear on the Job Ticket:
1. Open the Department record.
2. Set **Job Ticket Group** to a number greater than 0 (departments with 0 are hidden).
3. Set the **Sorting Order** to control placement on the ticket.
4. Enable **Include User Fields** and select **Group User Fields** if user fields should print.
5. Enable **Job Ticket Comments** if comments linked to this department should print.

## Examples

### Example: Job Ticket for a 4-Color Brochure

**Header:**
- Customer: ABC Corp | Order: 25001 | Deadline: July 15
- Job: Company Brochure Q1 | Quantity: 1,000

**Pre-press Section:**
- 4 plates required (CMYK)
- File: brochure_abc_final.pdf
- Proof approved by: Jane Smith

**Press Section:**
- Format: A4 | Stock: 130gsm Gloss Coated
- Colors: 4/4 | Sheets: 260 gross
- Machine: Heidelberg SM74

**Finishing Section:**
- Fold: Half-fold
- Saddle Stitch: 2 staples
- Trim: 3-sided, finished size 210 × 148mm

## See Also

- [Report Setup](report-setup.md)
- [Departments](../case-management/departments.md)
- [General Setup](../setup/general-setup.md)
- [Shop Floor](../shop-floor/shop-floor.md)
