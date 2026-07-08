# Job Material Movement

Job Material Movement (also called Pick) in PrintVis handles the physical movement of materials from the warehouse to the press or production area. It creates BC inventory movements or picks that transfer materials to the appropriate location for the job.

## Usage

Job Material Movement is used when:
- Materials are stored in a warehouse location and need to be moved to the press room
- Physical inventory control requires pick lists for material movement
- You want to track when materials were physically moved for a job

The process:
1. Based on material requirements, a pick list is created for the materials needed.
2. Warehouse staff use the pick list to physically move materials.
3. After movement, the system records that materials have been transferred.
4. At production time, materials are consumed from the press room location.

## Setup

Job Material Movement requires:
- BC Inventory/Warehouse location setup
- Location codes configured for press room(s) and warehouse
- Item ledger entries set up for inventory movement

!!! warning "Missing Content"
    Detailed setup instructions for Job Material Movement are not fully documented in the current source material. Contact PrintVis support or refer to the legacy Job Material Movement documentation.

## Examples

!!! warning "Missing Content"
    No specific examples are currently documented for Job Material Movement.

## See Also

- [Material Requirements](material-requirements.md)
- [Items](items.md)
- [Shop Floor](../shop-floor/shop-floor.md)
