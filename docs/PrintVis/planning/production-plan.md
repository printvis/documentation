# Production Plan

The Production Plan in PrintVis is a list-based view of all jobs in the production queue. It provides an overview of what is planned, when each job is scheduled, and how production is progressing.

## Usage

The Production Plan is the primary tool for coordinators to:
- See all jobs currently in production or scheduled for production
- Check planned start and end dates for each job/operation
- Monitor job status and identify delays
- Change status, assign resources, or add comments to jobs
- Navigate to the Planning Board for detailed scheduling

### Key Information in the Production Plan

- **Case/Job information** — Customer, job name, order type, deadline
- **Planning Unit** — Which cost center/machine the operation is planned on
- **Planned dates** — When the operation is scheduled to start and end
- **Status** — Current production status (planned, in progress, complete)
- **Capacity** — How much capacity is allocated

### Filtering and Sorting

The Production Plan can be filtered by:
- Department
- Planning Unit / Cost Center
- Date range
- Status Code
- Responsible user

This allows each department to see only their relevant jobs.

## Setup

The Production Plan displays data based on:
- **Planning Units** — Must be set up for each cost center you want to plan
- **Status Codes** — The case must be at a status that allows planning
- **Opening Hours** — Used to calculate available capacity

### Enabling Planning for a Status Code

1. Open the **Status Code** for the production stage.
2. Enable the **Allow Planning** flag.
3. Cases at this status can now appear in the Production Plan.

## Examples

!!! warning "Missing Content"
    Detailed step-by-step usage examples for the Production Plan are not fully documented in the current source material. Refer to the legacy Production Plan documentation for specific navigation and workflow examples.

## See Also

- [Planning Board](planning-board.md)
- [Planning Units](planning-units.md)
- [Status Codes](../case-management/status-codes.md)
- [Opening Hours](opening-hours.md)
