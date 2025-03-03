# Invoice - Touchpoints between Business Central and PrintVis

## PrintVis Invoicing

Invoices created from PrintVis are standard Business Central Sales Invoices that posts directly on G/L Accounts because most PrintVis customers are not creating items/inventory for the production result.

PrintVis Invoice Template Codes can be setup and used on Sales Invoices to be able to create invoice lines based on PrintVis case information.

Invoices for a case can be based on:

- The confirmed amount only

- PrintVis shipments

- Business Central Posted Sales Shipments

	- For this, items are used and the invoice lines are created from posted shipments lines.

Other options for building invoices consist of:

- Job level

- Shipment

- Tax Area (based on shipments)


PrintVis G/L Posting Setup is required as well.


![Invoice - Touchpoints between Business Central and PrintVis.jpg](.assets/Invoice - Touchpoints between Business Central and PrintVis.jpg)


It is also possible to create invoices using the Invoicing Guide through the PrintVis Case Card, which also can use PrintVis Invoice Template Codes.

Invoicing through PrintVis is designed to have the possibility to invoice without shipping anything. Examples are prepress work, fulfillment packaging, and part invoicing. Also, more product can be shipped versus what the customer ordered, and this is setup by design for over deliveryivery opportunities.

PrintVis Invoice is designed to utilize the PrintVis Order No (which can also be linked to Sales Order) in order to build up the Sales Invoice.

