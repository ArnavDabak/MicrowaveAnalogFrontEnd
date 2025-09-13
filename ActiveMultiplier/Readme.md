# Active Multiplier

## Introduction
- Using the nonlinearity of the FET for frequency multiplication
- Here I am simulating a compressed class A Active Frequency Multiplier 
- First I am determining the cut off frequency of the Transistor used and then simulating a Active multiplier using a Harmonic Balance Testbench setup

## Simulation Setup
The simulation setup for the Active Multiplier includes the following components:
1. **Schematic Design**
    ![Active Multiplier](images/ActiveMultiplier_HB_Testbench.png)
2. **Testbenches**:
   - **DC Operation Simulation**: To determine the operating point of the transistor
    ![DC Simulation Testbench](images/DC_testbench_setup.png)
   - **Cutoff Frequency Test**: To determine cutoff frequency of the transistor
    ![Cutoff frequency TB](images/Cutoff_freq_testbench.png)


## Results
The simulation results include:
1. **DC Operation**:
    ![DC Simulation](images/DC_operation_simulation.png)
    VGS=2V & VDS=2.5V
2. **Cutoff Frequency**:
    ![Cutoff frequency](images/cutoff_frequency.png)
3. **Harmonic Balance**: We can observe a range of frequencies generated at the output
   ![HB Output](images/ActiveMultiplierOutput_SingletoneHBtest.png)
