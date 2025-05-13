# Userfields


Userfields contain all information not covered elsewhere in the system. They organize and make relevant information available in one place, allowing your company to define a fixed structure for information accessible to all members of the organization.

Userfields can be accessed by searching PrintVis Userfield Tables.

![User Fields 1.jpg](./assets/User Fields 1.jpg)

## PrintVis General Setup

You can define which Userfields are visible on the case card and price units here.

![User Fields 2.jpg](./assets/User Fields 2.jpg)

## Userfield Groups
User Field Groups are crucial for printing userfields on the Job Ticket. Refer to the following for setup:
- [PrintVis Departments](#)
- [Setup Job Ticket Report](#)

Example for Userfield Groups:

![User Fields 3.jpg](./assets/User Fields 3.jpg)


## User Field Setup

![User Fields 4.jpg](./assets/User Fields 4.jpg)

![User Fields 5.jpg](./assets/User Fields 5.jpg)

| **Field**                   | **Description**                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Field No.                  | Field No. is a unique entry number which is assigned to the field.                                                                                                                                                                                                                                                                               |
| Field Name                 | Enter a name/explanatory text for the field.                                                                                                                                                                                                                                                                                                     |
| Group Code                 | Select which group this field belongs to.                                                                                                                                                                                                                                                                                                        |
| Datatype                   | Choose between:<br>- **Text**: For example "Is only used in Prepress"<br>- **Numbers**: For numerical values like 27<br>- **Yes/No**: Binary choice (can be empty)<br>- **Date**: For dates<br>- **Time**: For hours and minutes (e.g., 13:05)<br>- **Selection field**: Choose from a dropdown of multiple options                                 |
| Option Values              | Sums up how many option fields the Field column contains in the User Fields window.                                                                                                                                                                                                                                                             |
| Option Values only         | Should only options be allowed (no manual input).                                                                                                                                                                                                                                                                                                |
| Field Sorting              | Indicate the order in which fields must appear.                                                                                                                                                                                                                                                                                                 |
| Production Plan            | Display this field in Production Plan?                                                                                                                                                                                                                                                                                                          |
| Editable in Production Plan| Should this field be editable in Production Plan?                                                                                                                                                                                                                                                                                              |
| Must Be Filled In          | If selected, the field must always be filled in. Marked with a red question mark in User Fields.                                                                                                                                                                                                                                                 |
| Report Print               | Options:<br>- **Empty**: Field left blank<br>- **If filled-in**: Included in report if a value exists<br>- **Always**: Always included in report                                                                                                                                                                                                 |
| Report Location            | Options:<br>- **Section**: Placed in body text<br>- **Top**: Placed in header<br>- **Bottom**: Below shipment lines                                                                                                                                                                                                                              |
| Section Placement          | Choose between:<br>- Empty<br>- Left<br>- Right<br>- Center                                                                                                                                                                                                                                                                                      |
| External Suppliers         | Export the field to vendor reports (e.g., purchase quote).                                                                                                                                                                                                                                                                                       |
| External Customers         | Export the field to customer reports (e.g., quote print).                                                                                                                                                                                                                                                                                        |
| Style                      | Select the field Style from a fixed list.                                                                                                                                                                                                                                                                                                        |
| Blocked                    | Select this if the line should be blocked from further editing.                                                                                                                                                                                                                                                                                  |
| Decimals                   | Number of decimals (only active if Data Type is Numbers).                                                                                                                                                                                                                                                                                        |
| Initial Value              | Define a default value for the field. Must align with datatype setup. For Number fields, text values are not allowed.<br>**Note**: If Initial Value is defined, "Report Print" must be "Always".                                                                                                                                                |
| Minimum Value              | Only active if Data Type is Numbers.                                                                                                                                                                                                                                                                                                              |
| Maximum Value              | Only active if Data Type is Numbers.                                                                                                                                                                                                                                                                                                              |
| Length                     | Define the maximum length of the field.                                                                                                                                                                                                                                                                                                           |
| Help Text                  | Auxiliary text displayed when entering data.                                                                                                                                                                                                                                                                                                     |


## Field Options Setup

Here you enter the options for the User Fields.

![User Fields 6.jpg](./assets/User Fields 6.jpg)

![User Fields 7.jpg](./assets/User Fields 7.jpg)


## Userfields on Case Card

- **At the Top**: Order User Fields.
- **Below**: Job User Fields.

![User Fields 8.jpg](./assets/User Fields 8.jpg)
