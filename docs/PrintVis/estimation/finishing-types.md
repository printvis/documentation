# Finishing Types

Finishing Types define the different finishing processes available in PrintVis estimation. They are used to categorize and select finishing operations on job sheets, enabling the estimation system to calculate finishing costs correctly.

## Usage

Finishing Types are assigned to job sheets/items on the Job Card. They help:
- Define what finishing operations are applicable for a given sheet
- Filter available Calculation Units to show only relevant finishing options
- Control imposition (some finishing types, like die-cutting, have specific imposition requirements)
- Appear on the Job Ticket as process descriptions

## Setup

Finishing Types are found by searching **PrintVis Finishing Types**.

!!! warning "Missing Content"
    Detailed field-by-field documentation for Finishing Types is not fully available in the current source material. Contact PrintVis support for detailed setup guidance.

### General Field Descriptions

| Field | Description |
|---|---|
| **Code** | Unique identifier for the finishing type. |
| **Description** | Name of the finishing type. |
| **Sorting Order** | Controls the display order in selection lists. |

## Examples

### Example: Common Finishing Types

| Code | Description |
|---|---|
| FOLD | Folding |
| SADDLE | Saddle Stitching |
| PERFECT | Perfect Binding |
| CUT | Trimming/Cutting |
| LAMINATE | Laminating |
| DIE-CUT | Die Cutting |
| EMBOSS | Embossing |
| FOIL | Foil Stamping |
| SPIRAL | Spiral Binding |
| WIRE-O | Wire-O Binding |

## See Also

- [Estimation Overview](overview.md)
- [Component Types](component-types.md)
- [Calculation Units](calculation-units.md)
