## Usage

### View live count summary on Electronic Ticket

When the current user is logged into a configured Cost Center, the Electronic Ticket page shows the SpencerMetrics Count Summary FactBox.

The FactBox displays accumulated Difference Count values grouped by UOM for the active job context.

### Review detailed counter entries

Open SpencerMetrics Counter Entries to inspect each reading:

- Current Count
- Difference Count
- Current Time
- Device Status
- Speed
- Case ID and Plan ID
- Include In Job Costing

Use XML Content to review the raw SpencerMetrics payload for a selected entry.

### Assign missed counts to Job Costing

If counts were not automatically included in job costing, they can be assigned manually:

1. Open SpencerMetrics Counter Entries.
2. Select an entry where Include In Job Costing is false.
3. Choose Assign to Job Costing.
4. Select a Job Costing Entry from the same Cost Center.
5. Confirm with OK.

Result:

- Job Costing quantity is incremented by the selected Difference Count.
- The counter entry is marked as included in job costing.

## Example

### Example scenario: Finishing line with 15-second polling

A company tracks a finishing Cost Center named FIN-01.

Configuration:

- Cost Center: FIN-01
- Interval: 15000 ms
- Max Session Duration: 480 min
- API Key: valid key from SpencerMetrics

During production:

1. Operator logs into Shop Floor on FIN-01.
2. The integration session starts automatically.
3. Counter entries are collected every 15 seconds.
4. Electronic Ticket FactBox updates with live accumulated counts.

Sample counter sequence:

- Entry 1001: Current Count = 120000, Difference Count = 0
- Entry 1002: Current Count = 120240, Difference Count = 240
- Entry 1003: Current Count = 120460, Difference Count = 220

If one reading was not tied to a Job Costing record, a supervisor opens Counter Entries and uses Assign to Job Costing for that row.

Outcome:

- Captured machine output remains aligned with actual job costing quantities.
- Session activity can be audited in Session Log.

## Troubleshooting

### Unauthorized - invalid login key

- Recheck API Key for the Cost Center.
- Confirm API key is active in SpencerMetrics.

### Invalid JSON response

- Verify Base URL is correct.
- Check external connectivity from the Business Central environment.

### No new entries created

- Confirm the user logged into Shop Floor on the configured Cost Center.
- Confirm Enabled is true and Last Heartbeat is updating.
- Check Session Log for failed session start events.
- Check the permissions on the Microsoft Entra Application setup. This can occur if the application doesn't have permission to read/write information.