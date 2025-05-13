# Publications and Editions


## Summary

Publications is a set of fields, screens, and functions designed to handle periodicals, newspapers, or other printing items issued regularly in the same format. A publication may be connected to an issued calendar and may have a set of sections tied to different schedules or technical attributes.

Working with publications involves handling many orders for the same product but differentiating them by issue date.

## Example

To work with publications, the following fields must be shown on the case card job lines:

- Publication Code
- Publication Description
- Edition
- Edition ID

This setup is done in the main PrintVis Setup menu on the **Estimating** tab in the field: `Show Publication Fields`.

## Publication List

The basic setup is a list of publications to be handled in the database. Each publication is connected to a customer. You may choose to enter one publication for a product type or several for different days of the product, as shown in this example.

The remaining setup involves defining which sections each publication consists of and which editions it comes in.

## Sections

Sections apply to products that may be divided into logical parts. For instance, this could be the sports section of a newspaper or the color section of a magazine.

### Example: 

The configuration levels of publications and sections may be defined as fits best for the customer. For example, LEN (Lisbon Evening News) could be set as one publication with different publications manually set for each day of the week. Alternatively, TN (Tokyo News) could have each day of the week as a separate publication, each with its own configuration of sections.

 Field List

| Field           | Description                                                                                                            |
|-----------------|------------------------------------------------------------------------------------------------------------------------|
| Publication Code| The publication code for this edition. Not visible in normal configuration but filled out via the Publication list. |
| Section Code    | A unique code for a given type of section for this publication. The same section may be configured for several publications. |
| Description     | Text description of the section code.                                                                                |
| Used            | The publication code for this edition. Not visible in normal configuration but filled out via the Publication list. |

## Editions

Editions of publications refer to the dates of issue for a given publication. For example, a publication of Tokyo News on Mondays will have editions for Jan 3rd, 2011, Jan 10th, 2011, and so on. Editions may be daily, weekly, monthly, or have no specific periodical association.

**Example:** The planned editions for Lisbon Evening News, which is a daily newspaper.

 Field List

| Field            | Description                                                                                                      |
|------------------|------------------------------------------------------------------------------------------------------------------|
| Publication Code | The publication code for this edition. Not visible in normal configuration but filled out via the Publication list. |
| Edition ID       | A unique identifier for the edition numbers of the publication. The number is numerical from 1 and is set by the system. |
| Edition Date     | Set by the user, representing the date when the edition should be available to end users or in shops.            |
| Edition No.      | An identifier open for setting by the user. This code may be alphanumerically set and is a Code 20 field.         |
| Week Day         | System-set weekday information taken from the date input provided by the user.                                   |
| Week             | System-set week information taken from the date input provided by the user.                                      |
| Jobs             | Number of active jobs on case cards assigned with this particular Publication Code and Edition ID.               |

## Using the Publication in an Installation

By defining a newspaper as one or more publications (e.g., one daily publication or one publication per day of the week), you must provide the system with information on publication editions (the calendar) and sections (contents). 

Whereas one publication has specific editions, sections within each edition may vary. Therefore, sections for each edition must be defined. At least one Case Card per edition must be created. This is typically done by creating one basic template or base order and then using the periodical copying function to create many copies of the same order. Each order must then be manually attached to the correct edition of the publication.

Please note that there may be a difference between Edition Date and the required delivery date, as the delivery date may be before the edition date when the publication must be available in shops.

Each Case Card is reviewed for correct sections.

### Using Sections on Job Card

On the Job Card, one sheet is created per section, with the Section Code attached on each sheet. Given the number of pages in the section and the printing machine configuration, there may be residual sheets.

The system will track this code on relevant forms and tables for production:

- PrintVis Job Item
- PrintVis Sheet
- PrintVis Planning Unit
- PrintVis Job Costing

This means that the section is a part of the job costing breakdown and is available in production planning and Web Vision production plans.

**Publication and Section** are available on planning units and when recording the consumption of time and materials, and are clearly visible on Case Card statistics.
