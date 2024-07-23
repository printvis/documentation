# Order Types
Order Types are used in the system as a general statistical dimension to measure a case.  Typically, the Order Type is combined with a **Product Group**.  Order Types are also used in **Responsibility Areas** setup to control the workflow of a case. 

Beyond having a statistical purpose and being used to manage case workflow, the Order Type may be used to filter the list of **Product Groups**. 

## Use of Order Types
In Order Type setup, you can decide which **Status Code** a case is initially assigned. When selecting the Order Type on a case, the **Status Code** is filled in automatically.   

The Order Type setup also gives you the option to filter the available **product groups** once the Order Type is selected on the case. On the **product group**, if an Order Type is selected that is how the product group filter is established. When filtering product groups by Order Type, the filtered list will display all **product groups** with the given order type and any product groups with no order type filled in. When looking up the **Product Group** field on the **Case**, the user will only see the Product Group(s) that have been selected. 

**Eco-Label** code can also be defaulted on a case based on Order Type setup. The user subsequently has the option to change/remove the **Eco-Label** code from the **Case**. 

In our **Responsibility Area** setup, you have the option of building different **Status Code** workflows for the different Order Types. This is useful for when you have an Order Type that must start in a specific **Status Code** and then skip the normal workflow when the **Change Status** action is selected. An example could be an Order Type for WebOrders. This could start in a Status Code of WEBORDER for review and then jump directly to Production, bypassing the prepress related workflow. 

## See Also

- <a href="../pvscasemanagement.md" target="_self">Case Management</a>
- Product Groups
- Status Code
- Responsiblity Areas
- ECO-Labels
