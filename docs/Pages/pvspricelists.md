# Using Price Lists

PrintVis Price Lists are available to be used on calculation details for operations, items, and subcontracting. An example for operational prices could be click cost on digital presses. Item prices could be agreements with the vendor where the prices differ from unit to unit. And there could be price lists with agreements about subcontracting cost with certain vendors and their services.

The fields **Vendor No., Vendor Name and Type**, or if it **Belongs to a specific Cost Center** are only used for information purposes.

The **Calculation Unit** and **Ordering Unit** are important. The quantities in the Price List Lines should always be related to the quantity on the calculation detail line, e.g. the unit from the calculation formula, whereas the Calculation Unit is the unit for the cost and price. For example, the quantity could be in pieces or, for paper, in sheets and the Calculation Unit could be the cost and price per 1000 sheets or for 100 kg.

> **Note:** The conversion into another unit from the quantity unit is only possible if the parameters for the conversion are available like the size and weight unit for paper on the item card.

## Dimensions

It is possible to set up several dimensions as parameters for entering the price list entries. More dimensions selected means more line combinations can be created as Price List Entries. Please make sure the quantity unit for the **Unit 1, Unit 2, and Unit 3 Dimension** is the same as the unit of the calculation detail line (Pcs/Weight/Length, etc.).

### Dimension formulas

When using formulas as dimensions, you can choose the formula number below the dimension field. The formula values will then be taken from the specific record related to the calculation detail where this price list is being used. Formulas that have no relation to the specific calculation detail cannot be used or will have a result of 0.

### Other Dimensions

When enabling one of the additional other dimensions, the related column for this dimension will be editable in the Price List Entries. For example, there could be special prices for certain **Customers or Customer Groups** and **Product Group** related prices.

The dimensions for **Price Group** and **Time Group** parameters can be selected by the user on the job or calculation unit (see **Estimating**). For example, there could be an impact from a manual input selection field. An example could be the user must choose if it is an average, complex, or simple job, which might have an impact on the cost and/or price. For that, the specific **Price Group** or **Time Group** must be set up and selected from the lookup.

## Preferences

In this section, it is possible to select additional parameters on filters to find the desired price list entry or to set **Min. or Max. values** for the Cost and Price.

For details, see the tooltips when hovering over the field captions with the mouse.

## Info

This section displays information about the date and user who created or last modified this record.

## Price List Entries

The **Price List Entries** reflect the cost and price data. Here, you can create a line for each dimension combination and its cost, overhead, and price. Please make sure for the **DIM 1, DIM 2, and DIM 3 Dimension**, that the quantity unit is the same as the unit of the calculation detail line (Pcs/Weight/Length etc.) and the **Calculation Unit** is the unit for the Cost and Price. For example, the quantity could be in pieces or, for paper, in sheets (unit is still pcs.!) and the Calculation Unit could be the cost and price per 1000 sheets or for 100 kg.

For details, see the tooltips when hovering over the field captions with the mouse.