# Business Central Touchpoints

PrintVis integrates with Business Central to provide a vertical-specific solution for the print industry. The seamless integration between the two products results in several touchpoints where the systems interact.

## Usage

The following topics outline key integration points between Business Central and PrintVis. Understanding these touchpoints helps avoid incorrect setup and confusion about when PrintVis handles a function differently from standard Business Central.

### Key TouchPoint Areas

| Touchpoint | Description |
|---|---|
| **CRM Functionality** | PrintVis uses Business Central CRM for opportunity and contact management. Cases can be linked to BC opportunities. |
| **Item Card** | Items used in PrintVis (paper, consumables, finished goods) are BC items. PrintVis adds item type codes and qualities on top of BC item functionality. |
| **Purchasing** | Purchase orders for subcontracting and materials flow through standard BC purchasing. PrintVis provides a Purchase Guide for job-linked purchasing. |
| **Reservations** | Material reservations for jobs are managed through PrintVis material requirements linked to BC inventory. |
| **Item Consumption (Shop Floor)** | When shop floor users declare production, material consumption posts through BC item ledger entries. |
| **Material Movement / Pick** | PrintVis job material movement creates BC warehouse or inventory picks. |
| **Shipments** | PrintVis provides its own Shipment Card as an alternative to BC Sales Shipments. Standard BC shipments can also be used. |
| **Finished Goods Items** | Finished goods produced by PrintVis jobs post to BC inventory as item ledger entries. |
| **Invoice** | PrintVis invoice drafts post through BC Sales Invoices, using BC G/L posting setup and invoice posting groups. |
| **Work in Progress (WIP)** | PrintVis WIP journals post to BC G/L accounts defined in PrintVis G/L Posting Setup. |
| **G/L Posting Setup** | PrintVis has its own G/L posting setup that maps production costs, WIP, and invoicing to BC general ledger accounts. |

### PrintVis Functionality That Replaces BC Manufacturing

PrintVis does **not** use the Business Central Manufacturing module. A **Premium license is not required**. PrintVis replaces:

| BC Manufacturing Function | PrintVis Replacement |
|---|---|
| BOMs and Routings | Calculation Units and Templates |
| Sales Orders (for jobs) | PrintVis Cases |
| Resource Scheduling / Schedule Board | PrintVis Planning Board |
| Shop Floor User Interface | PrintVis Shop Floor |

### Key PrintVis-Specific Features

- **Estimation and Calculations** — Replaces BC routing and BOMs. All production costs are estimated through Calculation Units.
- **Cases** — Replace Sales Orders for job management, tracking the full lifecycle from request through invoicing.
- **PrintVis Userfields** — Allow customer-specific information during quoting, ordering, production, and shipping. Reduces the need for customizations.
- **Planning Board** — Visual production scheduling linked to PrintVis Cases.
- **Shop Floor** — Job-specific interface with Job Ticket, Production Tile, and Tooltips.
- **Shipment Card** — Optional alternative to BC Sales Shipments for handling PrintVis job shipments.

## Setup

!!! warning "Missing Content"
    The BC Touchpoints themselves do not require dedicated setup beyond what is covered in other articles. For specific setup related to each touchpoint, refer to:

    - G/L Posting Setup → [G/L Posting Setup](../invoicing/gl-posting-setup.md)
    - Shipments → [Shipments](../shipping/shipments.md)
    - WIP → [WIP](../shop-floor/wip.md)
    - Items → [Items](../warehouse/items.md)

## Examples

### Example: Why PrintVis Does Not Need a Premium License

A printing company moving from a basic BC setup to PrintVis does not need to upgrade to a Premium BC license. PrintVis replaces BC Manufacturing entirely. The company uses:

- PrintVis Cases instead of BC Production Orders
- PrintVis Calculation Units instead of BC BOMs/Routings
- PrintVis Shop Floor instead of BC Shop Floor

This means that estimation, production tracking, and job costing all run through PrintVis without touching the BC Manufacturing module.

## See Also

- [G/L Posting Setup](../invoicing/gl-posting-setup.md)
- [Shipments](../shipping/shipments.md)
- [Shop Floor](../shop-floor/shop-floor.md)
- [Items](../warehouse/items.md)
