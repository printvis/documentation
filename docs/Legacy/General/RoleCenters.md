# PrintVis Role Centers - Profiles

## Summary

In Business Central, all users are assigned profiles that reflect their business roles, departments, or other categorizations. Profiles allow administrators to manage what different user types can see and do in the user interface, enabling efficient task performance.

A **Role Center** gives users quick access to information pertinent to their daily work, displaying relevant data and facilitating navigation to necessary pages for tasks.

PrintVis extends this functionality by providing specific Role Centers for various user roles in a printing company.

 Available PrintVis Profiles

The screenshot below shows the list of available PrintVis profiles:

![PrintVis Role Centers - Profiles 1.jpg](./assets/PrintVis Role Centers - Profiles 1.jpg)

In this document, the term "Profile" encompasses both roles and profiles, referring to the same concept.

## Usage

PrintVis profiles aim to provide access to specific print production-related areas of PrintVis and Business Central. If a company wishes to create custom profiles, it is recommended to copy an existing profile with the required access and modify it, keeping the original PrintVis profiles intact.

![PrintVis Role Centers - Profiles 2.jpg](./assets/PrintVis Role Centers - Profiles 2.jpg)

Profiles are assigned to users under "User Settings" (field "Role"). If no profile is assigned, the default profile is used. Profiles can be copied and saved under a custom name on the Profiles page.

![PrintVis Role Centers - Profiles 3.jpg](./assets/PrintVis Role Centers - Profiles 3.jpg)

#### Common PrintVis Profiles

- **PrintVis Admin Profile**  
  For setting up and administrating PrintVis. Access all setup areas, including RapidStart/Assisted setup.

- **PrintVis Coordinator Profile**  
  For customer service and scheduling. Manages typical requests and order management tasks, including purchase and inventory.

- **PrintVis Shop Floor Worker Profile**  
  For production staff, providing access to production information and shop floor data collection.

## PrintVis role profiles

This table describes the PrintVis profiles, also known as Role Center roles, what they are designed for, who should use them, and whether the role includes UI simplifications.

### Role profile overview

| Profile | Designed for | Typical users |
| --- | --- | --- |
| PrintVis Admin | System-wide PrintVis administration, setup, and monitoring. | ERP admins, solution owners, super users. |
| PrintVis Accounting | Finance and bookkeeping activities, approvals, and financial reporting. | Bookkeepers, AP/AR accountants, finance operations. |
| PrintVis Coordinator | Coordinating cases, order flow, and complaint follow-up. | Production coordinators, operations coordinators, customer service coordinators. |
| PrintVis Estimator | Estimation and quote-related activities in case flow. | Estimators, prepress and quote specialists. |
| PrintVis Customer Sales Services* | Sales and customer-service-focused case handling with reduced complexity. | CSR users, inside sales, order desk. |
| PrintVis Planner | Capacity and production planning, planning board, and production plan execution. | Production planners, schedulers. |
| PrintVis Purchaser | Procurement-focused workbench for vendor and purchasing processes. | Buyers, purchasing agents. |
| PrintVis Sales & Relationship Manager | CRM and pipeline-oriented sales relationship management. | Sales managers, key account managers. |
| PrintVis Warehouse Worker | Shipment and warehouse execution tasks. | Warehouse operators, shipping clerks, dispatch users. |
| PrintVis Legacy ShopFloor Manager | Legacy shop floor supervision and monitoring. | Shop floor supervisors using legacy UI. |
| PrintVis Legacy ShopFloor Worker | Legacy operator role for registration and shop floor execution. | Shop floor operators using legacy UI. |
| PrintVis ShopFloor Worker | New ShopFloor UI role for clocking, activity, and worksheet execution. | Shop floor operators on the current ShopFloor UI. |
| PrintVis Onboarding | Guided initial setup and onboarding workflow. | New implementations, onboarding admins, rollout teams. |
<br>

***PrintVis Customer Sales Services**

This profile is designed to simplify the user experience for sales and customer service personnel. The Case Card has been streamlined by hiding fields, actions, and functionality that are primarily intended for production, planning, estimation, or other advanced PrintVis processes. By removing features that these users typically do not need, the interface becomes cleaner, easier to navigate, and more focused on creating and managing customer orders. Similar simplifications are also applied to the Case List, job views, planning pages, and shipment pages, helping users concentrate on their daily sales and customer service tasks.

### PrintVis Admin Profile

This profile is designed for users who build and maintain the PrintVis setup. It allows access to all setup areas and the initiation and control of the initial PrintVis setup.

To select the PrintVis Admin role/profile:
1. Click the gear icon in the upper right-hand corner of the screen.

![PrintVis Role Centers - Profiles 4.jpg](./assets/PrintVis Role Centers - Profiles 4.jpg)

2. Choose "PrintVis Admin" from the role options.

![PrintVis Role Centers - Profiles 5.jpg](./assets/PrintVis Role Centers - Profiles 5.jpg)

3. Click "OK" to access the Admin Role Center.

![PrintVis Role Centers - Profiles 6.jpg](./assets/PrintVis Role Centers - Profiles 6.jpg)

#### Main Menu

![PrintVis Role Centers - Profiles 7.jpg](./assets/PrintVis Role Centers - Profiles 7.jpg)

Access major PrintVis and Business Central areas to create case examples, items, purchase orders, and other tests for setup changes.

#### Actions

![PrintVis Role Centers - Profiles 8.jpg](./assets/PrintVis Role Centers - Profiles 8.jpg)

In this area, all relevant PrintVis setup options are accessible, grouped by specific topics:

| Menu Topic          | Description                                                                                       |
|---------------------|---------------------------------------------------------------------------------------------------|
| **PrintVis General** | Essential settings not part of another group, including: PrintVis Assisted Setup, General Setup, User Setup, Cost Center Setup |
| **Estimation**       | Estimation-related setup, including: Order Types/Product Groups, Calculation Units, Component Types, Additional Rates |
| **Scheduling/Planning** | Planning-related setup, including: Capacity Units and Groups, Planning Units, Opening Hours and Profiles |
| **Job Costing**      | Job costing-related setup, including: Units of Measure, Job Costing Journals, Shop Floor Setup |
| **Invoicing**        | Job invoicing-related setup, including: G/L Posting Setup, Invoice Templates, and BC General/Inventory Posting Setup |
| **Case Management**  | Setup related to status flow, including: Status Code Setup, Responsibility Areas Setup, Planning Unit Setup |
| **Materials**        | Item-related settings, including: Item Qualities, Item Types Codes, BC Item Templates |
| **Tools / Dies**     | Tool and die-related settings and the Tools/Dies themselves |
| **Web2PrintVis**     | Back-end and front-end related settings |
| **Customer Setup**   | Customer-related settings |
| **Reports/Documents** | Storage, Report, and PV Document setup-related settings |
| **PrintVis System**  | System settings not relevant for the above menus |

#### Insights

![PrintVis Role Centers - Profiles 9.jpg](./assets/PrintVis Role Centers - Profiles 9.jpg)

Provides direct access to related and important setup areas/tables, with a tile showing the number of entries and opening the table with one click.

#### PrintVis News

Direct links to PrintVis documentation, such as release information and documentation on the PrintVis Support Portal.

#### PrintVis Information

Displays more PrintVis-related information, including the version of the currently installed PrintVis base app.