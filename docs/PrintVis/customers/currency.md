# Currency Management

Currency management in PrintVis follows Business Central's standard currency functionality. Cases, invoices, and price lists can be set up in foreign currencies for international customers.

## Usage

Currency is used on:

- **Customer Card** — A default currency can be set per customer; cases for that customer default to the customer's currency
- **Case Card** — The currency for a specific case can be set or overridden
- **Price Lists** — Price lists can be created in specific currencies
- **Invoicing** — Invoice drafts use the currency from the case; BC handles exchange rate conversion on posting

When a case is in a foreign currency, PrintVis displays prices in the case currency. BC handles the exchange rate conversion when the invoice is posted to the general ledger.

## Setup

Currency setup follows standard Business Central configuration:

1. Search for **Currencies** in Business Central.
2. Add all currencies your company uses.
3. Set up **Currency Exchange Rates** — either manually or via an automatic currency feed.
4. Assign default currencies to foreign customers on the **Customer Card**.

!!! note "Exchange Rates"
    Exchange rates must be kept up to date for accurate invoicing. BC supports automated exchange rate updates via the Exchange Rate Service.

## Examples

!!! warning "Missing Content"
    No PrintVis-specific currency examples are currently documented. Currency management in PrintVis follows standard BC currency practices. Refer to Business Central documentation for exchange rate and currency setup details.

## See Also

- [Customers](customers.md)
- [Invoicing](../invoicing/invoicing.md)
- [Price Lists](../estimation/price-lists.md)
