# PrintVis WIP Journal

The PrintVis WIP Journal page allows the calculation of the WIP amount, to print a WIP report, and to post WIP amounts into the G/L entries.

## How it works

The most important page actions are:

- **Build WIP Journal** - Selecting this action will prompt the user for a posting date and then build the WIP journal based on the **PrintVis WIP Setup**.
- **Show/Hide no WIP** - When building the WIP Journal, all active order cases that have not been archived are included in the build process. Archived cases that have previous (unreversed) WIP postings are also included in the build process. By default, after calculating, the WIP Journal hides any of the cases that have a calculated WIP amount = 0. The Show/Hide no WIP action will display/hide these 0 WIP amount entries.
- **Post WIP to G/L** - This action posts all entries in the WIP journal to the G/L entries. Every time the WIP journal is posted, all previous WIP G/L entries for that case/account are reversed and new entries are created.

If necessary, the user can manually correct the values in the WIP Journal Line and post new values.

The WIP Journal shows the columns associated with the **WIP Method** in the **PrintVis WIP Setup**.

## See Also

- <a href="../pvswipsetup/" target="_self">PrintVis WIP Setup</a>
- <a href="../pvspostedwip/" target="_self">Posted WIP Entries</a>