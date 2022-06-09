# FaultClf_Dataset_SmartGrids_withRE

Information about Dataset:

This dataset is extracted from IEEE-13 node test feeder with renewable energy (RE) such as  wind turbin, solar energy, and energy storage connected to the network. A distribution network operating at 4.16 kV simulated in MATLAB Simulink environments. The dataset is organized in two main sub-folders:

1. RawTimeSeriesDate: There are two sub-folders for raw time-series data one contains raw faulty data and the other health data: 
a. FaultySignal_withRE: For fault simulation, we divided the network into four zones (red boxes) as shown in Figure 1. We injected 11 fault types (AG, BG, CG, AB, AC, BC, ABG, ACG, BCG, ABC, ABCG) with 22 different resistances for each type of faults to these four critical zones adjacent to load flow buses number 671, 633, 675 and 680 in for the whole simulation time was t = [0.0 - 0.022]. Each fault with every resistances have been applied at a certain start time t= 0.01 and revoked at time t= 0.02, so t_f = [0.01-0.02] represents the faulty duration, while t_h = [0-0.01] represents the healthy (non-faulty) time period. This folder contains three .csv files that include phase A, B, and C voltage measurements.

<img width="497" alt="Screen Shot 2022-05-28 at 5 42 14 PM" src="https://user-images.githubusercontent.com/38736959/172878749-e7b9beaf-7b96-4d4e-8ef5-46a95785eba2.png">
