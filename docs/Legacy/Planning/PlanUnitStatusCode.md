# Planning Unit Status Code

## Introduction

It is possible to change the status code automatically based on Planning Unit setup. This means that when a machine operator completes a planning unit, the status code changes to the next status as defined by the scheduling/planning.

## Example

When a CTP employee finalizes the Planning Unit "CTP plate production," the status changes to **PROD**.

![Status Code Field at Planning Unit Setup 1.jpg](./assets/Status Code Field at Planning Unit Setup 1.jpg)

You can use the **Status Code** field to change the status if all Calculation Units at this Planning Unit are marked as "Completed" from the Shop Floor, Production Plan, or Job Costing Journal. The next status will be determined in the following sequence:

<ol>
  <li>
    A planning unit line with a status code assigned that has a higher sorting order than the current one.
    <ul>
      <li>The next status to change to is taken from that planning unit.</li>
    </ul>
  </li>
  <li>
    If no more planning units exist, PrintVis attempts to find the next status code by filtering on:
    <ul>
      <li>Sorting must be higher than the actual status code</li>
      <li>Status code is set to "Production Ended = True"</li>
      <li>If no status code can be found, proceed to step 3.</li>
    </ul>
  </li>
  <li>
    The next status code is taken from the "Responsibility Areas" setup.
  </li>
  <li>
    If no next status is set up in the Responsibility Areas:
    <ul>
      <li>The next status code is taken from the "Status Code" setup.</li>
    </ul>
  </li>
</ol>

## Planning Unit Setup

![Status Code Field at Planning Unit Setup 2.jpg](./assets/Status Code Field at Planning Unit Setup 2.jpg)

### Planning

![Status Code Field at Planning Unit Setup 3.jpg](./assets/Status Code Field at Planning Unit Setup 3.jpg)

If Capacity Units 3000 or 3400 are marked as completed, the status code changes to **PLATE PRODUCTION**. The status will change after the first planning line is completed.

PrintVis does not wait until all tasks from this unit are finished. For example, if the plates are ready, printing can already begin, even if not all plates for all sheets are completed.

**Note:** If you want to use this function, the setup of the next Status Code field at the Status Code setup and Responsibility Areas will be overridden if planning is existing! See the sequence description above!
