# Job Material Movement/Pick

The Job Material Movement/Pick Report is used to move raw materials to the cost centers for use or consumption, depending on the company setup. This report will pull in all materials needed based on the filter settings, including replacement reservation items.

## Use of Job Material Movement/Pick

The report will generate the appropriate warehouse **Movement Worksheets** when the directed warehousing is used. The only required fields are the **Location Code** set to the used direct warehouse, and the **Name** of the Warehouse movement can be selected.

The report will generate the appropriate **Internal Movement** worksheet when the **Bin Mandatory** warehousing is used. The only required field is the **Location Code** set to the used bin mandatory warehouse.

The report will generate the **PrintVis** **Material Delivery Journal**, which performs based on the **Job Costing Journal** settings when the basic (inventory only) warehousing is used. The only required field is the **Job Costing Journal**. The **Job Costing Journal** settings direct how the material is moved or consumed when posted.

The following fields are utilized in all warehousing setups:

- **From Date** - use this field to find material needs based on a specific start date (no earlier than).  Leave this field blank to pull from all orders.
- **To Date** - use this field to find material needs based on a specific end date (no later than).  Leave this field blank to pull from all orders.
- **Order No**. - use this field to find material needs specific to an order. Leave this field blank to pull from all orders.

It should also be noted that the Job Material Movement/Pick process only looks at items that have a quality code set with "Raw Material Pick" checked.

## See Also

- <a href="../pvsmaterialreq/" target="_self">Material Requirements</a>
- <a href="../location/" target="_self">Locations</a>
- <a href="../item/" target="_self">Item</a>
- Job Costing Journal