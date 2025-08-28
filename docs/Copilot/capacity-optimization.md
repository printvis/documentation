# Capacity Optimization (Public Preview)

Capacity Optimization is a Copilot assisted planning tool to help planners balance workload across capacity units with capacity shift setup. This is done by automatically optimizing and shifting planning units and placing them into a planning simulation.

## Installation

To begin using this public preview feature, install the [PrintVis Copilot app](https://) from AppSource.


## Accessing Capacity Optimization

1. Open the **Planning Board** in PrintVis.  
2. Select the Copilot icon in the upper left corner of the menu.  
3. Choose **Optimize**.  


## Running the Optimization

1. Select the primary capacity unit. This list will show the first unit in the capacity shift value on capacity units.
2. Enter the start date that you want Copilot to use as the scheduling start date.
3. The end date will automatically fill in 3 days after the start date. You can adjust the end date but no more than 5 days total.
4. Select an optimization option if you want Copilot to consider one of the available options when determining how to plan.
   - No optimization: use only the earliest start / latest end date and additional notes for optimization.
   - Paper item no.: for sheet specific planning units, use the paper item no.
   - Paper quality: for sheet specific planning units, use the paper quality.
   - Paper weight: for sheet specific planning units, use the paper weight.
   - Sheet format: for sheet specific planning units, use the sheet format.
   - No of pages: for sheet specific planning units, use the number of pages value.
5. Enter additional notes Copilot should consider when optimizing the planning units such as "avoid paper changes" or "there is only 1 operator for the 3 machines"
6. A list of planning units that will be passed to Copilot for optimization will be listed.


When you click Optimize:

1. Copilot evaluates the capacity schedule, capacity blockings, planning units, and instructions provided.  
2. It will return a list of planning units it was unable to plan.


## Reviewing Suggestions

1. Clicking Load Simulation will add the planning units it was able to plan to the planning board in simulation mode.
2. Each planning unit will have an added tooltip to give the Copilot explanation for why it placed that unit in that specific space.
3. Each planning unit can be adjusted on the planning board manually by the planner.

## Applying the Results

Once satisfied with the optimization suggestions:

1. Select **Apply Simulation** in the menu.  
2. The planning units from the simulation will be applied to the live schedule and the planning board will refresh.

If you want to discard the Copilot simulation, click Reload in the menu or simply exit the planning board.


## Tips and Notes

- Capacity Optimization works best when resource calendars and shop calendars are up to date.  
- Use this tool in combination with **Auto Scheduling** for maximum flexibility.  
- You can re-run optimization at any time if production priorities change.