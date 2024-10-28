# PVS Purchase Guide

Via the Purchase Guide, it is possible to order necessary items for an order directly from the **Case Card** or from the **Material Requirements**.

The Purchase Guide is typically used for creating purchase orders/quotes for the purchase of items and services such as subcontracting, items purchased specifically for the order, and, in a few cases, purchase of inventory-controlled items.

To be able to order an item via the Purchase Guide, you must make sure the item has a “**Quality Code**” attached on the **Item Card** which is selected for "**Use Purchase Guide**". Furthermore, it is required that the **Case** has reached “order” status or has “**Remove Material Requirements**” on the “**Status Code”** set to “No”.

The window is divided into 3 sections. At the top, the material lines are displayed, which are included in the calculation, and which need to be purchased (by setup on “**Quality Code**”). In the middle part, the purchase orders or quotes, which have been created via the purchase guide, are displayed. Finally, at the bottom are the posted purchases for the Case.

## How it works

To process the Purchase Guide lines, the lines need to have the ordering quantity and vendor number completed. The “**Expected Delivery Date**” is calculated by taking the “**Lead Time Calculation**” value from the **Item Card**. The “**Expected Delivery Date**” can be modified manually and will be used as "**Due Date**" on the requisition worksheet and “**Expected Delivery Date**” on the purchase line.

The next step is to enable one of the following Booleans to choose the result when hitting the action "**Create Purchase**":

- **Create Order** or **Create Quote** \- This will create a **Purchase Order** or **Purchase Quote** line for the related item. The system will find the last Purchase Order against the vendor. If that is released, it will create a new Purchase Quote/Order. If the last Purchase Quote/Order is open and refers to the same vendor, the system will add the quantity to that Purchase Order. Status field shows the status of the Purchase Order/Quote. This is beneficial if there are multiple Purchase Quote/Orders with a single vendor for a case.
- **Create Journal** - This will create a **Requisition Worksheet** line for the related item. The requisition worksheet to be used for this process is set up in the **PrintVis User**. **Create Journal** is being used in case the coordinator does not do a purchase quote/order by himself. With this option, (s)he can publish a line in a requisition worksheet that is used to form a centralized purchaser who will do the purchase.

The **Location** for the purchase order is based on the “**Purchase Location”** setting on the **Shop Floor** setup page. If the “**Purchase Location**” is set to **Vendor**, the Purchase Guide will use the “**Location Code**” from the Vendor card. If the “**Purchasing Location**” is set to “**Cost Center**”, the Purchase Guide will use the “**Location Code**” from the “**Cost Center**”.

Main actions:

- **Create Purchase** - creates a Purchase Order or an Internal Purchase Quote. One or more lines are created in the **Purchase Quotes/Orders** section below.
- **Quote/Order** - opens the created Purchase Order or Purchase Quote from the middle section of this page.
- **Item Card** - opens the item card for the selected line.
- **Matrix** - from the Matrix menu, you can select the period and category of information that determines the criteria for the displayed values in the line (scroll to the right-hand side to see information about the items).

## See Also

- <a href="../pvsmaterialreq/" target="_self">Material Requirements</a>
- <a href="../item/" target="_self">Item</a>
- <a href="../pvscasemanagement/" target="_self">Case Management</a>