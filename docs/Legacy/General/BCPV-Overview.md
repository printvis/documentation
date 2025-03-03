# Overview - Touchpoints between Business Central and PrintVis

## Summary
PrintVis is integrated with Business Central to provide a vertical-specific solution for the print industry. The seamless integration between the two products results in several touchpoints where the systems interact. This article provides an overview of these touchpoints and explains how PrintVis handles various aspects of the system differently than Business Central.

---

## Touchpoints Between Business Central and PrintVis
The following topics outline key integration points between Business Central and PrintVis. Each touchpoint has a dedicated article that can be found in the same folder as this document. You can also search by using "Touchpoint <topic>."

- CRM Functionality
- Item Card
- Purchasing
- Reservations
- Item Consumption with PrintVis Shopfloor
- Material Movement / Pick
- Shipments
- Finished Goods Items
- Invoice
- Work in Progress (WIP)
- G/L Posting Setup

---

## PrintVis Functionality
The functionality described below is unique to PrintVis and does not involve Business Central’s Manufacturing module. No Business Central Manufacturing functionality is required, meaning that a **Premium license** is **not** needed.

### Key Functionalities in PrintVis:

- **Estimation and Calculations**
  - Replaces the routing and BOMs used in Business Central Manufacturing.

- **Quote Creation**
  - PrintVis has its own Quote system that replaces Sales Orders. It uses **Cases** to manage jobs from request to invoicing.

- **Order Creation**
  - PrintVis manages orders using **Cases**, which contain the entire job information from request to invoicing.

- **PrintVis Userfield**
  - Allows customer-specific information to be set up and used during quoting, ordering, production, and shipping. Reduces the need for customizations if standard PrintVis fields do not meet the customer's requirements.

- **Planning / Scheduling**
  - Job Scheduling and Production Planning are linked to PrintVis Cases.
  - The **Planning Board** provides a visual representation of the schedule, replacing Business Central’s **Resource Scheduling** and **Schedule Board**.

- **Shop Floor**
  - PrintVis replaces Business Central's **shop-floor user interface**.
  - Job-specific information is displayed in three ways:
    - **Job Ticket:** A customizable job ticket with details specific to each job.
    - **Production Tile:** Displays essential job information when selecting a job on the shop floor.
    - **Tooltips:** Displays job-specific details on the right side of the screen when a user is clocked into a job.

- **Shipments**
  - Sales Shipments are optional in PrintVis.
  - PrintVis provides a separate **Shipment Card**, allowing shipments to be handled without Business Central’s shipment functionality.

---

## Why Is This Important?
Incorrect setup and customer confusion often result from missing communication and a lack of understanding of PrintVis’ standard options.

Before performing any setup that seems cumbersome or incorrect, or considering customization, **contact us**. We are happy to share our expertise and best practices.

---

   PrintVis Contact Information:
- **Email:** support@printvis.com  
- **Website:** [PrintVis.com](https://printvis.com/)  
- **Phone:** +45 8625 0303 (EU) | +1 470-681-7890 (US)  

For any further questions, please reach out to our team!




