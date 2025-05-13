# How to use more printing machines on one sheet

We are often asked, "How to define one calculation unit (printing machine) for the front and another one for the back?" 

For example, the front could be printed with varnishing on one machine, and the back could be printed with perforating on another.

## Steps to Define Calculation Units

### 1. Define the Calculation Units

**For the Front Printing:**
- **Select the Machine:** Choose the printing machine that will handle the front side. This machine might also include varnishing.
- **Set Up the Calculation Unit:** Create or select a calculation unit for this machine. Ensure it includes any additional processes like varnishing or pop-ups.

**For the Back Printing:**
- **Select the Machine:** Choose a different machine for printing the back side. This machine might include perforating or other processes.
- **Set Up the Calculation Unit:** Create or select a calculation unit for this machine. This unit should handle the back printing processes.

### 2. Adjust Paper Calculation

- **Paper for Front Machine:** Ensure that the paper unit for the front machine is set up correctly and includes the necessary paper calculation.
- **Paper for Back Machine:** For the back printing machine, create a paper unit where the value is set to Zero. This avoids double-counting the paper cost for the second print run.

### 3. Configure the Job Item

- **Front Side Setup:** Assign the front printing machine and its associated calculation unit to the first part of the job.
- **Back Side Setup:** Assign the back printing machine and its paper-free calculation unit to the second part of the job.

### 4. Manage Imposition and Layout

- Ensure that the imposition and layout are set up correctly so that the front and back sides are aligned as required.

### 5. Verify the Results

- **Check Cost Calculations:** Verify that the paper costs are only calculated for the front machine and not for the back machine.
- **Review the Estimation:** Make sure the front and back printing processes are correctly reflected in the job estimation.

By following these steps, you can effectively manage different machines and processes for printing the front and back of a job while ensuring accurate cost calculations.
