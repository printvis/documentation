# Copying a Case or Job

To re-use a case or job with all related data, it is possible to copy a case or job.

A copy of a case or job is a 1:1 copy, which means all data is 1:1 copied. If master data has changed, the new case or job must be updated manually by the user, e.g. if the customer address has changed. The estimate is also copied and not updated with the latest speed, cost, or price settings. In this case, a recalculation is required.

## Copy to…

The Copy to… action on the case card copies the case and its active job to a new case. Based on the PrintVis General Setup or PrintVis Users Setup, a dialog is displayed for the user to select the status code for the new case.

If there is more than 1 active version for a job, only the highest status job is copied. The job statuses are from highest to lowest: “Production Order”, “Order”, “Quote”, and “Request”.

## Copy from…

The Copy from... action copies a job into the current case. A dialog is displayed to choose a job to be copied. There is a default filter for the job of the current customer that can be disabled to choose from all existing jobs (Customer Search Yes/No). After a job is selected and the OK button is hit, the selected job is copied into the current case with the next higher job number.

Additionally, it is possible to copy the case data by enabling the field Copy Order Head or create new versions instead of new jobs by enabling the field Add New Versions.

## Copy Alternatives

Typically, if more than 1 version of a job is required, the New Version action can be used to create a copy of the current versions into a new version with all related data. This is useful if a customer requests different quantities to be quoted.

In case many alternative versions are required, the Copy Alternatives action can be used. The function can be found from the Job Actions on the Case Card - under 'Copy' -> 'Copy Alternatives'. In the page displayed, create a line for each copy. You will be required to at least fill in the quantity for each new version. Additionally, there is the possibility to state variances of the no. of Pages, Colors Front, and Colors Back for each new version. Once the OK button is hit, the new versions are copied from the current job and updated with the data from the Copy Alternatives page.

## Copy Periodic Job

Once a Job has been fully estimated, prepared, and scheduled, PrintVis offers an option to copy the job out into multiple new releases (new cases and jobs typically), for a Monthly issue of a magazine, for example.

The function can be found from the Job Actions on the Case Card - under 'Copy' -> 'Copy Periodic Job'. Once opened, you will be required to fill in publication frequencies, etc.