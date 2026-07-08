# Report Setup

PrintVis uses reports for job tickets, quotes, order confirmations, invoices, and analysis. Report Setup controls which reports are used for each document type and how they are formatted.

## Usage

Report Setup is used to configure:
- Which report is used for each document type (quote, order, job ticket, invoice, etc.)
- Default reports assigned per Order Type or Product Group
- Shipping document reports
- When and how reports are automatically triggered (e.g., auto-print on status change)

### Report Selection

PrintVis uses BC's standard Report Selection pages for defining which reports to use for sales documents (quotes, invoices, etc.). PrintVis-specific reports are added to the selection for print-specific documents.

## Setup

### PrintVis Report Setup

1. Search for **PrintVis Report Setup**.
2. Configure which report to use for each PrintVis document type.

| Document Type | Description |
|---|---|
| **Quote** | Report used for printing/sending customer quotes |
| **Order Confirmation** | Report for order confirmations |
| **Job Ticket** | Report for the production job ticket |
| **Invoice** | Report for invoices (also configured in BC Report Selections) |
| **Delivery Note** | Report for delivery/packing slips |

### Job Ticket Setup

Job Ticket layout and content is also influenced by:
- **General Setup** — Job Ticket layout (1 or 2 columns), text wrap settings
- **Departments** — Which departments appear on the job ticket and their order
- **User Fields** — Whether user field groups are included per department

### Report Setup for Shipping Documents

Shipping document reports are configured separately:
1. Search for **PrintVis Report Setup - Shipping**.
2. Configure shipping document reports for each shipping agent or document type.

## Examples

!!! warning "Missing Content"
    Specific Report Setup examples are not fully documented in this article. Refer to the legacy Report Setup documentation for detailed configuration examples.

## See Also

- [Job Tickets](job-tickets.md)
- [General Setup](../setup/general-setup.md)
- [Departments](../case-management/departments.md)
