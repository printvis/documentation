# Quick Quote

Quick Quote is a streamlined quoting feature in PrintVis designed for creating fast estimates for simple, repetitive, or standard products. It provides a simplified interface compared to the full estimation workflow, enabling salespeople to generate quotes quickly without needing deep estimation knowledge.

## Usage

Quick Quote is used when:
- A customer requests a quick price for a standard product
- The product has been estimated before and the parameters are well-known
- Speed of quoting is more important than detailed cost breakdown
- Salespeople (non-estimators) need to generate quotes independently

Quick Quote works by using pre-configured Quick Quote templates that define the parameters and pricing for standard products. The salesperson selects the template, enters the key variables (quantity, pages, format), and the system calculates the price.

### How to Use Quick Quote

1. Open **Quick Quote** from the Case Card or the Quick Quote menu.
2. Select the Quick Quote template for the product type.
3. Enter the key job parameters:
   - Quantity
   - Number of pages (if applicable)
   - Format
   - Colors
4. The system calculates the price based on the template's pricing rules.
5. The quote can be printed or sent directly.
6. If the customer accepts, the Quick Quote can be converted to a full case with a detailed estimate.

## Setup

Quick Quote requires setup in two areas:

### Setting Up Quick Quote Templates

1. Search for **Quick Quote Setup** or access via the Estimation menu.
2. Create a Quick Quote template for each standard product.
3. For each template, define:
   - The product parameters (quantity ranges, format ranges, page ranges)
   - The pricing rules (how price is calculated from the parameters)
   - The associated estimation template (for conversion to full estimate)

### Assigning Quick Quote Access

Quick Quote can be accessed from:
- The Case Card (Quick Quote action)
- The Quick Quote list (for managing multiple quick quotes)
- Configured as a shortcut on role centers for salespeople

## Examples

### Example: Quick Quote for Business Cards

A print shop creates a Quick Quote template for standard business cards:

- Template: BUSINESS-CARDS
- Parameters: Quantity (250, 500, 1,000, 2,500, 5,000)
- Format: Standard 3.5" × 2" or 85mm × 55mm
- Colors: 4/4 (full color both sides)
- Pricing: Pre-calculated price grid per quantity

When a customer calls asking for business card pricing:
1. The salesperson opens Quick Quote, selects BUSINESS-CARDS.
2. Enters quantity = 1,000.
3. The system immediately shows the price.
4. The salesperson emails the quote without involving an estimator.

## See Also

- [Estimation Overview](overview.md)
- [Creating an Estimate](creating-estimate.md)
- [Templates](templates.md)
