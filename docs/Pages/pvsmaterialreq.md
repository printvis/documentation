# Material Requirements

The Material Requirement page (top list) displays information about Items to be consumed by the Case.

The bottom list displays the item reservation entries for the selected item in the top list (the reservation is listed as a negative number).

## How it works

The Material Requirement list is created when a **Case** receives a **Status** that requires a material list to be designated. The user can manually correct the calculated quantity. If the user purchases items via the **Purchase Guide**, the date the items are available in stock is displayed as well as a checkmark if the items have been picked/released from the inventory.

Meaning of the quantity fields:

- **Quantity** - the quantity estimated for the job.
- **Quantity Needed** - the quantity estimated minus the quantity reserved minus the quantity consumed. This value will never go below 0.
- **Reserved Quantity** - the base quantity of the item reserved.
- **PV Reserved Quantity** - the quantity reserved based on the reservation factor.
- **Open Qty From Purchase Orders** - the open purchase orders quantity that have not been received.

The **Inventory available date** is set based on the following order:

- The planned start date of the calculation unit where that material is attached.
- The requested shipment date.
- Today’s date.

By using the **Reserve** action, users can easily create standard reservations for selected items and subsequent replacements for those items. This can prevent scheduling snags caused by inadequate inventory.

## See Also

- <a href="../item/" target="_self">Item</a>
- Purchase Guide
- Job Material Item Replacement