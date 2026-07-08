# Extra Work Codes

Extra Work Codes in PrintVis allow operators to register additional work activities that fall outside the standard job structure. They are used when production tasks are not covered by the standard calculation units in the estimate.

## Usage

Extra Work Codes are used for:
- Additional work that was not planned or estimated
- Rework or quality corrections
- Special processes performed on an ad-hoc basis
- Recording time for tasks outside the normal job workflow

Extra Work Codes appear in the Job Costing Journal and are posted as additional job costing entries against the case.

## Setup

!!! warning "Assisted Setup Note"
    Extra Work Codes are one of the sections in PrintVis Assisted Setup. Standard codes can be imported from the reference database.

Extra Work Codes are found by searching **PrintVis Extra Work Codes**.

### Field Descriptions

| Field | Description |
|---|---|
| **Code** | Unique identifier for the extra work code. |
| **Description** | Description of the extra work activity. |
| **Cost Center** | The cost center to post this extra work against. |
| **Unit of Measure** | The unit for registering this work (hours, minutes, etc.). |
| **Rate Type** | How costs are calculated (hourly rate, fixed charge, etc.). |

## Examples

### Example: Common Extra Work Codes

| Code | Description |
|---|---|
| REWORK | Quality Rework |
| REPRINT | Reprint due to error |
| CUSTOMER-REQ | Special customer request |
| ARTWORK-CHANGE | Late artwork change by customer |
| FREIGHT | Special freight handling |

## See Also

- [Work Codes](work-codes.md)
- [Shop Floor](shop-floor.md)
- [Job Costing](job-costing.md)
