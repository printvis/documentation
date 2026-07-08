# Format Codes

Format Codes define the standard paper and substrate sizes used in PrintVis estimation. They are a foundational piece of master data used throughout estimation for calculating sheet layouts, impositions, and material requirements.

## Usage

Format Codes are used when:
- Selecting the format of a job on the Case Card or job line
- Calculating how many pages fit on a sheet (imposition)
- Determining machine run speeds (via Speed Tables that use format codes)
- Calculating paper consumption and scrap

Formats in PrintVis can be defined as standard sheet sizes, web widths, or roll widths depending on the production process.

## Setup

Format Codes are found by searching **PrintVis Format Codes**.

!!! warning "Assisted Setup Reminder"
    Format Codes are one of the sections covered in PrintVis Assisted Setup. If you are setting up a new company, consider using Assisted Setup to import standard format codes from the reference database.

### Field Descriptions

| Field | Description |
|---|---|
| **Code** | Unique identifier for the format (e.g., A4, A3, LETTER, 8.5x11). |
| **Description** | Full name of the format. |
| **Format Type** | Sheet, Web, or Roll — determines how the format is used in calculation. |
| **Length** | Length of the format (in the unit of measure set up in General Setup). |
| **Width** | Width of the format. |
| **Grain Direction** | Default grain direction for this format (Long, Short, or Any). |

### Configuring for Metric or Imperial

The unit of measure for format dimensions is controlled by the **Captions on Options** setting in General Setup (Metric or Imperial). Ensure format codes are entered in the correct units for your region.

## Examples

### Example: Common Format Codes for a Commercial Print Shop (Metric)

| Code | Description | Length | Width |
|---|---|---|---|
| A4 | A4 Sheet | 297 | 210 |
| A3 | A3 Sheet | 420 | 297 |
| SRA3 | SRA3 Sheet | 450 | 320 |
| 70X100 | 70 x 100 cm | 1000 | 700 |
| 52X74 | 52 x 74 cm | 740 | 520 |

### Example: Common Format Codes for a North American Print Shop (Imperial)

| Code | Description | Length | Width |
|---|---|---|---|
| LETTER | Letter 8.5 x 11 | 11 | 8.5 |
| LEGAL | Legal 8.5 x 14 | 14 | 8.5 |
| TABLOID | Tabloid 11 x 17 | 17 | 11 |
| 25X38 | 25 x 38 inch | 38 | 25 |
| 28X40 | 28 x 40 inch | 40 | 28 |

## See Also

- [Estimation Overview](overview.md)
- [Speed Tables](speed-tables.md)
- [General Setup](../setup/general-setup.md)
