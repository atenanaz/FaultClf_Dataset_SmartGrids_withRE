# FaultClf_Dataset_SmartGrids_withRE

Information about Dataset:

This dataset is extracted from IEEE-13 node test feeder with renewable energy (RE) such as  wind turbin, solar energy, and energy storage connected to the network. A distribution network operating at 4.16 kV simulated in MATLAB Simulink environments. The dataset is organized in two main sub-folders:

1. RawTimeSeriesDate: There are two sub-folders for raw time-series data one contains raw faulty data and the other health data: 
a. FaultySignal_withRE: For fault simulation, we divided the network into four zones (red boxes) as shown in Figure 1. We injected 11 fault types (AG, BG, CG, AB, AC, BC, ABG, ACG, BCG, ABC, ABCG) with 22 different resistances for each type of faults to these four critical zones adjacent to load flow buses number 671, 633, 675 and 680 in for the whole simulation time was t = [0.0 - 0.022]. Each fault with every resistances have been applied at a certain start time t= 0.01 and revoked at time t= 0.02, so t_f = [0.01-0.02] represents the faulty duration, while t_h = [0-0.01] represents the healthy (non-faulty) time period. This folder contains three .csv files that include phase A, B, and C voltage measurements.

<img width="497" alt="Screen Shot 2022-05-28 at 5 42 14 PM" src="https://user-images.githubusercontent.com/38736959/172878749-e7b9beaf-7b96-4d4e-8ef5-46a95785eba2.png">


b. HealthySignal_withRE: For Healthy data, we got raw healthy signals for 88 line lengths by measuring from four locations and for three phases. This folder contains three .xlsx files that include phase A, B, and C voltage measurements. The whole simulation time was t = [0.0 - 0.022]. The number of samples created by simulation for both faulty and healthy signals with renewable energies is demonstrated in the figure below.

![Design of dataset](https://user-images.githubusercontent.com/38736959/172881783-64986151-3951-461b-b28a-4f8ce62dc346.png)


2.FeatureData: includes features from three domains: time, frequency (discrete Fourier transform DFT), and Discrete wavelet transform (DWT).
For feature representation, we investigate the impact of several statistical aggregation functions computing the n-th moment of the probability distribution functions (PDFs) (n \ in [1,4]) inculde (mean, standard deviation, skewness, kurtosis) together with the energy and maximum level of the signals for three domains as an input of classifiers. In total, 48 features are extracted: 6 features from time-domain, 6 features from DFT, and 36 features from DWT (5 levels of decomposition + 1 level of approximation). In this regard, for DWT 6 features are multiplied by 6. In this folder there are two folders related to features for faulty and healthy signals.

a. Features_faultySignal: For faulty data, there are three .csv files that each include 48 features and labels with 3872 samples for phases A, B, and C, respectively. Furthermore, there are two labels, “locLabel” and “faultLabel” and information about resistance and where the measurements are done in columns by headers “resistance” and “measloc”.

b. Features_healthySignal: For healthy data, there are three .csv files that each include 48 features and labels with 352 samples for phases A, B, and C, respectively. Furthermore, there are information about line length and where the measurements are done in columns by headers “lineLength” and “measloc”.

The diagram of folders is shown in the following:


