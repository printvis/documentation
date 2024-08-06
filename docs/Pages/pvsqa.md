# Quality Assurance
PrintVis Quality Assurance provides a customizable checklist for production quality control.  It is possible to log all important information on the Case at user level.  It can be set for General, Make Ready, or Production, where everything is checked at the start of operation, and/or have ongoing production registrations.  The fields can be Checkmarks, Comments, optional, or mandatory.  It is possible to have different QA Checklists based on various parameters, Customer groups, Customers, Order types, Product Groups, or ECO-label Codes.

The operator can access this QA Checklist from the Shop Floor – Electronic Ticket.

Setup for the QA Checklist can be found by searching **QA Setup**.  The list can be set up by:
- A basic set of questions
- Questions especially for a specific order type
- Questions especially for a specific customer
- And more
If an order is for the given order type AND customer, the checklist will contain all questions for all 3 usage groups.

## Using Quality Assurance
There are 2 levels in Quality Assurance – Usage and Lines:

Usage - Various parameters are set up here: Customer groups, Customers, Order types, Product Groups, or ECO-label Codes.

Lines - The quality questions (Lines) presented to the operator is the summary of those parameters.  The checklist can be presented on the Case Card - Job and in the Shop Floor Role Center.

Lines can be linked to departments or Cost Centers (generic or very specific).

If a line is Mandatory – you have 4 options
- None – The operator can fill out in the field
- Checkmark only – The operator must check “Is OK”
- Comment only – The operator must fill out the field “Comments”
- Both – The operator must check “Is OK” and fill out the field “Comments”
Furthermore, it is possible to associate the lines with 3 options (used with the mandatory field):
- General - The operator must complete the QA line before a job can be marked "Job Complete."  If the operator presses job complete before completing all General, Make Ready, and Production mandatory lines, a message is given, and it will not complete the job.
- Production - The operator must complete the QA line before production time can be started.  If the operator presses a production time UOM before completing all Make Ready and Production mandatory lines, a message is given, and it will not start recording production time.
- Make Ready - The operator must complete the QA line before “make ready time” can be started.  If the operator presses a make ready time UOM before completing all Make Ready mandatory lines, a message is given, and it will not start recording production time.
Lines can also have a hyperlink, so the operator can access files or web pages.

Result

The lines which are set to “OK” by a user will store the User ID and date, showing when and by whom the lines were set to “OK.”

## See Also

- <a href="../pvscasemanagement/" target="_self">Case Management</a>
- Cost Center
- PrintVis UOM

