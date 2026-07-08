# Text Codes

Text Codes in PrintVis allow you to define reusable text blocks that can be applied to quotes, orders, and job tickets. They provide a way to standardize frequently-used text without manually typing it each time.

## Usage

Text Codes are used for:
- **Quote header text** — Standard terms and conditions or introductory text at the top of quotes
- **Quote footer text** — Standard closing text, payment terms, or disclaimers
- **Order header/footer text** — Similar text blocks for order confirmations
- **Job-specific text** — Standard instructions or notes that appear on job tickets

Text Codes are assigned in General Setup for system-wide defaults:
- **Text Code Quote Top** — Default text at the top of all quotes
- **Text Code Quote Bottom** — Default text at the bottom of all quotes
- **Text Code Order Top** — Default text at the top of all order confirmations
- **Text Code Order Bottom** — Default text at the bottom of all order confirmations

These can be overridden per case by selecting a different text code on the Case Card.

## Setup

Text Codes are found by searching **PrintVis Text Codes Setup**.

### Creating a Text Code

1. Search for **PrintVis Text Codes**.
2. Create a new text code with a Code and Description.
3. Enter the text content for the code.
4. The text can include line breaks and formatting.

### Assigning Default Text Codes

1. Open **General Setup**.
2. In the Case Management section, set:
   - **Text Code Quote Top**
   - **Text Code Quote Bottom**
   - **Text Code Order Top**
   - **Text Code Order Bottom**

## Examples

### Example: Standard Terms and Conditions Text Code

Create a text code: Code = T&C-QUOTE, Description = "Standard Quote Terms"

Content:
```
This quotation is valid for 30 days from the date of issue. 
Prices are based on the specifications provided. 
Any changes to specifications may result in revised pricing.
Payment terms: Net 30 days from invoice date.
```

Assign this text code as **Text Code Quote Bottom** in General Setup. It will appear at the bottom of every quote.

## See Also

- [General Setup](../setup/general-setup.md)
- [Report Setup](../reports/report-setup.md)
