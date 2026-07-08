# JDF (CIM) Integration

JDF (Job Definition Format) is an industry-standard XML format used for communication between print production systems. PrintVis supports JDF integration (also referred to as CIM — Computer Integrated Manufacturing) to connect with prepress systems, MIS systems, and production equipment.

## Usage

JDF integration in PrintVis is used to:
- Send job data to prepress systems (e.g., Esko, Kodak Prinergy) when a case reaches a specific status
- Receive production feedback from shop floor equipment
- Automate the flow of job information from MIS to production systems
- Reduce manual data entry by automatically transferring job specifications

### JDF Triggers

JDF messages can be triggered automatically when a case changes to a specific Status Code. Configure this in the **Status Code** setup by enabling the **Send CIM/JDF** flag.

### JDF Technical Communication

JDF integration uses a two-way communication setup:
- **PrintVis → External system** — Sends job data when a case reaches the configured status
- **External system → PrintVis** — Receives production feedback (e.g., actual run times, material consumption)

## Setup

JDF setup involves two parts:

### JDF Setup Data

1. Search for **PrintVis JDF Setup** or access via the Advanced Setup menu.
2. Configure the connection to the external system (server address, credentials, data format).

### JDF Technical Communications

1. Configure the communication protocol (HTTP, file-based, etc.).
2. Define the data mappings between PrintVis fields and JDF fields.
3. Test the connection with a sample job.

!!! warning "Missing Content"
    Detailed JDF setup documentation is not fully consolidated in this article. Refer to the legacy JDF Setup Data and JDF Technical Communications documentation for complete setup instructions.

## Examples

!!! warning "Missing Content"
    No specific JDF integration examples are currently documented. Contact PrintVis support for guidance on configuring JDF for your specific prepress system.

## See Also

- [Status Codes](../case-management/status-codes.md)
- [Esko Integration](esko.md)
- [PrintVis Link](printvis-link.md)
