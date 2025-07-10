# PrintVis Onboarding – Folder Management

This documentation is a supporting manual on how to use the PrintVis
Onboarding Setup. It describes the required setup steps for this module.

# PrintVis Folder Management

A PrintVis folder provides the ability to store any kind of file for
PrintVis cases. The files can be stored on Microsoft OneDrive or
SharePoint storage and for every case it is possible to create a
structure of folders there.

All users who can edit cases have access to the folders created and the
files stored - no special browsing is required and all files can be
found in the specific structure.

This setup provides the following steps:

-   Sign-in and test the connection to your OneDrive / SharePoint.

-   Select the root and sub folder to store your files

Please click on the Role Center tile “Ready for setup.” If the PrintVis
Case Management Module has been completed, the Folder Management setup
is available.

![PrintVis Folder Management](./assets/0500-image1.png)

Click on Folder Management and the “Welcome” and setup screen will be
displayed. Please read the instructions and hit the “Next” button when
you are ready to start.

![PrintVis Folder Management](./assets/0500-image2.png)

## Sign into OneDrive / SharePoint and test the connection.

Click on “Sign-in” and a popup opens to enter your credentials for
SharePoint access.

### No login Screen appears, only a counter?

Your browser’s popup blocker (this is the default for all new URLs!)
must be disabled for your Business Central URL.

Click on the icon (see below highlighted with a red frame) on the
browser address field and choose “Allow pop-ups and redirection for
<https://businesscentral.dynamics.com/>...”

Depending on the browser, the message might differ slightly. Please
still allow popups.

![PrintVis Folder Management](./assets/0500-image3.png)

If the following message appears, click “OK” and Sign-in again.

![PrintVis Folder Management](./assets/0500-image4.png)

## Sign-in

With your Business Central trial, you also receive a trial for other
Microsoft products such as SharePoint. Please use the same credentials
that you provided for your Business Central/PrintVis login.

Select you account type (typically Work or school account):

![PrintVis Folder Management](./assets/0500-image5.png)

Enter your user:

![PrintVis Folder Management](./assets/0500-image6.png)

Enter your password:

![PrintVis Folder Management](./assets/0500-image7.png)

Enable field “Accept for your organization” (or similar) and click the
“Accept” button.

![PrintVis Folder Management](./assets/0500-image8.png)

Now you are logged in successfully.

![PrintVis Folder Management](./assets/0500-image9.png)

To verify the connection, click on “Test connection.”

![PrintVis Folder Management](./assets/0500-image10.png)

Hit the button “Next” to proceed.

## Select Where to Store New Files

Please note: In the next steps please follow the example given. It is
necessary to walk through the steps carefully because the token and
structure on SharePoint cannot be preset automatically.

Click the 3 dots in each field to select or create a folder on
SharePoint.

![PrintVis Folder Management](./assets/0500-image11.png)

On “Documents Site” for example choose &lt;Root site&gt;. If you choose
anything else, the next lookups may be different!

![PrintVis Folder Management](./assets/0500-image12.png)

On “Documents Library” for example, choose “Sharepoint Library.” If you
choose anything else, the next lookups may be different!

![PrintVis Folder Management](./assets/0500-image13.png)

In the field “Base Folder,” you could use the root (first line) or
create a new sub folder.

![PrintVis Folder Management](./assets/0500-image14.png)

In this example a new sub folder “PrintVis Files” was created and
selected.

![PrintVis Folder Management](./assets/0500-image15.png)

Click “Ok to see the result:

![PrintVis Folder Management](./assets/0500-image16.png)

Click “Next” to proceed.

In this step you are creating a folder group, where PrintVis will create
sub-folders for each case.

![PrintVis Folder Management](./assets/0500-image17.png)

Until we have gained more experience, do not create additional settings;
simply select the root (first) line and click “OK.”

![PrintVis Folder Management](./assets/0500-image18.png)

Result:

![PrintVis Folder Management](./assets/0500-image19.png)

Click “Next.”

In this screen (enlarge the page on the upper right-hand side) you can
set up in which phase of a case a folder should be created.

You can follow this example which is “best practice” in the beginning.
This setup can be changed later.

-   Keep the settings as suggested.

-   In the field “Status Code 3,” choose the status code for your
    “Quote” status (in case you have renamed it).

![PrintVis Folder Management](./assets/0500-image20.png)

With this setup, your folder will be created when a case is in a quote
phase, but also in an order phase if not already created before. You can
access an order directly for a new case if you have an agreement with
your customer that does not require a quote.

![PrintVis Folder Management](./assets/0500-image21.png)

Click Next to proceed.

In this setup you could set sub-folders with a specific logic by using
variables. A variable is represented by the %-sign and a variable
number, e.g., %9, which will read the job name of the current case.

![PrintVis Folder Management](./assets/0500-image22.png)

As an example, you will see the setup for 2 sub folders created for each
case:

-   “../2023/1234/Customer/”

    -   This could be a case folder where all customer provided or
        related files are stored.

-   ../2023/1234/Internal/”

    -   This could be a case folder where all internal files are stored.

You can keep the example which is good enough for early usage - and
later extend the setup.

Examples for the variables are:

-   %1=Customer No

-   %2=Customer Letter (the first letter of the customer’s name)

-   %3=Customer Name

-   %6=Order ID

-   %8=Year

-   %9=Jobname

Click “Next” to get to the final page.

After hitting “Finish,” the page will close, the setup is completed and
marked as “Ready.”

![PrintVis Folder Management](./assets/0500-image23.png)
