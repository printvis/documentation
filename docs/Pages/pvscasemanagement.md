# Using case management

PrintVis Case Management offers insights and serves as the central hub for daily administrative tasks for all job-related personnel. It provides comprehensive visibility into cases, offering detailed data on deadlines, delivery dates, customer details, and order history. Each case acts as a comprehensive repository, encapsulating all pertinent information from quotation to invoicing. Through Case Management, you wield control over and track the progression of jobs across your organization, with clear visibility into pending quotes, confirmed orders, and ongoing tasks.

## Creating a case

Select **New** to create a new case.

Complete the **Sell-To** information, Order Type, and Product Group to get started. You are now ready to fill in the job details in the **Jobs** section. 

The initial entry will have job number **1** and version number **1**. If your case is in a **Request** status, the job line will have a type of Request. If your case is in a **Quote** status, the job line will have a type of Quote. If your case is in an **Order** status, the job line will have a type of Order or Production Order based on the status code setup. In PrintVis each job number represents a unique product being produced. You can create a new Job line with a new job number by selecting the **New Job** button. It is possible for multiple jobs to be **Active** on a single case each having their own estimate, production schedule, and shipments. You can also have different versions of each job. A version could be different quantities the customer wants quoted, different page counts, etc. Also, when a case is moved from a quote status to an order status, the quote lines will remain and an order line will be created with the same job number but an incremented version number. This happens automatically when there is only one quote job/version but will need to be done manually by selecting the **Create Order** button when more than one quote line exists. The selected line is the quote line that will be converted to an order. Also, it is important to note that only a single version of a job can be active at one time. 

The **Jobs** section is where you will define the ordered quantity, page count, format size, colors, requested shipment date, external description, and other general job information. If you are utilizing templates, it is likely that a quoted price will already be calculated by simply entering this basic information. You can always override the calculated quoted price by changing the contribution margin/net profit fields or by manually setting the quoted price.

The **Job Items** section is where you will define the components of the job. The job items section consists of *sheets* and *job items*. A *sheet* should be considered based on a single substrate run through a press. A *job item* is what is placed on a sheet. A job item is automatically created when a sheet is created but it is possible to add additional job items to a sheet. To create a new sheet select the **Create Sheet** button. To add an additional job item to a sheet, highlight the sheet in the list and select the **Extra Job Item** button.

In the **Job Items** section is where you will define the component type, description, number of pages, colors front/back, which substrate will be used for the component, and the *list of units* which is the press that will print the component with any additional units required for printing such as platemakers, etc.

The **Case Description** section allows you to create general or department specific notes that can be accessed on the case and on the shop floor. 

The **Invoicing** section allows you to change the *Bill-to* customer for this case.

The **Info** section displays some statistics such as request completed date/time, estimate completed date/time, date/time the case was converted to an order, the date/time production was completed, and the date the case was archived.

## See also

- Copying
- Job Costing
- Material Requirements
- Purchase Guide
- User Fields
- Invoicing Guide
- Folders
- Reports
- Pricing Details
- Estimating
- Scheduling
- Shipments
- Milestones
- Product Versions
- Quality Assurance
- Commission
- <a href="../pvsordertype/" target="_self">Order Types</a>
