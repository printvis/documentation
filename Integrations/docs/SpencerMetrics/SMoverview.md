# Spencer Metrics Overview

The SpencerMetrics Integration for PrintVis captures live production counter data from SpencerMetrics-connected equipment and links that data to PrintVis Shop Floor activity.

The integration polls SpencerMetrics on a configurable interval per Cost Center, stores each counter snapshot in Business Central, and calculates:

- Current machine count
- Difference count since the previous reading
- Machine speed based on elapsed time and count difference
- Device status from the SpencerMetrics response

This allows production teams to monitor machine output directly in PrintVis and include missed or delayed counts in Job Costing.

<i>Note: We currently only support using the PrintVis Shop Floor electronic ticket. Future development may include the possibility to use the Spencer Metrics electronic ticket and get that data into PrintVis Job Costing.</i>