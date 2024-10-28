# PrintVis WIP Setup

The PrintVis WIP Setup page sets the WIP method and the G/L Accounts to which work-in-progress will be posted.

## How it works

PrintVis has 4 WIP Methods for calculating the amounts:

- **None** - No WIP will be calculated or posted.
- **Earned Sales** - WIP is calculated based on how much of the sales have been earned at the time of calculation. This transfers all costs, revenues, and inventory value to the balance accounts, except for earned sales.
- **Completed Job - Single Cost Acct.** - WIP is calculated based on the actual labor costs at the time of calculation, and all of it goes into one account. This transfers all costs, revenue, and inventory value to the balance accounts. If any accounts are left blank, those values are ignored and remain in their original posted account.
- **Completed Job - Multiple Cost Accts.** - WIP is calculated based on the actual labor costs at the time of calculation, and labor costs can be broken down into materials, subcontracting, labor, other direct costs, and overhead. This transfers all costs, revenue, and inventory value to the balance accounts. If any accounts are left blank, those values are ignored and remain in their original posted account. If the same account is used in multiple fields, the WIP amounts will be totaled.

After selecting the **WIP Method,** the system will show dedicated columns for this method.

**WIP No. Series** contains the Series No. code used to create the Document No. during posting.

The WIP posting setup lines allow the setup to be split by **Order Types**, **Product Groups**, and **Customer Groups**.

The **WIP Earned Sales Account** and **WIP Earned Sales Applied Account** are only available when the WIP Method is **Earned Sales**. These accounts are where the earned sales WIP amounts are posted.

The **WIP Costs Account** and **WIP Costs Applied Account** are only available when the WIP Method is **Completed Job - Single Cost Acct**. These accounts are where the WIP actual costs are posted.

The **WIP Costs Account (Materials)** and **WIP Costs Applied Account (Materials)** are only available when the WIP Method is **Completed Job - Multiple Cost Accts**. These accounts are where the WIP actual cost of materials are posted.

The **WIP Costs Account (Subcontracting)** and **WIP Costs Applied Account (Subcontracting)** are only available when the WIP Method is **Completed Job - Multiple Cost Accts**. These accounts are where the WIP actual cost of subcontracting is posted.

The **WIP Costs Account (Labor)** and **WIP Costs Applied Account (Labor)** are only available when the WIP Method is **Completed Job - Multiple Cost Accts**. These accounts are where the WIP actual cost of labor is posted.

The **WIP Costs Account (Other Direct Costs)** and **WIP Costs Applied Account (Other Direct Costs)** are only available when the WIP Method is **Completed Job - Multiple Cost Accts**. These accounts are where the WIP actual cost of other direct costs are posted.

The **WIP Costs Account (Overhead)** and **WIP Costs Applied Account (Overhead)** are only available when the WIP Method is **Completed Job - Multiple Cost Accts**. These accounts are where the WIP actual cost of overhead are posted.

The **WIP Invoiced Account** and **WIP Invoiced Applied Account** are available with all the WIP Methods. These accounts are where any actual invoiced amounts are posted.

The **WIP Inventory Account** and **WIP Inventory Applied Account** are available with all the WIP Methods. These accounts are where any actual released finished goods amounts are posted.

## See Also

- <a href="../pvswipjournal/" target="_self">PrintVis WIP Journal</a>
- <a href="../pvspostedwip/" target="_self">Posted WIP Entries</a>