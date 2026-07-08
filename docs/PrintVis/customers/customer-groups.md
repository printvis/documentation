# Customer Groups

Customer Groups are used in PrintVis to categorize customers for statistical purposes, workflow management, and QA checklist assignment.

## Usage

Customer Groups are used in:

- **Responsibility Areas** — Define a specific workflow or responsible person for all customers in a group
- **QA Setup** — Apply specific QA checklists to cases for customers in a specific group
- **Analysis** — Segment sales and production data by customer group
- **Price Lists** — Customer-group-specific pricing

## Setup

Customer Groups are set up in Business Central. Search for **Customer Price Groups** or **Customer Groups** depending on your BC version and PrintVis setup.

Assign a Customer Group to a customer on the **Customer Card** in the appropriate field.

!!! warning "Missing Content"
    Detailed setup steps and field descriptions for Customer Groups specific to PrintVis are not fully documented in the available source material. The customer group functionality is part of Business Central's standard customer management. Contact PrintVis support for guidance on PrintVis-specific customer group configuration.

## Examples

### Example: Using Customer Groups for Workflow Control

A printing company has two types of customers: **Retail** (individual jobs) and **Publishing** (high-volume, repeat jobs). They want different workflows for each:

1. Create customer groups: RETAIL and PUBLISHING.
2. Assign the appropriate group to each customer.
3. In **Responsibility Areas**, create rows for each Status Code with Order Type and Customer Group specified:
   - Status Code QUOTE + Customer Group PUBLISHING → Responsible = Senior Estimator
   - Status Code ORDER + Customer Group PUBLISHING → Responsible = Publishing Coordinator
4. Cases for publishing customers now automatically route to the publishing-specific team.

## See Also

- [Customers](customers.md)
- [Responsibility Areas](../case-management/responsibility-areas.md)
- [Quality Assurance](../case-management/qa.md)
