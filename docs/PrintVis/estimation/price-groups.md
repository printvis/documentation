# Price Groups

Price Groups in PrintVis allow you to define different pricing tiers that can be applied to customers or jobs. They provide a way to offer different pricing to different customer segments without setting up individual price lists for each customer.

## Usage

Price Groups are referenced in:
- Price List setup — price lists can be assigned to specific price groups
- Customer setup — customers can be assigned to a price group
- Calculation units — price group-specific rates can be defined

When a job is estimated for a customer in a specific price group, the system applies the pricing from the price list associated with that group.

## Setup

Price Groups are found by searching **PrintVis Price Groups**.

!!! warning "Missing Content"
    Detailed setup documentation for Price Groups is not fully available in the current source material. Contact PrintVis support or refer to the legacy documentation (Legacy/Estimation/PriceGroups.md) for detailed field descriptions.

## Examples

### Example: Common Price Groups

| Code | Description |
|---|---|
| STANDARD | Standard pricing |
| PREFERRED | Preferred customer pricing (5% discount) |
| WHOLESALE | Wholesale/reseller pricing (15% discount) |
| PREMIUM | Premium service pricing (10% premium) |

## See Also

- [Price Lists](price-lists.md)
- [Additional Rates](additional-rates.md)
- [Customers](../customers/customers.md)
