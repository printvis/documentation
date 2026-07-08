# Planning Units

Planning Units define how individual operations within a cost center are scheduled and tracked in the PrintVis production plan. Each Planning Unit represents a schedulable slot on a specific machine or resource.

## Usage

Planning Units are the fundamental units of production scheduling in PrintVis. They appear on the Production Plan and Planning Board as the rows/resources that jobs are scheduled against.

A Planning Unit typically maps to:
- A specific machine or cost center
- A shift or time-of-day slot
- A specific operator or team

### Planning Unit Status Codes

Each Planning Unit can have its own Status Code that controls:
- What is visible in the production plan
- When a unit is available for scheduling
- How job progress is tracked

## Setup

Planning Units are found by searching **PrintVis Planning Units**.

### Field Descriptions

| Field | Description |
|---|---|
| **Code** | Unique identifier for the planning unit. |
| **Description** | Name of the planning unit. |
| **Cost Center** | The cost center this planning unit is linked to. |
| **Department** | The department this planning unit belongs to. |
| **Sorting Order** | Controls the display order in the Production Plan and Planning Board. |
| **Capacity** | The nominal capacity of this planning unit (used for load calculations). |

### Linking Planning Units to Cost Centers

Each cost center that needs to appear in the Production Plan must have at least one Planning Unit. Multiple Planning Units can be linked to the same cost center (e.g., for multi-shift operations or when a cost center has multiple identical machines).

## Examples

!!! warning "Missing Content"
    Detailed Planning Unit setup examples are not fully documented in the current source material. Refer to the legacy Planning Units documentation for specific configuration examples.

## See Also

- [Production Plan](production-plan.md)
- [Planning Board](planning-board.md)
- [Capacity Resources](capacity-resources.md)
- [Opening Hours](opening-hours.md)
