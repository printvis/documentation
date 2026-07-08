# Component Types

Component Types define the different structural parts that make up a print job. They are used in estimation to organize and label the various components of a product (e.g., cover, text body, insert, spine, flap) and control how job items are structured on the Case Card.

## Usage

Component Types appear on:
- The Job Card — each job item (sheet) is assigned a component type
- Imposition calculations — component types affect how sheets are arranged
- Job Ticket — component type labels appear on the job ticket to describe each part of the job
- Reports — component types provide structure for job reporting

Common component types for a book:
- **Cover** — The outer cover sheets
- **Text** — The main text body
- **Insert** — A special insert page
- **Endpaper** — End papers for hardcover books
- **Spine** — Spine label for case-bound books

## Setup

Component Types are found by searching **PrintVis Component Types**.

!!! warning "Assisted Setup Note"
    Component Types are one of the sections covered in PrintVis Assisted Setup. Standard component types can be imported from the reference database during initial setup.

### Field Descriptions

| Field | Description |
|---|---|
| **Code** | Unique identifier for the component type. |
| **Description** | Name of the component type as displayed in the system. |
| **Sorting Order** | Controls the display order in selection lists. |

## Examples

### Example: Component Types for a Hardcover Book

| Code | Description |
|---|---|
| COVER | Cover |
| TEXT | Text Body |
| ENDPAPER | End Paper |
| JACKET | Dust Jacket |
| HEADBAND | Headband |

### Example: Component Types for a Folded Brochure

| Code | Description |
|---|---|
| SELF-COVER | Self-Cover (text and cover same stock) |
| COVER | Separate Cover |
| TEXT | Text Pages |
| INSERT | Loose Insert |

## See Also

- [Estimation Overview](overview.md)
- [Templates](templates.md)
- [Finishing Types](finishing-types.md)
