# Calculation Formulas

Calculation Formulas allow you to define custom calculation logic in PrintVis estimation. They are used within Calculation Units to perform calculations that go beyond simple time or quantity lookups — such as complex material calculations, conditional logic, or multi-factor formulas.

## Usage

Calculation Formulas are referenced from Calculation Unit lines. When a line uses a formula, the formula is evaluated to determine the calculated value (time, quantity, cost, etc.).

Common uses:
- Calculating ink consumption based on coverage, format, and quantity
- Calculating paper waste using a custom formula
- Computing a cost based on multiple variables (quantity, format, colors)
- Adding a fixed charge per job plus a variable charge per unit

### Custom Formulas with Additional Quantities

Formulas can be set up to handle custom quantity inputs. For example, a formula can accept an "additional quantity" input from the estimator and incorporate it into the calculation. See [Tips & Tricks](tips-tricks.md) for specific examples.

### Formula on a Speed Table

Custom formulas can also be used in conjunction with speed tables to modify the calculated speed based on additional factors. See [Tips & Tricks](tips-tricks.md) for details.

## Setup

Calculation Formulas are found by searching **PrintVis Calculation Formulas**.

!!! warning "Missing Content"
    Detailed field-by-field setup documentation for Calculation Formulas is not fully included in the available source material. Contact PrintVis support or refer to the legacy Formulas documentation (Legacy/Estimation/Formulas.md) for detailed field descriptions and formula syntax.

### General Setup Steps

1. Search for **PrintVis Calculation Formulas**.
2. Create a new formula with a Code and Description.
3. Define the formula logic using PrintVis formula syntax.
4. Test the formula by using it in a calculation unit on a test case.
5. Assign the formula to a calculation unit line.

## Examples

!!! warning "Missing Content"
    Specific formula examples with full syntax are not available in the current source material. Refer to the legacy Formulas documentation for examples of formula syntax and usage patterns.

## See Also

- [Calculation Units](calculation-units.md)
- [Tips & Tricks](tips-tricks.md)
- [Estimation Overview](overview.md)
