# Using Power Automate with PrintVis folders 

**Note: For cloud customers with Microsoft 365 account**

**Customer Request**

Have you ever had a customer ask if a template file can be automatically
added to a PrintVis folder when the folder is created?

For example: We have a certification checklist that is needed for all of
John Haddock, Inc. jobs. Is it possible to have this checklist template
added to a Certification folder when a case becomes an order?

**Accomplishing the Request**

While there is no specific way within PrintVis or Business Central to
accomplish this request, with the use of Power Automate you can
accomplish this for your customer.

First, we are going to create a new Folder Group for John Haddock:

![Power Automate](./assets/PA1.png)

Advanced Usage Options:

![Power Automate](./assets/PA2.png)

Folders:

![Power Automate](./assets/PA3.png)

Power Automate can be found by clicking the "waffle" dots in the upper
left corner and selecting Power Automate.

![Power Automate](./assets/PA4.png)

Select My flows:

![Power Automate](./assets/PA5.png)

Select New flow, then Automated cloud flow:

![Power Automate](./assets/PA6.png)

Search “When a file is created (properties)” in the Choose your flow’s
trigger field and select "When a file is created (properties only)
SharePoint," then click the "Create" button.

![Power Automate](./assets/PA7.png)

In the Site Address field, select your SharePoint address. In the
Library Name field, select the Documents Drive from your Cloud Storage
Setup page. And in the Folder field, select the Base Folder from the
Cloud Storage Setup page.

![Power Automate](./assets/PA8.png)

![Power Automate](./assets/PA9.png)

Select the New step button and chose the Condition Control:

![Power Automate](./assets/PA10.png)

In the Condition filter, choose "IsFolder" dynamic content is equal to
true, and Add Row with Name dynamic content is equal to “Certification”
or the name of the folder where you want the file located.

![Power Automate](./assets/PA11.png)

In the "If Yes" section, click Add Action and select Copy file:

![Power Automate](./assets/PA12.png)

In the Copy file box, fill in the Current Site Address as the SharePoint
location from where to copy the file and the File to Copy as the exact
location where the file resides. In the Destination Site Address, enter
the Document Site from the Cloud Storage Setup page, and in Destination
Folder enter the Full Path dynamic content. In the "If another file" is
already there, select Replace, Copy with a new name, or Fail this
action.

![Power Automate](./assets/PA13.png)

Click Save.

![Power Automate](./assets/PA14.png)

Once this is completed, whenever the Certification folder is created,
the Checklist.xlsx file will automatically be added to that case folder:

![Power Automate](./assets/PA15.png)

![Power Automate](./assets/PA16.png)
