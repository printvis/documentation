# Extra Work Codes

## Summary

Here you create and maintain the company's extra work descriptions (referred to as waste codes on the shop floor worker pages). Extra Work Codes are used in connection with the production department's job costing to indicate when additional time, materials, or other resources have been used on a given job.

## Setup

The Extra Work Codes setup can be found by searching “PrintVis Extra Work Codes”.

![Extra Work Codes.jpg](./assets/Extra Work Codes.jpg)

 Code

| **Field**                 | **Description** |
|--------------------------|-----------------|
| Code                     |                 |
| Extra Work Code          |                 |
| Text                     |                 |
| Extra Work Code Description |            |
| Item Type                | If the slack is only to be used for the registration of additional item consumption, you select which of the system item types slack is to be registered for, by a look-up in the field. <br><br>**Options:** Paper, Plates, Film, Color, Die, Repro, External Finishing.<br><br>If you leave the field empty, the system will regard the field as not filled in. |
| Can be debited           | You select this field if the registered slack is to be automatically included on the invoice draft when you structure this for production. This will typically be slack caused by the customer – e.g., last-minute changes, errors in forwarded material, or similar. <br><br>In the company's Setup (PV General Setup), you define how the slack time that can be debited is to be included in the invoice building. |
| Job Cost. Sales Price = 0| Is selected if you do not want the slack included in the job costed price for a case. However, cost price and total cost will still be calculated for the registered slack. |
| Department Code          | If you want to attach the slack to a specific department, you select the desired department by a look-up in the field. |
| Department Name          | If a department is selected in the Department Code field, the department name will appear in the field. |
| Department are required  | If selected, the user must select a department at the shop floor. |
| Comments are required    | If selected, the user must enter a comment at the shop floor. |
| Vendor Error             | Is selected if you want to register that the slack occurred due to a vendor causing extra production. |


For more information, see the Job Costing article.
