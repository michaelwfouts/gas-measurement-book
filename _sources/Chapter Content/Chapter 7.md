# Chapter 7: Instrumentation

## Instrumentation

While this book has gone over the math of gas measurement, it has yet to talk about how we get the data for these calculations.  Accurate measurement of natural gas relies on specialized instrumentation that can precisely quantify flow rates, pressures, temperatures, and gas composition.  This chapter focuses on each of these variables and discusses the instrumentation used to measure them.

## Meter Run

To measure the four variables to calculate the amount of energy passing through the pipeline, a pipeline configuration known as a meter run is typically constructed.  The design of the meter run is built by engineers to be compliant with applicable standards, typically based on the meter, such as AGA 3 for orifice meters and AGA 9 for ultrasonic meters.  This consists of a meter with two straight sections of pipe on each end.  On the downstream side, olets are put into place to allow taps for the temperature setup and gas quality probe.  Pressure can also be taken downstream or from a tap on the meter body itself.

## Temperature

To measure temperature, a three-piece setup is used.  This consists of:

1. RTD (Resistance Temperature Detector) - This is the sensing element in the setup that physically measures the temperature by using the property that metal's electric resistance changes with temperature.
2. Transmitter - Supplies excitation to the RTD.  Also generates a signal from that RTD that can be read by a computer.
3. Thermowell - This is a solid piece of metal that acts as the pressure-containing piece of equipment between the pressurized natural gas and the atmosphere.

## Pressure

Pressure is typically measured by an all-in-one device that has a single tap for pressure.  However, it has an additional component that, while not required, is typically added to most setups known as a manifold.  For a pressure transmitter, this is a two-valve manifold containing an isolation and bleed valve. An example can be seen in the figure below.

```{figure} ../Assets/two-valve-manifold.png
---
name: two-valve-manifold
---
Two Valve Manifold Diagram
```

Under normal operations, the isolation valve is open and the bleed valve is closed, allowing the transmitter to read to process pressure.  The addition of the valve allows for easy testing though without blowing down the entire meter run.  To do this, simply close the isolation valve, open the bleed valve to bleed off the trapped gas to atmosphere, and hook your testing equipment up to the bleed valve.  Once done, close the bleed valve and open the isolation valve to return the transmitter to normal operations.

## Meter (Volume)

Meters will be extensively covered in Chapter 8.

## Gas Chromatograph (Gas Quality)

Gas Chromatographs are covered in Chapter 5.

## Transmitter Communication

We know what devices measure the needed variables to calculate the total energy content in the pipelines; however, the calculations are not done by hand once the data is collected.  Rather, computers do these mathematical calculations for us.  But how do the transmitters communicate these values to a computer?

The industry standard for instrumentation communication for pressure and temperature transmitters is a technology known as 4-20 mA current loops.  The transmitters are set up in such a fashion that they have an operating range.  When the lowest value in the range is measured, the transmitter feeds 4 mA to the computer.  When the highest value in the range is measured, the transmitter feeds a 20 mA current to the computer.  For any value in between, the value of the current loop is linearly proportional to the value in the transmitter's operating range.

This operating range gets a special name for the transmitter called the span.  The span is typically described by the minimum and maximum value of the transmitter.  To convert between the current loop output and the transmitter reading, linear interpolation (a mathematical technique) can be applied to get the following equation.

\begin{gather*}
\\
\frac{mA \: Reading - Low \: mA}{High \: mA - Low \: mA} = \frac{Transmitter \: Reading - Low \: Span}{High \: Span - Low \: Span} \\
\end{gather*} 

However, since we are specifically dealing with a 4-20 mA current loop, this equation can be simplified since the Low mA and High mA values on the left-hand side will always be constants.

\begin{gather*}
\\
\frac{mA \: Reading - 4 mA}{20 mA - 4 mA} = \frac{Transmitter \: Reading - Low \: Span}{High \: Span - Low \: Span} \\
or \\
\frac{mA \: Reading - 4 mA}{16 mA} = \frac{Transmitter \: Reading - Low \: Span}{High \: Span - Low \: Span} \\
\end{gather*}

\begin{align*}
& where: \\
  & \qquad mA \: Reading = mA \: value \: being \: sent \: to \: the \: computer \: (mA)\\
  & \qquad Transmitter \: Reading = Transmitter \: value \: interpreted \: by \: computer (units \: depend \: on \: variable \: being \: measured)\\
  & \qquad Low \: Span = Lowest \: value \: transmitter \: can \: measure \: (units \: depend \: on \: variable \: being \: measured)\\
  & \qquad High \: Span = Highest \: value \: transmitter \: can \: measure \: (units \: depend \: on \: variable \: being \: measured)\\
\end{align*}

```{note}
Zero is not the lowest value for mA because if there is a power failure (0 mA), you would not know if you are just reading at the bottom value of your device or if there is a power failure.  This is why if there is a power failure, the computer will interpret it as being much outside the range of the device.
```

### Example (Basic mA Signal Reading Calculation)  
```{admonition} **Problem:**  
You are setting up a temperature transmitter that is spanned from -40°F to 140°F.  The transmitter is currently reading 15°F. What should the mA output of the transmitter be? 
```

```{admonition} **Solution:**  
:class: tip, dropdown  
This problem can be simply solved using the equation above knowing the following values.

\begin{gather*}
mA \: Reading = ? \\
Transmitter \: Reading = 15°F \\
Low \: Span = -40°F \\
High \: Span = 140°F \\
\end{gather*}

\begin{gather*}
\\
\frac{mA \: Reading - 4 mA}{16 mA} = \frac{Transmitter \: Reading - Low \: Span}{High \: Span - Low \: Span} \\
\\
\frac{mA \: Reading - 4 mA}{16 mA} = \frac{15°F - -40°F}{140°F - -40°F} \\
\\
mA \: Reading = 8.889 mA \approx \textbf{8.89 mA}
\end{gather*}
``` 

### Example (Basic Transmitter Reading Calculation)  
```{admonition} **Problem:**  
A pressure transmitter spanned from 0-1000 psig has a 4-20 mA current loop that is outputting 17mA.  What pressure does this indicate?
```

```{admonition} **Solution:**  
:class: tip, dropdown  
This problem can be simply solved using the equation above knowing the following values.

\begin{gather*}
Transmitter \: Reading = ? \\
mA \: Reading = 17mA \\
Low \: Span = 0 \: psig \\
High \: Span = 1000 \: psig \\
\end{gather*}

\begin{gather*}
\\
\frac{mA \: Reading - 4 mA}{16 mA} = \frac{Transmitter \: Reading - Low \: Span}{High \: Span - Low \: Span} \\
\\
\frac{17 mA - 4 mA}{16 mA} = \frac{Transmitter \: Reading - 0 \: psig}{1000 \: psig - 0 \: psig} \\
\\
Transmitter \: Reading = 812.5 \: psig \approx \textbf{813 \: psig}
\end{gather*}
``` 

## Questions
1. What is the pressure reading on a static pressure transmitter that is spanned from 0 to 500 psig and has a 4-20 mA current loop currently reading 15 mA?

2. What is the temperature reading on a temperature transmitter that is spanned from -20 to 140°F and has a 4-20 mA current loop currently reading 6 mA?

3. A rotary meter was operating at 100 psig and 90°F.  From reading the index, you gather that 22,300 actual cubic feet have flown through the meter during a month's time.
    a. How much gas in standard cubic feet has flown through this meter?  Ignore supercompressibility and assume you are operating in the Appalachian Basin Region.
    b. During your testing, you found that the pressure transmitter was reading high by 0.5mA on it's 4-20mA current loop (example, it was reading 8 mA when in reality it should have been 7.5mA).  If the pressure that was read (the incorrect pressure) was 100 psig for the entire month on a static pressure transmitter spanned from 0-500 psig, what is the new volume in standard cubic feet once the adjustment for the static pressure issue is taken into consideration?

4. A rotary meter is has a pressure transmitter spanned from 0 to 1000 psig and is currently reading 15.2 mA on its 4-20 circuit.  It also has a temperature transmitter that is spanned from 0-150 °F and is currently reading 9.7 mA.  From reading the index over a 24 hour period, you find that when you first read the index, it has an accumulated volume of 150,423 ACF and 219,847 ACF when you return later.  The gas chromatograph tells you that the energy density is 1078 BTU/SCF. How much energy in dekatherms has flown through this meter?  Please make sure to factor in supercompressibility.  Assume that z is 1.128 and you are operating in the Appalachian Basin.

5. Draw a two-valve manifold diagram for a Static Pressure Transmitter and label the isolation and bleed valves.  Also, explain what the proper procedure would be for operating this when you want to test the transmitter.