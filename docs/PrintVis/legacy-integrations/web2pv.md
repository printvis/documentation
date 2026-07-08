# Web2PV REST API

The Web2PV REST API allows external applications to interact with PrintVis programmatically. It provides endpoints for creating cases, querying job status, submitting files, and triggering workflows.

## Usage

The Web2PV REST API is used for:
- Web-to-print storefront integrations (customer-facing ordering)
- Automated job submission from external systems
- Real-time job status queries from portals or dashboards
- Programmatic document submission and file handling

!!! note "Advanced License Required"
    Web2PV integration requires an **Advanced PrintVis User** license and the **PVS 365 ADV Setup** permission set for configuration.

## Setup

### Back-End Setup

1. Access Web2PrintVis settings from the Admin Role Center → Web2PrintVis menu.
2. Configure API authentication (API keys, credentials).
3. Define which data is exposed via the API.
4. Set up field mappings between external data formats and PrintVis fields.

### Front-End Setup

For storefront or portal integration:
1. Configure the web application to use the PrintVis API endpoints.
2. Map the storefront's product options to PrintVis Order Types and Product Groups.
3. Test the integration with sample orders.

!!! warning "Missing Content"
    Detailed API documentation including endpoints, request/response formats, and authentication details are not fully consolidated in this article. Refer to the legacy Web2PV REST API documentation (Legacy/Integrations/Web2PVREST.md) for detailed technical guidance.

## Examples

!!! warning "Missing Content"
    No specific API integration examples are currently documented. Contact PrintVis support for API documentation and integration guidance.

## See Also

- [PrintVis Link](printvis-link.md)
- [Permission Sets](../setup/permission-sets.md)
