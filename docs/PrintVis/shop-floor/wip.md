# WIP (Work in Progress)

WIP (Work in Progress) in PrintVis tracks the production costs that have been incurred for jobs that are not yet invoiced. WIP posting transfers the accumulated job costs from expense accounts to WIP balance sheet accounts, enabling accurate financial reporting during production.

## Usage

WIP is used to:
- Track the value of work that has been started but not yet invoiced
- Provide accurate financial reporting for open production jobs
- Post production costs to WIP accounts at month-end
- Reverse WIP when jobs are invoiced

### WIP Workflow

1. Production time and materials are registered on the shop floor.
2. Job costing entries accumulate against the case.
3. At month-end (or when needed), WIP is posted:
   - Debit: WIP Asset Account
   - Credit: Expense/COGS Account
4. When the job is invoiced, WIP is reversed.

### WIP Setup and WIP Journal

The WIP Setup and WIP Journal pages allow you to:
- Configure which G/L accounts are used for WIP posting
- Review WIP entries before posting
- Post WIP to the general ledger
- View posted WIP entries

## Setup

WIP posting requires G/L account setup in the PrintVis G/L Posting Setup:

1. Search for **PrintVis G/L Posting Setup**.
2. Configure the WIP accounts for each department or cost center.
3. Set up the WIP posting method (by department, by product group, etc.).

See also: [G/L Posting Setup](../invoicing/gl-posting-setup.md)

!!! warning "Missing Content"
    Detailed step-by-step WIP setup and workflow documentation is not fully consolidated in this article. Refer to the legacy WIP Posting and WIP Setup documentation for detailed setup and posting procedures.

## Examples

!!! warning "Missing Content"
    No specific WIP examples are currently documented in this article. Refer to the legacy WIP Posting documentation for posting examples.

## See Also

- [G/L Posting Setup](../invoicing/gl-posting-setup.md)
- [Job Costing](job-costing.md)
- [Shop Floor](shop-floor.md)
