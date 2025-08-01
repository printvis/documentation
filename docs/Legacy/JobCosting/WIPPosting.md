# Posting of WIP (Work in Progress Cost) with PrintVis

## Summary

In PrintVis, \*\*WIP (Work in Progress)\*\* cost will consist of purchased or consumed materials or services, plus time spent on orders that have not yet been archived. WIP is manually processed through the \*\*PrintVis WIP Journal\*\* or can be setup to process on a schedule via a job queue codeunit.

### WIP Material

Material can be registered through:

- A \*\*Purchase Invoice\*\*, posted with a Case Card Order number on the purchase line.
- A \*\*Purchase Order\*\*, received and posted with a Case Card Order number on the purchase line.
- \*\*Item consumption\*\* via a manual or auto posting by using a \*\*Job Costing Journal\*\*.
- \*\*Item consumption\*\* via a consumption posting in the \*\*Electronic Job Ticket\*\*.
- \*\*Item consumption\*\* via a posting from the \*\*PV Material Delivery Journal\*\* (page 6010385) from Logistics.

### WIP Subcontracted Work

Subcontracted work can be registered through:

- A \*\*Purchase Invoice\*\*, line type \*\*G/L Account\*\*, field \*\*Subcontracted\*\* set to \*Yes\*, posted with a Case Card Order number on the purchase line.
- A \*\*Purchase Invoice\*\*, line type \*\*Item\*\*, Item Card field \*\*Subcontracted\*\* set to \*Yes\* (which flows to the purchase line), posted with a Case Card Order number on the purchase line.
- \*\*Item consumption\*\* in a \*\*PV Consumption Journal\*\*, where Item Card field \*\*Subcontracted\*\* is set to \*Yes\*.
- A \*\*Posted Purchase Journal\*\* line, field \*\*Subcontracted\*\* set to \*Yes\*, posted with a Case Card Order number on the line.

### WIP Production Hours

Production hours can be registered through:

- \*\*Consumption of hours\*\* in a Job Costing Journal or through \*\*Start/Stop\*\* in the Electronic Job Ticket.
- \*\*Consumption manually posted\*\* in a Job Costing Journal from paper sheets.

> The page \*\*Estimation/Job Costing\*\* (page 6010509) on the Case Card will display these hours.


### WIP Setup

The \*\*PrintVis WIP Setup\*\* page is how you set the WIP method and the \*\*G/L accounts\*\* where WIP posting will occur.

![Posting of WIP (Work in Progress Cost) with PrintVis 1.jpg](./assets/Posting of WIP (Work in Progress Cost) with PrintVis 1.jpg)

#### WIP Methods

PrintVis has 4 WIP Methods for calculating the amount.

| Method                              | Description |

|-------------------------------------|-------------|

| None                                | No WIP will be calculated or posted. |

| Earned Sales                        | WIP is calculated based on how much in sales has been earned at the time of calculating. Essentially, this moves all costs, income, and inventory value into the balance accounts, except for the earned sales based on the calculation below:<br><br>- Actual job costing / estimated job costing = Percentage completed<br>- Quoted price + extra sales amount registered (extra work codes where can be debited = Yes) = Sales Amount Total<br>- WIP Amount = Sales Amount Total \* Percentage completed |

| Completed Job - Single Cost Acct.   | WIP is calculated based on actual job costing at the time of calculation and total goes into a single account. Essentially, this moves all costs, income, and inventory value into the balance accounts. If any accounts are left blank, these values will be ignored and remain in their original posted account. |

| Completed Job - Multiple Cost Accts.| WIP is calculated based on actual job costing at the time of calculation and the job costing can be separated into materials, subcontracting, labor, other direct cost, and overhead. Essentially, this moves all costs, income, and inventory value into the balance accounts. If any accounts are left blank, these values will be ignored and remain in their original posted account. If the same account is used in multiple fields, the WIP amounts will be totaled. |


#### WIP No. Series

A Business Central number series that is used as the document number when posting WIP.

#### Posting Setup

The WIP posting setup lines allow for the setting of G/L accounts.


| Field | Description |

|-------|-------------|

| Order Type | Ability to set different posting accounts based on the order type on the case. |

| Product Group | Ability to set different posting accounts based on the product group on the case. |

| Customer Group | Ability to set different posting accounts based on the customer group on the case. |

| WIP Earned Sales Account / WIP Earned Sales Applied Account | Available only when the WIP Method is \*\*Earned Sales\*\*. These accounts are where the earned sales WIP amounts are posted.<br>- The WIP Earned Sales Account is typically the balance account<br>- The WIP Earned Sales Applied Account is typically the income or P\&L account |

| WIP Costs Account / WIP Costs Applied Account | Available only when the WIP Method is \*\*Completed Job - Single Cost Acct.\*\* These accounts are where the WIP actual costs are posted.<br>- The WIP Costs Account is typically the balance sheet account<br>- The WIP Costs Applied Account is typically the income or P\&L account |

| WIP Costs Account (Materials) / WIP Costs Applied Account (Materials) | Available only when the WIP Method is \*\*Completed Job - Multiple Cost Acct.\*\* These accounts are where the WIP actual cost of materials are posted.<br>- The WIP Costs Account is typically the balance sheet account<br>- The WIP Costs Applied Account is typically the income or P\&L account |

| WIP Costs Account (Subcontracting) / WIP Costs Applied Account (Subcontracting) | Available only when the WIP Method is \*\*Completed Job - Multiple Cost Acct.\*\* These accounts are where the WIP actual cost of subcontracting are posted.<br>- The WIP Costs Account is typically the balance sheet account<br>- The WIP Costs Applied Account is typically the income or P\&L account |

| WIP Costs Account (Labor) / WIP Costs Applied Account (Labor) | Available only when the WIP Method is \*\*Completed Job - Multiple Cost Acct.\*\* These accounts are where the WIP actual cost of labor are posted.<br>- The WIP Costs Account is typically the balance sheet account<br>- The WIP Costs Applied Account is typically the income or P\&L account |

| WIP Costs Account (Other Direct Costs) / WIP Costs Applied Account (Other Direct Costs) | Available only when the WIP Method is \*\*Completed Job - Multiple Cost Acct.\*\* These accounts are where the WIP actual cost of other direct costs are posted.<br>- The WIP Costs Account is typically the balance sheet account<br>- The WIP Costs Applied Account is typically the income or P\&L account |

| WIP Costs Account (Overhead) / WIP Costs Applied Account (Overhead) | Available only when the WIP Method is \*\*Completed Job - Multiple Cost Acct.\*\* These accounts are where the WIP actual cost of overhead are posted.<br>- The WIP Costs Account is typically the balance sheet account<br>- The WIP Costs Applied Account is typically the income or P\&L account |

| WIP Invoiced Account / WIP Invoiced Applied Account | Available with \*\*all WIP Methods\*\*. These accounts are where any actual invoiced amounts are posted.<br>- The WIP Invoiced Account is typically the balance sheet account<br>- The WIP Invoiced Applied Account is typically the income or P\&L account |

| WIP Inventory Account / WIP Inventory Applied Account | Available with \*\*all WIP Methods\*\*. These accounts are where any actual released finished goods amounts are posted.<br>- The WIP Inventory Account is typically the balance sheet account<br>- The WIP Inventory Applied Account is typically the income or P\&L account |


### WIP Journal Usage

The PrintVis WIP Journal is where the WIP amount is calculated, a WIP report can be generated, and WIP is posted into the setup G/L accounts.

![Posting of WIP (Work in Progress Cost) with PrintVis 2.jpg](./assets/Posting of WIP (Work in Progress Cost) with PrintVis 2.jpg)


| Menu Action           | Description |

|------------------------|-------------|

| Build WIP Journal      | Selecting this action will prompt the user for a posting date and then build the WIP journal based on the WIP setup. |

| Show/Hide no WIP       | When building the WIP Journal, all active order cases that have not been archived are included in the build process. Archived cases that have previous (unreversed) WIP postings are also included in the build process. By default, after calculating, the WIP Journal hides any of the cases that have a calculated WIP amount = 0. The Show/Hide no WIP action will display/hide these 0 WIP amount entries. |

| Open Case              | Open the case card for the highlighted WIP journal entry. |

| WIP Report             | Generates a printable report of WIP journal entries. |

| Post WIP to G/L        | This action posts all entries in the WIP journal to the setup G/L accounts. Every time the WIP journal is posted, all previous WIP G/L entries for that case/account are reversed and new entries are created. |



| Field                         | Description |

|-------------------------------|-------------|

| WIP Account                   | The WIP account setup on the WIP setup page. |

| WIP Applied Account           | The WIP Applied account corresponding with the WIP account setup on the WIP setup page. |

| Date                          | The posting date used when building the WIP journal. If the posting date is left blank during the build, the user work date is used. |

| Description                   | A combination of the case order number and WIP account description. |

| WIP Amount                    | The amount that will be posted to the WIP / WIP applied accounts. This field is editable should the user want to adjust the amount posted. |

| Estimated Total Cost          | A read-only field that displays the estimated total cost of the case. This value is only displayed on the cost and earned sales account lines. |

| Quoted Price                  | A read-only field that displays the quoted price of the case. This value is only displayed on the invoice account lines. |

| Extra Sales Amount Registered | A read-only field that displays the extra sales amount registered on a case (extra work codes with can be debited = Yes). This value is only displayed on the invoice account lines. |

| Sales Amount Total            | A read-only field that is displayed when the WIP Method is Earned Sales. This field displays the quoted price + extra sales amount registered values used in the earned sales calculation. |

| Pct Completed                 | The calculated percentage completed of a case based on the actual job costing / estimated total costs of a case. This field is editable should the user want to adjust the percentage completed which will recalculate the WIP amount. This field is only available when the WIP Method is Earned Sales. |

| WIP Posted                    | A read-only field that displays the amount of WIP that has already been posted to the General Ledger for this case/account combination. This is the entry that will be reversed when the new journal is posted. |


### WIP Postings on a Case

From the case card, it is possible to see the WIP postings for that specific case. In the menu, it is located in Actions -> Case Info -> Posted WIP. This will display all the active and previous WIP postings for that case.

![Posting of WIP (Work in Progress Cost) with PrintVis 3.jpg](./assets/Posting of WIP (Work in Progress Cost) with PrintVis 3.jpg)

### Job Queue Codeunit

It is possible to schedule the WIP build and posting using a job queue entry. The Codeunit to setup this type of posting is 6010120 PVS WIP Management. When this job queue entry runs, it will perform the Build WIP Journal process with the posting date set to the date the job queue runs and then immediately performs the Post WIP to G/L process. 

![Posting of WIP (Work in Progress Cost) with PrintVis 4.jpg](./assets/Posting of WIP (Work in Progress Cost) with PrintVis 4.jpg)
