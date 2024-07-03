# Sales Order Integration

For many years, PrintVis has been able to integrate from regular BC sales orders. 

The use-cases would be for example;

    The company sells printed items among other things which are just merchandise from a purchased stock
    The company often takes orders of different printed items and likes how this can be organized on a sales order
    The company sells a lot of re-orders and the customers orders by item numbers

The sales order lines offer a nice way to organize these orders in a way which is easy to understand for the sales staff. Each line can refer to its own production order and have a separate production route through production and status code flow. An alternative (more advanced and with complexity) is to use PrintVis Project Management. 

Over the years we've had many requests for changes to the way the Sales Order integration functions for specific customers with many of these requests conflicting with requests from other customers. This is the reason we have decided to provide this sales order integration as an Open Source app so partners/customers can modify this code directly to meet the exact customer requirements. 

The extension will add some fields to the sales order header and sales order lines. The extra fields can be identified by zooming (CTRL+ALT+F1) while on the header or line, the fields will be numbered in the 80101..80133 range.

## Prerequisite setup

**PrintVis General Setup**

The most important setup required is on the Sales/Purchase Order tab on the PrintVis General Setup page:

| Field                           | Options                                | Description                                                                                                                                                                                                                              |
|---------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sales Order Calculation Wait    | Yes/No                                 | From earlier versions, not active in PV20 and up. It has previously been used for ankering custom hooks.                                                                                                                                  |
| Restrict items to customer      | Yes/No                                 | From earlier versions, not active in PV20 and up. Setting to Yes will restrict the list of items which can be seen from the sales order line to only the items which has the same Sell-to Number in that field on the item card.          |
| Production Page                 | Case Card, Job Card, Quick Quote       | This choice indicates the preference for which page should come up for the user, when the sales order integration is used. Quick Quote requires background setup, but the other options will open The Case Card and the Job Card respectively, giving the user an opportunity to review the data taken from a product group template or a finished goods template. |
| PopUp Page from Sales line      | Never, Always, If no template          | From earlier versions, not active in PV20 and up. This field is a choice enabling PrintVis to open the Case Card triggered by a tick in the Production Order Field, the first time on each line only. This could be helpful for the user as it saves some clicks compared to the user choosing to open the case card from the line menu. The choice 'if no template' will look at whether there is a template on the item which has been chosen on this line.               |
| Dim1 Sale Mandatory             | Yes/No                                 | From earlier versions, not active in PV20 and up. Setting to Yes will insert a check to see if Global Dimension 1 is filled in on the Sales Order header before it creates a sales order with the Production Order tick field.            |

**PrintVis Product Groups**

A company may well have product groups which are handled in the sales orders in one way - and others in other ways when it comes to production and pricing.

There are 2 fields on the Product Group fields to consider: 

| Field                       | Options                   | Description                                                                                                                                                                     |
|-----------------------------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sales Order Production Method | One job per line, One job item per line | This field determines how PrintVis will add more items to the same PrintVis Case Card order. This will be explained below.                                                      |
| Salesorder price method     | Item Price, Estimated Value | This is a very important setting - it determines how the Price per Unit is set on the sales order line. This could either be taken from the Price field on the item Card or be taken from the estimated sales price on the active Job on the Case Card. |

**Items**

Some setup is required on the Item as well for the Sales order integration to work.

Generally, the items should be regarded as Finished goods items.

There are 2 types of items we can use.

    Specific customer goods, where the item number has a relatively full template
    Generic Dummy items, at least 1 dummy item per product group.
    These items will have a generic template but the customer requirements will be put on top to create a new product and production order in the Case Card. 

In both cases, some fields should be set up:

| Field       | Description                                                                                                                                                                                                                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Item Type   | Create an Item Type code (at least 1) with this Item Type. You can have more codes, for example to differentiate between real items and dummy items, and within these have many Quality Codes to create other filtering options if there are many goods ordered this way.                             |
| Sell-to No. | If this item is related to a customer, add the customer number here. This will allow for filtering and is required if you later on want to add more items to the same production order.                                                                                                              |

| Field                       | Description                                                                                                                                                                                                                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Template ID/Job/Version     | A template is required. This is specified by all 3 fields. If the template is full, not much more is needed. If we are producing many variants of basically the same item (same box/pouch/card, but for apples, bananas, strawberries and oranges) then we can point to a central template for the basics of the product and then add some information on the individual items. If we have a nice generic template we can also add information here in the following additional fields. |
| Formula Code                | This field is not one of the influencers, since the finished goods item is not likely to be mentioned in the estimation lines. So do not use in this relation.                                                                                                                         |
| Colors Front                | If filled out, this value will be transported to the job line and job item line of the Job and Job item which the integration creates.                                                                                                                                                 |
| Colors Back                 | If filled out, this value will be transported to the job line and job item line of the Job and Job item which the integration creates.                                                                                                                                                 |
| Reverse Printing            | This field is used for ESKO integration. It will not be relevant for Sales Order integration.                                                                                                                                                                                          |
| Imposition Code             | This field will impact the Imposition Code on the Job Item.                                                                                                                                                                                                                            |
| Product Group Code          | This field will, in relation to the Sales Order integration, is required to be filled in - and must match - the same value in the other 'pears and bananas' products if you are trying to put more products from sales order lines into the same job.                                   |
| Intent Group Product Group  | This is filled out if there is a structure of Quick Quote associated with the item. Typically this would be a product group dummy item. Most often this would be in conjunction with choosing QuickQuote as the Production Order option in the General Setup.                              |
| Paper No.                   | This field will, in relation to the Sales Order integration, is required to be filled in - and must match - the same value in the other 'pears and bananas' products if you are trying to put more products from sales order lines into the same job.                                   |
| Finishing                   | This field will, in relation to the Sales Order integration, is required to be filled in - and must match - the same value in the other 'pears and bananas' products if you are trying to put more products from sales order lines into the same job.                                   |
| Unwind                      | This field will, in relation to the Sales Order integration, is required to be filled in - and must match - the same value in the other 'pears and bananas' products if you are trying to put more products from sales order lines into the same job.                                   |
| Tool 1 (here, Select Die)   | The Tool fields are typically used with product group dummy items as these are a big factor in the construction of the item and would normally be pre-selected in the customer FG item.                                                                                                 |
| Tool 2 (here, Print Cylinder) | The Tool fields are typically used with product group dummy items as these are a big factor in the construction of the item and would normally be pre-selected in the customer FG item.                                                                                                 |
| Tool 3 (here, Select Knives) | The Tool fields are typically used with product group dummy items as these are a big factor in the construction of the item and would normally be pre-selected in the customer FG item.                                                                                                 |
| Tool 4 (here, Tool 4)       | The Tool fields are typically used with product group dummy items as these are a big factor in the construction of the item and would normally be pre-selected in the customer FG item.                                                                                                 |

## Using the sales order integration

The sales order integration is available when the extension has been installed (see beginning of this article).

The Sales Order Integration concists of an automated creation of a PrintVis Case Card complete with a job and estimation, based on the choice of an eligible item and activating the Production Order field. It is operating normally in other aspects than this.

Prerequisite to starting this proces, the Status Code field on the Sales Header must be set to a status code of type Order. If not, the system will throw an error to remind the user to do so.

On the Case Card, the status Code and the Order Type plus various other fields will be copied from the values set on the Sales header.

On the sales line, the user chooses the item in question by number or other search - as normal.

Data from the item card will flow to the sales line.

After the quantity is entered, you can now initiate the integration:

..and you have now created a PrinVis Case Card with information from the template and from the item.

The quality of the estimation depends upon the setup and preparation.

You can now access the Case Card and job through the 2 PrintVis Line menus:

| Action                 | Description                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Production order       | This action opens the relevant screen as chosen in the PrintVis General setup: Case Card / Job Card/ Quick Quote.                                                                                                                                                                                                                                                                   |
| Job                    | This action opens the active Job Card.                                                                                                                                                                                                                                                                                                                                              |
| Estimation             | This action opens the active estimation for the job.                                                                                                                                                                                                                                                                                                                                |
| Milestone              | This action opens the milestone page. If the Case Card is not in a status where the planning is active yet, then the page will be empty. It is possible to add milestones to the empty list. These will blend in with the automatically created milestones which would come when the case reaches a status code which enables job planning.                                              |
| Copy Production Order  | This action allows the user to copy a job from previous orders and add these in to the case card. Although rarely used, the use-case could be a wish to replace the item template with another one - or add an extra job to the case card for packing/fulfillment orders.                                                                                                            |
| Item Card              | This action opens the item mentioned on the line.                                                                                                                                                                                                                                                                                                                                   |
| Freight Rates          | This action opens the Freight charges choices available for this customer - for inspection. There needs to be a setup of freight charges to support this.                                                                                                                                                                                                                            |
| No. Series             | This action opens a page to manage the number series (if used) for individual Finished Goods delivered to a certain customer.                                                                                                                                                                                                                                                       |

When the Sales Order integration has been activated, there will be 1 or more Case Cards related to the Sales Order.

From the Sales Order the user could now create and send confirmations to the customer - or choose to send confirmations from the individual Case Cards. This depends on preference and will of course require documents accordingly.

The User can now move the status code ahead on the Sales Order and move the individual Case Cards on to production when confirmed. Each Case will now run its course in the workflow.

As the production is moving along, the Status Code field on the Sales Order header will be updated from the Case Card with the least advanced stage. 

When things are ready to deliver, this will be visible.

To be practical, the handling from the Sales order requires the Shop Floor to put the goods on stock, using the correct location (if that is used). Then the user can complete the order by Shipping and/or invoicing the order.

The invoices Sales will now become a Posted invoice and/or an Archived Sales Order.

The Case Cards will, provided the status code setup is aimed at it, automatically move to Archive.