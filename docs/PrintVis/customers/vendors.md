# Vendors

Vendors in PrintVis are managed through the standard Business Central Vendor Card. They are used for purchasing materials, subcontracting services, and managing supplier relationships in the context of print production.

## Usage

Vendors are used in PrintVis for:

- **Purchasing materials** — Paper, inks, substrates, and other consumables are purchased from vendors through BC purchase orders
- **Subcontracting** — External finishing, specialty printing, or other outsourced work is managed through purchase orders linked to PrintVis jobs
- **Purchase Guide** — The PrintVis Purchase Guide uses vendor information to suggest purchase orders for job materials
- **Price lists and agreements** — Vendor pricing can be set up for recurring purchases

## Setup

### Creating a New Vendor

1. Search for **Vendors** in Business Central.
2. Click **New**.
3. Select a **Vendor Template** if available to pre-fill default settings.
4. Fill in all required fields:
   - **Name**
   - **Address** (Street, City, Post Code, Country)
   - **Gen. Bus. Posting Group**
   - **VAT Bus. Posting Group**
   - **Vendor Posting Group**
   - **Payment Terms**
   - **Currency Code** (if not in local currency)

### Creating a Vendor from a Contact

If you have an existing Contact for the vendor:

1. Go to the **Contact List**.
2. Find the contact.
3. Open **Actions** → **Functions** → **Create As** → **Vendor**.
4. Select the appropriate Vendor Template.
5. The system creates a vendor card linked to the contact.

### Linking Vendors to Items

For materials used in PrintVis jobs, link vendors to items via the **Item Vendor** subpage on the Item Card. This enables:
- Vendor-specific item numbers (cross-references)
- Vendor-specific lead times
- Vendor pricing for purchase orders

## Examples

!!! warning "Missing Content"
    No specific PrintVis-vendor workflow examples are currently documented. For subcontracting-specific vendor setup, refer to the Estimation section on Subcontracting configuration.

## See Also

- [Customers](customers.md)
- [Purchase Guide](../warehouse/purchase-guide.md)
- [Items](../warehouse/items.md)
