# PrintVis General Setup

The PrintVis General Setup page allows the company to set a number of standard parameters such as number series, invoicing, job costing, etc. The window consists of 12 sections, each containing information about specific parameters. The section content and function are described below.

## Menu

![General Setup 1](./assets/printvis General Setup 1.jpg)

| Function | Description |
| --- | --- |
| User Fields | View/Edit the General Setup integrated user fields. |
| Create PrintVis Standard Bitmaps | This will create the Standard Bitmaps system entries used in PrintVis. |

## Case Management

![General Setup 2](./assets/printvis General Setup 2.jpg)

| Field | Description |
| --- | --- |
| Application Type | PrintVis applies to Printing companies but also to other types of companies which may not use very specific printing pages and fields. For a unique, order-by-order production which is not based on production BOMs etc., PrintVis is the replacement for standard "Manufacturing" in 365 Business Central. PrintVis does not use BOMs or traditional routing. It is more the definition of job parts (called job "items," such as the cover and text of a book - its components) and the cost centers used for the production of those. If a company has different subsidiaries which are not all printing companies - and wants to use 365 Business Central without PrintVis, it is possible to disable the PrintVis functionality for those database companies. |
| General Manufacturing | Can be chosen if the print specific pages and fields will not be used. Estimation, document management, etc. will still work. |
| Print Manufacturing | Is used most of the time, any use of print specific description will benefit from the print specific pages. |
| Use Advanced | |
| Case Card | If enabled, the case card is a combination of the case card and job card, and the job is only opened to review the prices. It reduces the number of clicks for the user. The flow through all case details is: Case Card, Estimation, Specification. If disabled, the flow through all case details is: Case Card, Job Card, Estimation, Specification. |
| Quote No. Series | Quote No. Series relates to the "Code" field in table "No. Series". The Quote No. Series can be selected from the No. Series table. |
| Order No. Series | Order No. Series relates to the "Code" field in table "No. Series". The Order No. Series can be selected from the No. Series table. |
| Quote/Order no from Salesorder | This field relates to the Sales Order integration. If ticked, the Case Card quote or order number will be the sales order number, followed by a number. A Sales Order can be used to create several Case Cards and the xxx-1, xxx-2, etc. will make sure they are individually numbered for reference. |
| Shipment No. Series | Shipment No. Series relates to the "Code" field in table "No. Series". The Shipment No. Series can be selected from the No. Series table. This setup is mandatory, in case: Combined Shipments are in use The Case Shipment Method is set to "Create Posted Shipments" |
| Manual Contact Person | It is possible to enable or disable the ability for users of Case Cards to change the contact person which comes from the customer card. A tick in this field will enable this for the users. |
| Default Order Document | In Document Management, there may be several order confirmation documents. For automation of internal processes, it is an option to state a default document here. If the status changes to a status which generates an Order Number, this document may be automatically generated for the user. |
| Default Order Document Name | This field shows the Descriptive name of the default order document picked. |
| Search Name | The Case Card has a Search Name field which is updated from the user input. Here we can determine what is the most desired input: - Job Description - Customer Name |
| Exclude PrintVis Cases from Credit Limit check | By default, the quoted price on orders will be included in the total amount of the BC Credit Limit functionality. If this is not desired, you can switch this option on. Please note: The amount will include VAT in countries with VAT In countries with sales tax, the net amount will be included in the total amount |
| Do Not Show Customer Comments On Case Card | If a customer has comments attached to the customer card, these comments will be displayed by default after the customer is selected on a case card. If this is not desired, you can switch this option on. |
| Update Coupling Data Immediately | Immediately update coupled CRM data on changes. |
| Recreate Deleted CRM Data | If CRM data is deleted in the CRM system, checking this option will recreate this deleted information during the next update. |
| PrintVis Order CF Account No. | This field determines which Cash Flow Account the value of the PrintVis orders should be shown on. The use of this field requires active setup of Cash Flow. There is a white paper available on the setting and use of Cash Flow monitoring in PrintVis. |
| Additional Quantity | The business typical Additional Quantity is 1000 and this will be preset. However, for special companies, a smaller or larger additional quantity may be the usual, and this field may

# System Configuration Documentation

## Job Costing

### Location Production Released
When production is completed and goods are ready to ship, surplus materials may remain. This field designates the location for surplus materials when they are released from reservation.

### Auto Job Costing Journal
Relates to the "Code" field in the Job Costing Journal table. This journal is used for automatic posting of time and material to orders when production ends, based on the Unit of Measure for material and time calculation lines.

### Job Cost. Hour Unit Cost
Determines the costing method for job efficiency:
- **Default:** Uses standard time rates.
- **Weighted:** Adjusts recorded time based on user efficiency.
- **Actual:** Uses recorded hours with overtime considerations.

### Dim1 Job Costing Mandatory
Determines if Dimension 1 value is required for costing. Requires careful setup to avoid errors on the shop floor.

### Dim1 Job Costing Principle
If job costing is mandatory, this field specifies how to obtain the Dimension 1 value:
- **Manual:** User enters the value.
- **Case:** Value copied from the Case Card.
- **Department:** Value taken from the cost center's department.
- **User Department:** Value from the user's department field.

### Def. UoM Paper
Default Unit of Measure for paper if not specified on the item card.

### Def. UoM Plates
Default Unit of Measure for plates if not specified on the item card.

### Def. UoM Film
Default Unit of Measure for film if not specified on the item card.

### Def. UoM Die
Default Unit of Measure for die if not specified on the item card.

### UoM Slack Time
Defaults a unit of measure for slack time, used for tracking machine downtime and efficiency.

---

## Invoicing

### General Journal Templates
Specifies the General Journal Template for posting invoice lines.

### General Journal
Specifies the General Journal Batch for posting invoices.

### Dimension Allocation on Post
Determines if turnover should be allocated and re-posted according to dimensions when invoicing a customer.

---

## Posting

### Location Code Mandatory
Requires a location code for item-related transactions. Use NAV setup "Inventory Setup - field 'Location Mandatory'".

### Lock Archive Date
If checked, the Archiving Date on the Case Card is fixed and cannot be changed after its initial setting.

### Explode BOM on Posting
Decides if the Bill of Materials (BOM) should be expanded on posting:
- **Explode:** Expands the BOM.
- **Do not explode:** Does not expand the BOM.

---

## Logistics

### Copy Shipments
Specifies whether to copy shipments from an existing order when using the Copy To function:
- **Always**
- **Never**
- **Always but not combined shipment**

### Default Delivery Address
Determines the default address for shipments:
- **Sell-To Address:** Uses the customer address on the Case Card.
- **Sell-To Ship Address:** Uses the Ship-To Code address on the customer card.
- **No Address:** No address is copied from the case card.

### Receipt Merge Code
Defines the Merge Code for adding information lines on receipt documents.

### Way Bill Merge Code
Defines the Merge Code for adding information lines on shipment documents.

### Package Label Merge Code
Defines the Merge Code for adding information lines on package labels.

### Package Label Text 1…6
Sets fixed captions for up to 6 fields on the PrintVis Package Label, which should match merged text.

### Item Journal Template Name
Determines the Journal Template Group for posting items consumed from production.

### Item Journal Name
Determines the Item Journal used for posting items consumed from production.

### Warehouse Journal Template
Specifies the journal template for PrintVis integration in warehouse-related postings.

### Warehouse Journal Batch
Specifies the journal batch for PrintVis integration in warehouse-related postings.

### Create Shipment Item
Automatically generates a shipment item for distribution systems. Options include using a dummy item or generating a new item per shipment.

### Shipment Item Template
Template for creating new shipment items if an item is generated per shipment.

### Shipment Item No. Series
No. Series for numbering the new shipment items.

### Tax Area Code Mandatory on Shipment
Ensures the Tax Area Code is set on each shipment to avoid posting without it.

### Case Shipment Method
Defines how PrintVis shipments are processed:
- **No Sales Order:** Shipping managed through the PrintVis shipment card.
- **Create Sales Order Per Shipment:** Creates an open BC sales order.
- **Create Sales Order Per Shipment And Release:** Creates and releases a BC sales order.
- **Create Sales Order Per Shipment And Post:** Creates and posts a BC sales shipment.
- **Create Posted Shipments:** Creates a posted shipment directly.

### Shipment Sales Order Removal
Specifies when to remove the sales order after shipping:
- **On Ship (default)**
- **On Archive**
- **Never**

---

## Sales / Purchase Order

### Production Page
Specifies which page to display as the production plan:
- **Case Card**
- **Job Card**
- **Quick Quote**

### PopUp Page From Salesline
Determines if a popup page appears from a sales line:
- **Never**
- **Always**
- **If no template**

### Dim1 Sale Mandatory
Requires Dimension 1 on sales orders before creating a production order, copying it to the Case Card.

### Salesorder Calculation Wait
Not detailed, but typically relates to waiting periods in sales order calculations.

---

## Sales Shipment

### Ship Sales Order No. Series
No. Series for shipping sales orders.

### Ship Sales Invoice No. Series
No. Series for shipping sales invoices.

---

## Purchase Order

### Purchase Order No. from Sales Order
If selected, purchase orders created from sales orders receive the same number.

### Purchase Order No. Format
Defines formatting for purchase order numbers, allowing text before and/or after the number.

### Dim1 Purchasing
Specifies how Dimension 1 is set on purchase orders:
- **Manual**
- **PV Case**
- **Department**
- **User Department**
- **Purchaser Dimension**

### Dim1 Purchasing Mandatory
Requires Dimension 1 on all purchase orders.

### Purch. Order Paper Automatic
Activates automated paper purchase if eProcurement is set up.

### Purch. Order Paper Documents eProcurement
Activates paper purchase automation using eProcurement.

---

## Special

### Case Milestone 1 …10 Ok
Chooses milestones for presentation in the Production plan and Case Management overview.

### Report Production Plan
Replaces the standard Production Plan report with a customized version if needed.

### Report for Quote Description
Allows custom report for complex quote descriptions.

### Report Production Plan Milestones
Replaces the standard Milestones report with a customized version if needed.

---

## System

### Batch Manager Timer
Sets the timer for the Batch Manager in seconds to balance automation with user activity.

### Rounding Type
Determines rounding method for the Quoted Price field on the Job line:
- **No Rounding**
- **Up**
- **Down**
- **Nearest**

### Rounding Precision
Sets precision for rounding the Quoted Price in conjunction with Rounding Type.

### PrintVis Assisted Setup Webservice URL
URL for accessing PrintVis Assisted Setup with options for Imperial and Metric units.

- **Imperial Units:**
  - `http://rapidstart.printvis.com:7040/DynamicsNAV/WS/PRIME%203%20US/Codeunit/RapidStart`
  - `http://rapidstart.printvis.com:7040/DynamicsNAV/WS/PRIME 3 US/Codeunit/RapidStart`
- **Metric Units:**
  - `http://rapidstart.printvis.com:7040/DynamicsNAV/WS/PRIME%203/Codeunit/RapidStart`
  - `http://rapidstart.printvis.com:7040/DynamicsNAV/WS/PRIME 3/Codeunit/RapidStart`

### PrintVis Assisted Username
Username for logging into PV RapidStart.

### PrintVis Assisted Password
Password for logging into PV RapidStart.

### Frontend Merge Fields Language
Sets the language for merge fields, defaulting to English for new customers.

### CMYK Cyan
Item card for the CYAN color in CMYK color distribution.

### CMYK Magenta
Item card for the MAGENTA color in CMYK color distribution.

### CMYK Yellow
Item card for the YELLOW color in CMYK color distribution.

### CMYK Black
Item card for the BLACK color in CMYK color distribution.

### Abbr. Sheetwise
Internal abbreviation for the Sheetwise printing process, visible on the Job Ticket Report.

### Abbr. Work-and-Turn
Internal abbreviation for the Work-and-Turn printing process, visible on the Job Ticket Report.

### Abbr. Work-and-Tumble
Internal abbreviation for the Tumbling printing process, visible on the Job Ticket Report.

### Abbr. Perfecting
Internal abbreviation for the Perfecting printing process, visible on the Job Ticket Report.

---

## Job Queues

### Maintain Jobs (Req. JobQueue)
- **Description:** Not provided.

### Auto Create Jobs (Req. JobQueue)
- **Description:** Not provided.

### Transfer Costs (Req. JobQueue)
- **Description:** Not provided.

### Transfer Sales (Req. JobQueue)
- **Description:** Not provided.

---

## Cloud

### Queue Category Code
Cloud Queue Category Code relates to the "Code" field in table "Job Queue Category". The Cloud Queue Category Code can be selected from the Job Queue Category table.

### Notify on Success
Specifies whether a success log line should be created if cloud processing has been executed successfully.

### Skip Background Processing
Specifies whether the system should perform some functions as background processings, allowing the user to continue working while, for example, case folders are created with a status code move, or by the user trying to