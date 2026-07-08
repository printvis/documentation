# Special Estimation Scenarios

This article covers special estimation scenarios in PrintVis that require specific setup or workflow approaches beyond the standard estimation process.

## Usage

The following special scenarios are supported in PrintVis:

### Combined Sheets (Gang Printing)

Combined Sheets (ganging) allows multiple different jobs to be combined onto a single printing sheet to maximize press utilization. The gang job calculation handles the split of costs and materials across the combined jobs.

See also: [Combined Sheets](../../Pages/pvscombinedsheets.md) in the PrintVis Pages documentation.

### Continuous Fed Press

For web offset or other continuous-feed presses, a specific setup is required in PrintVis to handle the continuous paper feed, web width, and cutoff calculations.

Key differences from sheet-fed setup:
- Format is defined as web width + cutoff length
- Speed is typically measured in meters/hour or feet/minute
- Waste calculation accounts for web threading and splice waste

### Multipart NCR Forms

Multipart NCR (No Carbon Required) forms require special estimation setup to handle:
- Multiple parts (2-part, 3-part, 4-part sets)
- Interleaved paper types
- Collating and padding operations

### Ganged Production

Ganged production combines multiple customer orders for the same product type onto a shared press run. This is common for standard products like business cards, postcards, or rack cards.

- Jobs are planned as individual cases but combined on the press
- Costs are divided proportionally among the ganged jobs
- A gang job template is required (configured in General Setup)

### Newspaper Setup

Newspaper production requires specific setup for:
- Publication, edition, and section management
- Web press speeds and paper consumption
- Section-based planning and scheduling

### Price Concepts

PrintVis supports multiple pricing approaches:
- **Cost-plus pricing** — Price = Cost × Markup percentage
- **Market-based pricing** — Price set from a price list regardless of cost
- **Contribution margin pricing** — Price based on desired contribution to fixed costs

### Prepress Orders

Prepress orders can be managed as separate cases or as parts of a main production case. PrePress Status Codes and PrePress Product Groups (configured in General Setup) control how these cases are created and tracked.

### Quantity Variations and Over-Delivery

PrintVis supports setting tolerance percentages for quantity variations. When actual production exceeds or falls short of the ordered quantity, the system can handle:
- Over-delivery percentages
- Under-delivery minimums
- Automatic adjustment of invoiced quantities

### Publications and Editions

For publishers and magazine printers, PrintVis supports:
- Publication definitions
- Multiple editions per publication
- Section-based planning
- Subscription management integration

### Hourly Rate Scenarios

Complex hourly rate scenarios can be configured for situations where press rates vary based on:
- Time of day (shift differentials)
- Operator skill level
- Machine age/depreciation

## Setup

Each special scenario requires specific setup. Key setup areas:

| Scenario | Setup Location |
|---|---|
| Gang printing | General Setup → Gang Job settings |
| Continuous fed press | Cost Center Setup → Web Press configuration |
| Publications/Editions | General Setup → Show Publication Fields |
| Prepress orders | General Setup → PrePress settings |
| Quick Quote | Quick Quote Setup |

!!! warning "Missing Content"
    Detailed step-by-step setup instructions for each special scenario are not fully consolidated in this article. Refer to the individual legacy documentation articles for each scenario for detailed setup guidance.

## Examples

### Example: Setting Up for Gang/Combined Printing

1. Create a "gang job" case that serves as the master template.
2. In General Setup → Production, set:
   - **Gang Job Template** = the gang job case number
   - **Gang Job Status Code** = the status for new combined orders
   - **Gang Job Order Type** = the order type used for gang jobs
3. When creating a gang job, the system uses the template to set up the combined sheet structure.
4. Individual customer jobs are added as components of the gang job.
5. Costs are divided proportionally based on each job's share of the combined sheet.

## See Also

- [Combined Sheets](../../Pages/pvscombinedsheets.md)
- [General Setup](../setup/general-setup.md)
- [Estimation Overview](overview.md)
- [Templates](templates.md)
