# Apparel Usage

The apparel functionality will feel very comfortable for those that have
experience with PrintVis and is easy to learn with this usage guide.
Please make sure to review and complete all the steps on the Apparel
installation and setup article before continuing with this article.

## Definitions

*Decoration*: the ability to save individual artwork placed somewhere on
a raw material. The decoration includes the decoration type (such as
screenprint, embroidery, transfer, etc.), placement (such as back yoke,
center chest, left chest, etc.), colors, stitches, width, height, list
of units, finishing – how the artwork will be manufactured.

*Design*: A collection of decorations that can be reused.

*Style*: A collection of items grouped based on their attributes. The
attributes include: Brand, date established, gender, brand color, color,
base required, item type code, allowed decoration types, and allowed
decoration placements.

Creating an apparel case

General Case

The general section of the case card is identical to standard PrintVis.
Based on your industry caption setup, the rest of the case card will
adjust based on the order type or product group being an Apparel type.

![Apparel Usage](./assets/AU1.jpg)


Jobs Area

When the apparel functionality is enabled, the Jobs list has a Design
field and the Ordered Quantity field is now a link. The Design field can
be used to select a previously used design and automatically fill in the
decorations. The ordered quantity allows you to select the different
garment/material items for the job.

![Apparel Usage](./assets/AU2.jpg)

Clicking into the ordered quantity field displays the below page and
selecting the dropdown on the No. field will display a list of styles.

![Apparel Usage](./assets/AU3.jpg)

Selecting a style will display all the items or variants associated with
that style. Add the quantity for each size then you can click Close on
the page.

![Apparel Usage](./assets/AU4.jpg)

The Remove 0 Lines action will remove all the sizes that have no
quantity entered to clear up the list. The Load Style Items action will
reload all the sizes for the style if you removed any 0 quantities.

Once you return to the case card the ordered quantity will be updated to
the sum quantity of all the sizes.

There are also two calculation fields to show the material price per
piece and the production price per piece. These are the average material
and production prices per piece.

To save a design for use later, select the line to save and click the
Save Design action. This will display a dialog box using the design
number series as the New Code and a description of the design can be
entered. Clicking ok will create a design with all the decoration lines
and assign the design to the sell-to customer from the case.


Decorations Area

![Apparel Usage](./assets/AU5.jpg)

The decoration area allows you to add the decoration specifications for
the case. This includes the decoration type, placement, quantity,
colors, stitches, width, height, list of units, and finishing types.

To add additional decorations, click the New Decoration action. To
remove a decoration, select that line and click the Delete Decoration
action.

To save a decoration for use later, select the line to save and click
the Save Decoration action. This will display a dialog box using the
decoration number series as the New Code and a description of the
decoration can be entered. Clicking ok will create the decoration with
all the settings from the line and assign the decoration to the sell-to
customer from the case.

![Apparel Usage](./assets/AU6.jpg)

## Scheduling

To address the fact that decorations cannot be manufactured at the same
time since all the decorations are placed on the same garment/material,
a new setting is available on the planning unit to ensure this does not
occur. For calculation units that need to be done consecutively, assign
them to a planning unit and set that planning unit with a milestone
effect on flow setting of “Arranged”.

![Apparel Usage](./assets/AU7.jpg)

Using this setting will allow the flexibility to use concurrent and
consecutive steps within the same case. Here is an example of its use:

![Apparel Usage](./assets/AU8.jpg)

In the above schedule planning unit 3000 and 7000 are set with standard
milestone effect on flow and planning unit 5000 is set to Arranged.
Prepress is also set to allow multiple jobs at the same time.

You can see that the Sheet/Decoration No. 1 and 2 are done at the same
time for Prepress but once sent to the Diamondback screen printer they
are done one after the other. The Chiossi E Cavazzuti dryer continues
with this pattern because this machine only allows one job at a time.

## Shipping

The shipment page is updated when apparel is installed to include a
shipment allocation grid for each shipment.

![Apparel Usage](./assets/AU9.jpg)

This grid is automatically filled in with the items from the case and
updated as the case items are updated. These quantities can also be
manually updated on the allocation grid for each shipment. When a new
shipment is created it will automatically fill in the difference between
the other shipments and case quantity of each item.

## Invoicing

To invoice apparel cases, it is recommended to use the Case Shipment
Method “Create Sales Order and Post.”