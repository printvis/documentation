# Navigation & Tips

This article covers helpful tips for navigating PrintVis and Business Central, including dynamic date filters, finding hidden fields, resetting user customizations, and using the tile/brick view.

## Usage

### Searching in Business Central

Business Central provides a universal search function accessible via the magnifying glass icon (or **Alt+Q**). Use search to quickly navigate to any page, report, or setup area in PrintVis or Business Central without using the menu navigation.

**Tips for effective searching:**
- Search for partial words — Business Central matches on any part of the page name
- Use the search results categories (Pages, Reports, Documentation) to narrow results
- Recently visited pages appear at the top of the search results

### Tile and Brick View

Lists in Business Central can be displayed in two views:

| View | Description |
|---|---|
| **List view** | Displays records as rows in a table — ideal for scanning many records quickly |
| **Tile/Brick view** | Displays records as visual tiles — ideal for visual scanning and touchscreens |

Toggle between views using the view selector icons in the upper right corner of any list page.

### Dynamic Date Filters

Dynamic date filters allow you to filter dates relative to today's date without entering a specific date. These are supported throughout Business Central and PrintVis list views and reports.

| Filter Code | Description |
|---|---|
| `T` | Today |
| `T-1D` | Yesterday (Today minus 1 Day) |
| `T+1W` | One week from today |
| `T-1M` | One month ago |
| `W` | Current week (from start to end) |
| `M` | Current month |
| `Q` | Current quarter |
| `Y` | Current year |
| `CW` | Current week |
| `CM` | Current month |
| `CY` | Current year |

**Example:** To filter cases created in the last 30 days, enter `T-30D..T` in a date filter field.

### Finding Hidden Fields

If a field you need is not visible on a page, it may be hidden. Business Central allows you to personalize pages to show hidden fields:

1. Click the settings icon (gear) → **Personalize** (or use **Alt+F2**)
2. Click **+ Field** to see a list of all available fields for the current page
3. Drag the field you want from the list to the position where you want it
4. Click **Done** to save your personalization

### Resetting User Customizations

If a page appears incorrectly or personalization is causing issues, you can reset it:

1. Go to the affected page
2. Click the settings icon (gear) → **Personalize**
3. Click **Clear personalization** to reset the page to its default layout

To reset all personalizations for a user:

1. Search for **User Personalizations**
2. Find the affected user
3. Use the **Delete** action to remove all personalization for that user

## Setup

!!! warning "Missing Content"
    Navigation features are part of Business Central's built-in functionality and do not require PrintVis-specific setup. Role-based navigation is controlled through [Role Centers](role-centers.md) and [Users](../setup/users.md).

## Examples

### Example: Using Dynamic Date Filters in the Case List

To find all open quotes created this week:

1. Open the PrintVis Case List
2. Filter **Status Type** = Quote
3. Filter **Date of Creation** = `CW`

This returns all quote cases created during the current week, regardless of what day you run the filter.

## See Also

- [Role Centers](role-centers.md)
- [Users](../setup/users.md)
