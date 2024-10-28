# Item Type Codes

Item Type Codes are used to categorize items and to select and map **Item Types**. While **Item Types** are fixed options that are used throughout the PrintVis application, Item Type Codes must be linked to an existing Item Type option.

## How it works

It is mandatory to have **Item Type Codes** setup because **Item Types** cannot be selected directly on the **Item Card**, the field is not editable. The **Item Type** is set by the selected **Item Type Code** and is a mandatory field for Items used with PrintVis.

PrintVis options for **Item Types** are:

- **Paper** - Must be used for all print substrates, otherwise no possibility to choose an item as print substrate.
- **Plates** - All printing plates/cylinders, e.g. offset, flexo, flexo sleeves, screen, letterpress, rotogravure, etc.
- **Film** - For films used in prepress. Others are not relevant anymore and could be used for something else.
- **Ink** - Must be used for all ink, varnish, or glue items, otherwise no possibility to choose an item on color/glue/ink/consumables table.
- **Die** - All items to handle dies and other tools.
- **Repro** - For repro items used in prepress. Others are not relevant anymore and could be used for something else.
- **External Finishing** - Must be used for all items for subcontractors.
- **Finished Goods** - All finished products that are put on stock after production. See Label/Envelope.
- **Block** - Fixed use is not defined.
- **Label** - All finished products that are labels that are put on stock after production.
- **Envelope** - All finished products that are envelopes that are put on stock after production.
- **Board** - This is a special board type only used for the ESKO ArtiosCAD integration. Do not use this Item Type if the Item must be used as print substrate. Please see option "Paper".

## See Also

- <a href="../item/" target="_self">Item</a>
- <a href="../pvsitemtypefilter/" target="_self">Item Type Code Filters</a>