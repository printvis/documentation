# Cloud Migration from OnPrem to Cloud

To migrate PrintVis to BC sas we recommend that you use Microsoft's Guides for upgrade / Cloud Migration, we have added some links below to where you can find the Guides.

[Upgrading to Dynamics 365 Business Central](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrading-to-business-central)

 
Generally it is possible to go directly from BC / PVS 16 to BC 25 without any middle step.
 

 If the Current PrintVis Version is below then PVS 19.2 you will need to upgrade to 19.2 to take advantages of upgrade Code regarding "Report Selections". this is the only setup table that needs to be changed, and it is possible to skip 19.2 and the change manually after the cloud upgrade.

### On prem Versions
You will be able to find the OnPrem version of PrintVis here
[PrintVis Release](https://github.com/printvis/ReleaseLogs) 
 **_NOTE:_**  Older Version and upgrade tools can be found on our partner page [PrintVis Partner Page](https://www.printvispartner.com)
 

### Printvis PTE app migration
PrintVis have some apps that have been converted to PTE apps so it will be possible to use them in Cloud

Sales Order integration
PrintVis CIM

you can find the upgrade info in our Open Source Repo for each app that we have made migration app for on our open source repo
[PrintVis Open Source Github Repo](https://github.com/printvis/OpenSource)

### BC 14 C/side migration to app
when migrating fom c/side to app please take note that PrintVis is being split into multiple apps when migrating.

PrintVis
Sales Order integration
PrintVis CIM

## Upgrade path for BC 14 to 25+

on our partner page you can get the empty apps needed to use when you follow Microsoft upgrade path in the Upgrade Tool kit for PV14.0 to PV16.0.

In our [Open source](https://github.com/printvis/OpenSource) repo. you can find upgrade for some of our apps, the way they are structured is by using 3 different app's 
- Data app 
- Transfer to Data App
- Transfer to the new App

the reason for doing it this way is to be able to avoid ANY dependency and name / id conflict between the Old and the New app.

How to use

1. Install the Data app.
2. Install the Transfer to Data app. since they use the oninstall trigger it will copy all the records to the data app.
3. Uninstall the Transfer to Data app.
4. Do the upgrade of BC and PrintVis to the version of used for the migration.
5. Install the new PTE app.
6. Install the transfer to the new app app,
7. uninstall the 2 upgrade apps, when the copy of the data to the new app is done.
8. Install the PTE app in cloud environment used for the migration.
9. Do the cloud migration.

this procedure can be used for all version of BC 14 and up.
it can be that some of the apps needs to be adjusted to compensate for missing decencies and table / fields that have been removed.   

