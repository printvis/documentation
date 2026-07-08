# Planning Overview

PrintVis provides a comprehensive planning and scheduling system that integrates with the production workflow. Planning tools include the Production Plan, Planning Board, Milestones, Capacity management, and Auto Scheduling.

## Usage

The planning system allows coordinators and planners to:
- Schedule jobs onto specific cost centers (machines)
- Track production progress against planned timelines
- Manage capacity across all production resources
- Set up automatic scheduling based on rules
- Monitor bottlenecks and resource conflicts

Planning in PrintVis is linked to Cases and their Status Codes. A case must be at a status that allows planning before it can be scheduled.

## Key Planning Tools

| Tool | Description |
|---|---|
| **Production Plan** | List-based view of all jobs in the production queue, showing planned and actual dates |
| **Planning Board** | Gantt-chart-style visual scheduling tool for drag-and-drop planning |
| **Planning Units** | Defines how production units are scheduled (by cost center, by day, by shift) |
| **Milestones** | Key dates and checkpoints for production tracking |
| **Capacity Resources** | Individual operators/employees linked to production planning |
| **Capacity Groups** | Groups of resources that can be scheduled together |
| **Opening Hours** | Calendar defining when each cost center or resource is available |
| **Auto Scheduling** | Rules-based automatic scheduling that places jobs based on capacity and deadlines |
| **Bottleneck Planning** | Identifies and plans around capacity constraints |

## Setup

Planning setup involves:
1. [Opening Hours](opening-hours.md) — Define when cost centers are available
2. [Capacity Resources](capacity-resources.md) — Set up operators and resources
3. [Planning Units](planning-units.md) — Configure how planning units work
4. [Milestones](milestones.md) — Set up production checkpoints
5. [Auto Scheduling](auto-scheduling.md) — Configure scheduling rules (if using auto scheduling)

## See Also

- [Production Plan](production-plan.md)
- [Planning Board](planning-board.md)
- [Case Card](../case-management/case-card.md)
