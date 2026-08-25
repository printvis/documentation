## Setup

### Prerequisites

- PrintVis installed and running on Business Central.
- SpencerMetrics API key available for each Cost Center.
- User permission to configure PrintVis and integration setup pages.
- Permission set assigned for this app: PVS SM FULL.

### Step 1: Create Microsoft Entra App Registration and map it in Business Central

Before configuring SpencerMetrics setup values, create an App Registration in Microsoft Entra ID for the integration identity.

In Business Central, open Microsoft Entra Applications and create a record for this App Registration:

- Set the Client ID to the Application (client) ID from Microsoft Entra.
- Configure the app so user access and permission setup are managed through this identity.
- Assign permission sets required for this integration, including Spencer Metrics permission set PVS SM FULL.

This ensures the integration identity has the appropriate permissions to access the extension pages, tables, codeunits, and queries used by SpencerMetrics.

### Step 2: Configure global SpencerMetrics settings

Open SpencerMetrics Setup and configure:

- Base URL
  - Default value: https://clientlogin.spencermetrics.com/api/
- Max Session Duration (min)
  - Default value: 480
  - Set to 0 to disable automatic session rotation

### Step 3: Configure Cost Center setup

Open SpencerMetrics Cost Center Setup and create one line per Cost Center:

- Cost Center
- API Key
- Interval (ms)

Recommended interval:

- Minimum supported value: 5000
- Recommended operational value: 15000 or higher

### Step 4: Verify background session start

The integration starts automatically when a Shop Floor user logs in on a configured Cost Center.

Verify these fields in SpencerMetrics Cost Center Setup after a user logs in:

- Enabled = true
- Session ID is populated
- Last Heartbeat updates continuously
- Session Error is blank

If sessions rotate, check Session Log for Start and Stop events.