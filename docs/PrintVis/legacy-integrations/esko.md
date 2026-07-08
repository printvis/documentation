# Esko Integration

PrintVis integrates with Esko's prepress and packaging workflow systems. The integration supports both Esko Folding Carton and Esko Label workflows, enabling automated data exchange between PrintVis and Esko Automation Engine or WebCenter.

## Usage

The Esko integration is used to:
- Automatically send job data from PrintVis to Esko when a job is released to prepress
- Receive prepress status feedback from Esko into PrintVis
- Transfer structural design data (die lines, 3D models) between systems
- Automate the prepress workflow based on PrintVis job specifications

### Esko Folding Carton

For packaging print shops producing folding cartons, the Esko Folding Carton integration handles:
- Transfer of carton structure data to Esko
- Prepress workflow automation for folding carton jobs
- Status feedback from Esko (e.g., "Proof Approved", "CTP Complete")

### Esko Label

For label printers, the Esko Label integration handles:
- Label artwork and specification transfer
- Flexo/digital prepress workflow automation
- Status feedback for label jobs

## Setup

The Esko integration uses the JDF/CIM communication framework in PrintVis. See [JDF Integration](jdf.md) for the base communication setup.

!!! warning "Missing Content"
    Detailed Esko-specific setup documentation is not fully available in this article. Refer to the legacy Esko Folding Carton and Esko Label documentation for specific configuration steps.

## Examples

!!! warning "Missing Content"
    No specific Esko integration examples are currently documented. Contact PrintVis support for guidance on configuring the Esko integration.

## See Also

- [JDF Integration](jdf.md)
- [PrintVis Link](printvis-link.md)
