# Status Codes
Status Codes are an integrated tool in PrintVis which directs the workflow of a **case** through the company on a general level; controlling whether, for example, you may register job costing, plan, invoice, etc.  Also, on selected points, it checks whether a case has been created correctly before it changes status.  It is important that you consider how you want to control individual cases when you set up the company's status codes.  You must also consider the level of the case (request, quote, order, production order) and what a case is allowed to do in each individual status.

When the company's status codes have been created, you must also set up a natural status flow and set up who or what group is to be responsible for a case when it reaches a given status.  You do this in the **Responsibility Areas**.

Status Codes are available to all users by default, but it is possible to limit a user to only be able to change to a select few Status Codes in the menu of the **PrintVis User** setup page.

## Use of Status Codes
The Status Codes can be set up with different types (Request, Quote, Order, and Production Order).  With this, it is easy to filter the different types in the overviews.  The different Status Codes can also be used for analysis, as in our **PrintVis Analysis** pages (PrintVis Open Quotes, PrintVis Rejected Quotes, PrintVis Case Complexity).

It is also possible to set whether material can be reserved, planned, time and material posted, invoiced, or archived at each Status Code level.  You can also set up that a previous Request or Quote must or must not be corrected when an Order line has been created on the case.  This is used in many places to secure the historical data on the case.  The order line is adjusted to the actual order, but the quote line is maintained, so you can see on what basis a quotation has been sent.

Status Codes are also where you assign when the system must create folders in **SharePoint** and when **CIM (JDF)** must be sent to an external system.

On the individual Status Codes, it is possible to set the standard "Warning" or "Stop" if there is vital information missing on the case.  This could be missing Order Type, Product Group, Seller, Coordinator, ECO-label, missing invoicing, etc.

It is possible to develop custom checks, as well.  These checks can be linked to the individual Status Codes, so the check is made when the Case gets to that specific Status Code.

## User Specific Status Codes
PrintVis provides the possibility to limit Status Codes per user.  On each PrintVis User, a set of Status Codes can be selected from the existing Status Codes.  With such setup, it is only possible for the given user to work on a limited workflow and the user cannot change to other Status Codes than the ones selected in the PrintVis User Setup.

This could be used if a user should not be able to create Orders, Quotes, etc.

## See Also

- <a href="../pvsresponsibilityareas/" target="_self">Responsibility Areas</a>
- <a href="../pvscasemanagement/" target="_self">Case Management</a>
- PrintVis User
- PrintVis Analysis pages

