# 3 - Ultrasonic Meters
## Introduction to Ultrasonic Meters

Ultrasonic meters represent a significant advancement in flow measurement technologies.  Being a digital first type of measurement, it allows for several advantages over mechanical types of meters (such as positive displacement and turbine meters). Ultrasonic flow meters measure flow rate by sending ultrasonic sound waves diagonally across a pipe through the flowing gas. This creates a small time difference between the upstream and downstream signals that indicates flow velocity. They work by measuring the transmission time difference between upstream and downstream ultrasonic pulses. This transit time difference is proportional to flow velocity. The cross-sectional area of the pipe yields the volumetric flow rate.  A visualization and more detailed explanation can be found at the video below:

https://www.youtube.com/watch?v=Bx2RnrfLkQg

### Advantages of Ultrasonic Meters

Ultrasonic meters are one of the most technologically advanced methods to measure natural gas.  While this typically comes with a heavy price tag, engineering and design teams will often consider the price tag worth it for high volume applications.  The two largest advantages of Ultrasonic Meters are: 

1. <ins>Accuracy and Reliability</ins>: Ultrasonic meters provide high-precision, high-accuracy measurements of the gas volume. This ensures that billing is based on reliable data.  For comparison, an orifice meter's uncertainty is typically around ±2% while an ultrasonic meter's uncertainty is about ±0.25%, an 8 times increase in precision. The absence of moving parts reduces wear and tear, further enhancing measurement reliability over time.

2. <ins>Operational Diagnostics</ins>: Ultrasonic meters are equipped with sophisticated diagnostics that monitor the meter's performance and the condition of the gas flow. This capability enables early detection of measurement issues, flow disturbances, or maintenance needs, preventing potential problems before they impact operations. These diagnostics can even be sent via communication networks back to data centers meaning analytics and monitoring can be inspected remotely on the meter.

## Meter Diagnostics

Understanding the specific components of an ultrasonic meter maintenance report is crucial for ensuring the meter operates efficiently and accurately.  Below are some of the critical metrics that are used to evaluate the meter's performance:

1. <ins>Velocity</ins>:
This measures the flow velocity of the gas in each of the meter's paths. By analyzing the velocity across all paths, operators can ensure the meter is accurately capturing the flow's behavior and characteristics. Discrepancies in velocities across paths could highlight flow disturbances, asymmetrical flow profiles, or potential inaccuracies in the meter's flow calculations.

2. <ins>Profile</ins>:
The profile refers to the velocity profile of the gas flow through the meter. It provides insights into how uniformly the gas is flowing across the cross-section of the pipe. A uniform flow profile ensures that the meter's calculations are accurate. Deviations in the flow profile can indicate issues such as flow disturbances or obstructions that might affect the meter's accuracy.

3. <ins>Symmetry</ins>:
Symmetry is related to the profile and measures the balance of the flow's velocity profile between the upstream and downstream paths. Ideal symmetry means that the flow characteristics are consistent in both directions, which is crucial for the differential time measurement principle ultrasonic meters use. Asymmetry may suggest installation issues, flow disturbances, or physical obstructions that could skew measurements.

4. <ins>SOS (Speed of Sound)</ins>:
The speed of sound (SOS) in the gas is a fundamental parameter that ultrasonic meters use to calculate flow rate. It can be influenced by the gas composition, temperature, and pressure. Monitoring SOS helps in verifying the gas properties assumed during flow rate calculations. Significant deviations from expected SOS values could indicate changes in gas composition or other conditions affecting the meter's accuracy.

5. <ins>Gain</ins>:
Gain refers to the strength of the ultrasonic signal received after it travels through the gas medium. Each path in the meter has its own gain setting, ensuring that signals are detectable over the noise. Monitoring the gain levels for all paths helps identify issues such as signal attenuation due to fouling, corrosion, or changes in the gas composition. Consistent and appropriate gain levels are crucial for the meter's ability to accurately detect and measure the transit times of ultrasonic pulses.

6. <ins>Performance</ins>:
Performance is a measurement of the number of pulses that are read by a transducer per measurement.  For a given velocity data point, the ultrasonic meter will measure the velocity via ultrasonic pings multiple times and then average the velocities to give the single velocity data point.  For example, if the transducers send 20 pings per measurement, but the receiving transducer only hears 19 of them, the performance will be 95%.  Typically, a performance above 90% is considered a healthy for a meter.

7. <ins>SNR (Signal to Noise Ratio)</ins>:
Signal to noise ratio (SNR) measures the clarity and strength of the ultrasonic signal as it travels across the gas compared to the background noise within the system. A high SNR indicates that the signal is much stronger than the noise, which is crucial for an accurate flow measurement and healthy meter.

8. <ins>Turbulence</ins>:
Turbulence refers to unsteady vortices that appear in the meter.  Typically, flow in the meter tube is considered "Fully Developed" meaning that the flow velocity profile follows a bullet shape.  This should largely be taken into account via installation design by engineering for normal conditions.  However, a typical operating events (like blockages in the flow conditioner) can create turbulence issues inside the meter.

## Lab Instructions:
***NOTE:*** These lab instructions are specific to a FLOWSIC 600 Meter.  However, the general outline of the lab can still be followed for any Ultrasonic Meter.

1. Connect to the meter using the FLOWgate Software.  Connection types can greatly vary; however, for this specific lab, the connection information is as follows:  
    a. Serial Connection using RS-485 to USB Adapter  
    b. SICK MODBUS ASCII Protocol  
    c. 57600 Baudrate  
    d. Address 1  
2. Sign in as an Operator with no password.  
3. Collect the Maintenance Report by selecting the clipboard on the top bar and following the on screen instructions  
4. Collect the Diagnostic Session by selecting the cross on the top bar and following the on screen instructions

## Questions
1. When testing an Ultrasonic Meter, what two reports are typically collected for a SICK meter? What type of information does each of these reports contain?

2. Why is the typical testing of an ultrasonic meter much simpler than testing a positive displacement or turbine meter?

3. Using the maintenance report collected, please report what the following values are and why these values are important for checking the meter's health or to operations.  
    a. Velocity of Gas or VOG (all paths)  
    b. Profile  
    c. Symmetry  
    d. SOS (all paths)  
    e. Gain (all paths)  
    f. Performance (all paths)  
    g. Signal to Noise Ratio or SNR (all transducers)  
    h. Turbulence (all paths)  
    i. Actual Flowrate (ACFH)  