# Analysis Pages

PrintVis Analysis Pages provide built-in reporting and analysis tools for monitoring business performance. They enable management and sales teams to analyze quotes, orders, job costing, and production data without needing external BI tools.

## Usage

Analysis Pages are used to:
- Monitor open quotes and their status
- Analyze rejected quotes (with rejection reasons)
- Review job complexity and production performance
- Compare estimated vs. actual costs
- Track order deviation (planned vs. actual)

### Available Analysis Pages

| Page | Description |
|---|---|
| **PrintVis Open Quotes** | Shows all open quote cases — useful for sales management and follow-up. Filter by salesperson, customer, order type, etc. |
| **PrintVis Rejected Quotes** | Shows all rejected quote cases with rejection reasons — useful for analyzing win/loss trends. |
| **PrintVis Case Complexity** | Analyzes case complexity metrics — helps identify which types of jobs are most complex to estimate. |
| **Job Costing Analysis** | Compares estimated vs. actual time and materials for completed jobs. |
| **Order Deviation Report** | Shows the deviation between planned production dates and actual completion dates. |

### Using Status Codes for Analysis

Status Codes are the foundation for all case-based analysis. By assigning meaningful types (Request, Quote, Order, Production Order) to status codes, the system can accurately filter and categorize cases for analysis.

## Setup

Analysis Pages use data from Case Cards, Status Codes, Rejection Codes, and Job Costing. To get the most from analysis:

1. Ensure all Status Codes have the correct **Type** assigned (Request, Quote, Order, Production Order).
2. Set up **Rejection Codes** so rejected quotes have meaningful reasons.
3. Ensure Job Costing is being posted (either directly or via journals).
4. Configure User Fields and Case data for the dimensions you want to analyze.

!!! warning "Missing Content"
    Detailed setup and usage documentation for each individual Analysis Page is not fully consolidated in this article. Refer to the legacy Analysis Pages documentation for details on each report.

## Examples

### Example: Analyzing Quote Win Rate by Salesperson

1. Open **PrintVis Open Quotes**.
2. Filter by date range (e.g., current quarter).
3. Group by **Salesperson**.
4. Compare the number of quotes sent vs. converted to orders.

Then open **PrintVis Rejected Quotes** with the same filters to see:
- How many quotes were rejected
- The most common rejection reasons per salesperson

This analysis helps identify whether certain salespeople need pricing support, faster turnaround, or additional training.

## See Also

- [Rejection Codes](../case-management/rejection-codes.md)
- [Status Codes](../case-management/status-codes.md)
- [Job Costing](../shop-floor/job-costing.md)
- [Power BI](../../PowerBI/index.md)
