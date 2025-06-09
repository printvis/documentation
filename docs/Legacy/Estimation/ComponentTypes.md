# Component Types and Job Item Format Setup

## Summary

The PrintVis Component Types can be used to set default for every job
item to automate and simplify the input for the user. The component
types can act as a \"small template\" to preset default sheet,
imposition or finishing settings. The available component types can be
assigned to each Product Group (PrintVis Product Group Lookup Filters)
to ensure that only the relevant ones for the actual product group can
be selected.

By using Lists of Components it is even possible by selecting one list
to enfold all sheets/job items, such as for a hardcover book that
contains:

-   Hard-cover board

-   Hard-cover cloth or paper covering

-   Dust Jacket

-   Front paper

-   Back paper

-   Text/body

On top of the product size (Final Format), it is possible to define
additional flaps or other areas by using the Job Item Format Setup and
assigning them to each component type. This can be relevant for
packaging products in defining areas for gussets, zippers, etc. With
that PrintVis is able to calculate the open size of the product for an
exact calculation of the required print substrate.

## Component Types

A common list for commercial printing might look like this:

![Image](./assets/image1.png){width="6.5in"
height="4.282638888888889in"}

The example below shows a common setup for a cover of a perfect bound
book. Fields that are not filled will retain the default value from the
job or template.

![Image](./assets/image2.png){width="6.5in"
height="8.230555555555556in"}

Fields

+---------------+------------------------------------------------------+
| Pages with    | Number of pages with print this component will have. |
| Print         | This number will be transferred to the job item.\    |
|               | This can be useful for a a component of type cover   |
|               | that always contains 4 pages instead of using the    |
|               | pages from the job input                             |
+===============+======================================================+
| Colors Front  | The number of colors to be printed on the front of   |
|               | the printed item. This value will be transferred to  |
|               | the field \"Colors Front\" on the job item.          |
+---------------+------------------------------------------------------+
| Colors Back   | The number of colors to be printed on the back of    |
|               | the printed item. This value will be transferred to  |
|               | the field \"Colors Back\" on the job item.           |
+---------------+------------------------------------------------------+
| Job Item      | This field may contain a predefined final format     |
| Format Code   | which will be transferred to the job item. This is   |
|               | an option which is mainly used if the component acts |
|               | as a more complete template for a particular         |
|               | product.\                                            |
|               | Example: Business cards often have a the same size.  |
+---------------+------------------------------------------------------+
| Paper Item    | This value will be transferred to the job items      |
| No.           | Paper Item Number Field, in case there is a standard |
|               | paper for this component type.                       |
+---------------+------------------------------------------------------+
| Finishing     | This value will be transferred to the Finishing      |
|               | field of the Job Item, in case there is standard     |
|               | finishing type for this component type.\             |
|               | Example: Covers always need trimming.                |
+---------------+------------------------------------------------------+
| JDF Product   | For a JDF workflow it can be required to define a    |
| Type          | Product type. The available options are based on the |
|               | JDF Specification.\                                  |
|               | \                                                    |
|               | The type \"Cover\" also has impact on the PrintVis   |
|               | Calculation Formula 107, which identifies if the     |
|               | calculation contains a cover.                        |
+---------------+------------------------------------------------------+
| Imposition    | This value will be transferred to the Imposition     |
| Type          | Type field of the Job Item, in case there is         |
|               | standard Imposition Type for this component type.    |
+---------------+------------------------------------------------------+
| Length Factor | This value is a multiplier for the final format      |
|               | (size). The value multiplied with the Length of the  |
|               | format code will populate the "Length" field of the  |
|               | job item.                                            |
|               |                                                      |
|               | Example: If the final format is 10x15 (width x       |
|               | length) and the Width Factor is 3 and Length factor  |
|               | is 2 the Width will be 30 (3 x 10) and the Length    |
|               | will be 30 (2 x 15). This means the final size for   |
|               | the imposition is 30x30.                             |
+---------------+------------------------------------------------------+
| Width Factor  | This value is a multiplier for the final format      |
|               | (size). The value multiplied with the Width of the   |
|               | format code will populate the "Width" field of the   |
|               | job item.                                            |
|               |                                                      |
|               | Example: If the final format is 10x15 (width x       |
|               | length) and the Width Factor is 3 and Length factor  |
|               | is 2 the Width will be 30 (3 x 10) and the Length    |
|               | will be 30 (2 x 15). This means the final size for   |
|               | the imposition is 30x30.                             |
+---------------+------------------------------------------------------+
| Imposition    | This value will be transferred to the Job Item field |
| Factor Length | \"Conjugate Length,\" to calculate the open format   |
|               | from the Job Item \"Length\" field.                  |
+---------------+------------------------------------------------------+
| Imposition    | This value will be transferred to the Job Item field |
| Factor Width  | \"Conjugate Width,\" to calculate the open format    |
|               | from the Job Item \"Width\" field.                   |
+---------------+------------------------------------------------------+
| Ignore        | If this field is enabled on the selected component   |
| Margins\      | type of the job item, all margins from the cost      |
| on 1-up       | center configuration (e.g. Gripper, pull-mark, color |
| layouts       | bar/strip) are set to =0, if the component only      |
|               | includes 1 up.\                                      |
|               | \                                                    |
|               | This will be used in case the printing is made on    |
|               | the final cut format, for example if finished        |
|               | products will be printed. This can be for example    |
|               | printing on envelopes, gift/greeting cards etc.      |
+---------------+------------------------------------------------------+
| Include in    | This Boolean field should be set = TRUE in case the  |
| Spine         | actual component should have impact on the spine     |
| Calculation   | thickness for the cover. Formulas 650/651 will       |
|               | include the paper thickness for those components.    |
+---------------+------------------------------------------------------+
| Include in    | Enable this field if the component is a part of the  |
| Hardcover     | spine for e.g. a hardcover book. Formula 652         |
| Spine         | calculates the spine thickness either with the paper |
| Calculation   | thickness of the components or the given values from |
|               | the spine type setup in the Job Item Formats.        |
+---------------+------------------------------------------------------+
|               |                                                      |
+---------------+------------------------------------------------------+
| Formula Spine | It is possible to select a formula to calculate the  |
| Thickness     | spine thickness of a perfect bound (or similar)      |
|               | cover. The value will be displayed in the field      |
|               | \"Spine Thickness\" on the Job Item, which is an     |
|               | editable field and will be also used for the         |
|               | imposition calculation for the open size of the      |
|               | cover.\                                              |
|               | \                                                    |
|               | This value should contain a factor on top of the     |
|               | pure paper thickness because a closed and folded     |
|               | product is thicker than just the paper.\             |
|               | PrintVis provides calculation formula 651 which add  |
|               | 8% to the net paper thickness of all components with |
|               | the setting \"Include in Spine Calculation\" = TRUE. |
|               | This is typically the spine for a softcover book or  |
|               | just the book block thickness for a hardcover book.\ |
|               | \                                                    |
|               | For Hardcover spine calculation formula 652 can be   |
|               | used. In the Job Item Format setup the components    |
|               | for the hardcover can be defined. The components can |
|               | be either calculated from the material thickness     |
|               | with the setting \"Include in Hardcover Spine        |
|               | Calculation\" = TRUE                                 |
+---------------+------------------------------------------------------+
| Formula Spine | It is possible to select a formula to calculate the  |
| Thickness Net | spine thickness of a perfect bound (or similar)      |
|               | cover.\                                              |
|               | The value will be displayed in the field \"Spine     |
|               | Thickness, Net\" on the Job Item. This value is only |
|               | for information.\                                    |
|               | PrintVis provides calculation formula 650 which      |
|               | gives the net paper thickness of all components with |
|               | the setting \"Include in Spine Calculation\" = TRUE. |
+---------------+------------------------------------------------------+

## Lists of Components

You are able to set up a combination of "Component Types" in the "PV
Component List." After setting up all components for a product, they can
be collected in the component list. When choosing this list on a new
sheet and expanding it, all required sheets/Job Items will be created.

This can be useful for a hardcover book that could contain for example:

-   Hardcover board

-   Hardcover cloth or paper covering

-   Dust Jacket

-   Front paper

-   Back paper

-   Text/body

For this follow the steps:

1.  Create all individual component types for a product.

2.  Create a list of components and assign all required components.\
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./assets/image3.png){width="6.5in"
    height="2.4784722222222224in"}\
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./assets/image4.png){width="6.5in"
    height="2.140277777777778in"}

3.  On the Job Card of a case, create a new sheet and select the list of
    components\
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./assets/image5.png){width="6.5in"
    height="1.5083333333333333in"}

4.  Click expand to create all required sheets. Result:\
    ![A screenshot of a computer AI-generated content may be
    incorrect.](./assets/image6.png){width="6.5in"
    height="2.370138888888889in"}

## Job Item Formats

On top of the product size (Final Format), it is possible to define
additional flaps or other areas by using the Job Item Format Setup and
assigning them to each component type. This can be relevant for
packaging products in defining areas for gussets, zippers, etc. With
this PrintVis is able to calculate the open size of the product for an
exact calculation of the required print substrate.

## Job Item Format Setup

Below we show a setup for flexible packaging production (stand up
pouches) or narrow web label production.

![Image](./assets/image7.png){width="6.5in"
height="3.611111111111111in"}

Fields

  -----------------------------------------------------------------------
  Code              Enter a code for this Job Item Format Setup
  ----------------- -----------------------------------------------------
  Description       Enter a description for this Job Item Format Setup

  Format type       Select the required format type from the options
                    list. See the format types description below.

  Factor            Enter a factor which will be the multiplier for the
                    given value.

  Blocked           If this field is enabled the \'\'Job Item Format
                    Setup\'\' is blocked from being used in the system.
  -----------------------------------------------------------------------

## Format Types

  -----------------------------------------------------------------------
  Depth             The given value will be multiplied with the factor
                    and added to the length of the product to calculate
                    the open size of the product on the print substrate.
  ----------------- -----------------------------------------------------
  Width             The given value will be multiplied with the factor
                    and added to the width of the product to calculate
                    the open size of the product on the print substrate.

  Minimum distance  This is the minimum distance between the items in the
  front             length/circumference for a die.\
                    This is used in the PrintVis Tools Selection as a
                    preset value and to store a user-modified value for
                    the actual sheet.

  Maximum distance  This is the maximum distance between the items in the
  front             length/circumference for a die.\
                    This is used in the PrintVis Tools Selection as a
                    preset value and to store a user-modified value for
                    the actual sheet.

  Distance across   This is the distance between the items in the width
                    for a die.\
                    This is used in the PrintVis Tools Selection as a
                    preset value and to store a user-modified value for
                    the actual sheet.

  Corner radius     This is the corner radius for a die.\
                    This is used in the PrintVis Tools Selection as a
                    preset value and to store a user-modified value for
                    the actual sheet.

  Spine Book block  Using this type it is possible to enter the book
                    block thickness for a cover component.\
                    \
                    If you leave the value = 0 on the component,
                    calculation formula 652 filters on the components
                    with \"Include in Spine Calculation = TRUE\" to
                    calculate the thickness.

  Spine cardboard   Using this type it is possible to enter the cardboard
                    thickness for a hardcover component.\
                    \
                    If you leave the value = 0 on the component,
                    calculation formula 652 filters on the components
                    with \"Cover material type= Spine cardboard\" to
                    calculate the thickness.

  Spine cover /     Using this type it is possible to enter the thickness
  cloth material    of cover cloth material for a hardcover.\
                    \
                    If you leave the value = 0 on the component,
                    calculation formula 652 filters on the components
                    with \"Cover material type= Spine cover / cloth
                    material\" to calculate the thickness.

  Spine front (end) Using this type it is possible to enter the thickness
  paper             for the end paper for a hardcover book.\
                    \
                    If you leave the value = 0 on the component,
                    calculation formula 652 filters on the components
                    with \"Cover material type= Spine front (end)
                    paper\" to calculate the thickness .

  Spine back (end)  Using this type it is possible to enter the thickness
  paper             for the end paper for a hardcover book.\
                    \
                    If you leave the value = 0 on the component,
                    calculation formula 652 filters on the components
                    with \"Cover material type= Spine back (end)
                    paper\" to calculate the thickness .

  Spine jacket      Using this type it is possible to enter the thickness
                    for jacket of a hardcover.\
                    \
                    If you leave the value = 0 on the component,
                    calculation formula 652 filters on the components
                    with \"Cover material type= Spine jacket\" to
                    calculate the thickness.

  Spine glued/thead Using this type it is possible to enter the cardboard
                    thickness for a hardcover component.\
                    \
                    If you leave the value = 0 on the component,
                    calculation formula 652 filters on the components
                    with \"Cover material type= Spine cover / cloth
                    material\".

  Spine per folding Using this type it is possible to enter a margin to
  sheet             be added to each folding sheet that is part of the
                    book block.\
                    \
                    Formula 652 adds this margin x no. of folding sheets
                    to be included into the spine. Typically a folded
                    sheet is thicker than just the paper thickness after
                    folding.

  Spine side glue   Using this type it is possible to enter a margin to
                    be added to spine thickness in case there is side
                    glue.\
                    \
                    Formula 652 adds this margin to be included into the
                    spine.
  -----------------------------------------------------------------------

## Example for a stand-up pouch with a zipper

A stand-up pouch with a zipper needs on top of the final size extra
material for the 

-   Bottom gusset

    -   BG setup 

        -   Format type = Depth

        -   Factor = 1

-   2 side gussets

    -   SG setup 

        -   Format type = Width

        -   Factor = 2

-   Zipper

    -   Zipper setup 

        -   Format type = Depth

        -   Factor = 2

Value for the actual Component type:

![Image](./assets/image8.png){width="6.5in"
height="4.5055555555555555in"}

![A screenshot of a calendar AI-generated content may be
incorrect.](./assets/image9.png){width="6.5in"
height="1.8493055555555555in"}

**Result in Width and Length on Job item:**

![Image](./assets/image10.png){width="6.5in"
height="1.5104166666666667in"}

Length is calculated: 

-   (\"Job Item Format Length\" x \"Length factor\") + (Bottom Gusset
    Value+ Factor) + (Zipper Value+ Factor)\
    (10.5 x 2 = 21)+( 1 x 1 = 1) + (0.75 x 2 = 1.5) = 23.5

Width is calculated: 

-   (\"Job Item Format Width\" x \"Length factor (if not setup, value
    =1)\") + (Side Gusset Value+ Factor)\
    (10.5 x 1 = 10.5)+( 1 x 2 = 2) = 12.5

## Example for the Tools Selection

Component type = TOOL

![Image](./assets/image11.png){width="6.5in"
height="1.7333333333333334in"}

Values:

![Image](./assets/image12.png){width="6.5in" height="1.85625in"}

![Image](./assets/image13.png){width="6.5in"
height="2.189583333333333in"}

After editing the values and selecting a tool combination, the new
values are stored on the Job Item formats for this sheet.

![Image](./assets/image14.png){width="6.5in"
height="2.1506944444444445in"}

## Example for a hardcover book

For hardcover books there are several parts that must be included into
the calculation for the spine thickness. Calculation formula 652 is
calculating the total spine thickness from these values.

Step 1: Setup Job Item Formats

Description below explains how it calculates with formula 652

![Image](./assets/image15.png){width="6.5in"
height="2.834722222222222in"}

Step 2: Setup the required Component Types

Setup a Component Type for each component that should be included in the
hardcover spine thickness. Make sure to set the required Cover material
type.

![Image](./assets/image16.png){width="6.5in"
height="5.278472222222222in"}

Step3: Setup on the components that represents/contains the spine
formula 652 in the spine thickness field.

![Image](./assets/image17.png){width="6.5in"
height="5.607638888888889in"}

Step 4: Setup on the components that represents/contains the spine,
values for the spine elements on action Job Item Formats. Keep the value
= 0 if it should be calculated from a component that must be created in
a case as job item(s). 

![Image](./assets/image18.png){width="6.5in"
height="3.3027777777777776in"}

Step 5:

Create you estimate with the components for your book.

![Image](./assets/image19.png){width="6.5in"
height="4.311111111111111in"}

Step 6:

Edit the values if required. It is possible to lookup and adjust the
values with the lookup in the spine thickness field.

![Image](./assets/image20.png){width="6.5in"
height="1.9881944444444444in"}

Adjust the values as required. It is possible to personalize the page
for the ability to edit the factor value which is most probably not
needed for the estimator/CSR. The changes are for the current job item
only.

![Image](./assets/image21.png){width="6.5in"
height="2.8027777777777776in"}

The Spine Thickness value on the job item will be recalculated
accordingly.
