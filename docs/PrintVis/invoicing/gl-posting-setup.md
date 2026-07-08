# G/L Posting Setup

The PrintVis G/L Posting Setup maps PrintVis production activities to Business Central General Ledger accounts. This ensures that production costs, WIP, and invoicing are all posted to the correct accounts in the chart of accounts.

## Usage

The G/L Posting Setup is used whenever PrintVis posts financial transactions to the general ledger:
- **Job costing entries** — Time and material costs posted to expense accounts
- **WIP posting** — Moving accumulated costs to WIP balance sheet accounts
- **Invoice posting** — Revenue posted to sales accounts
- **Subcontracting** — Purchase costs linked to job costing

A well-configured G/L Posting Setup ensures that:
- Financial statements accurately reflect production costs
- WIP balances correctly represent work in progress
- Invoice revenue is posted to the correct accounts by product type

### Structure of G/L Posting Setup

The G/L Posting Setup works in combination with Business Central's existing posting setup:
- BC already handles the core financial posting (Customer Posting Groups, Gen. Posting Setup, VAT)
- PrintVis adds additional mappings specifically for production costs and WIP

## Setup

1. Search for **PrintVis G/L Posting Setup**.
2. Configure account mappings for each combination of Department/Cost Center and posting type.

### Key Account Mappings

| Account Type | Description |
|---|---|
| **WIP Account** | Balance sheet account for WIP. Debit when posting WIP, credit when invoiced. |
| **Cost of Goods Sold** | Expense account for production costs when jobs are invoiced. |
| **Direct Cost Account** | Account for direct material and labor costs. |
| **Overhead Account** | Account for overhead/indirect cost absorption. |

!!! warning "Missing Content"
    Detailed field-by-field setup instructions for the PrintVis G/L Posting Setup are not fully consolidated in this article. Refer to the legacy G/L Posting Setup documentation for complete field descriptions.

## Examples

### Example: Basic G/L Account Structure for a Print Shop

| Account | Description | Type |
|---|---|---|
| 1400 | Work in Progress | Balance Sheet (Asset) |
| 4000 | Sales Revenue | Income |
| 5000 | Direct Labor | Expense |
| 5100 | Direct Materials | Expense |
| 5500 | Overhead | Expense |
| 6000 | Cost of Goods Sold | COGS |

## See Also

- [WIP](../shop-floor/wip.md)
- [Invoicing](invoicing.md)
- [Job Costing](../shop-floor/job-costing.md)
