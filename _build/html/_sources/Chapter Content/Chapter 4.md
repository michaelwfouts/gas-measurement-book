# Chapter 4: The Basic Math of Gas Measurement

## The Combined Gas Law

This book has already made the case for why natural gas needs to be measured and it's given the appropriate background information to start talking about the math behind gas measurement.  The main equation used in gas measurement is called the combined gas law, which joins together two other gas laws - Boyle's law and Charles' law.

Boyle's law describes the relationship between a gas's pressure and volume at constant temperature. It states that pressure and volume are inversely proportional. As volume increases, pressure decreases proportionally, and vice versa.

Charles' law describes the relationship between a gas's volume and temperature at constant pressure. It states that volume and temperature are directly proportional. As temperature increases, volume increases proportionally, and vice versa.

The combined gas law integrates these two laws.  An easy way of thinking about the combined gas law is that it states for a <u>constant</u> number of molecules of gas, the pressure, temperature, and actual occupied volume can be modeled between a known state (referred to by subscript 1) and an unknown state (referred to by subscript 2) as shown below.

\begin{gather*}
\\
\frac{P_1 V_1}{T_1} = \frac{P_2 V_2}{T_2} 
\\
\end{gather*} 

An important fact to note about the combined gas law is that when using it, all values <u>must be in absolute units</u>.  If not, this can create large discrepancies in calculated values.

### Example (Combined Gas Law)  
```{admonition} **Problem:**  
Assume you have a volume of 10 ft<sup>3</sup> of gas at 62°F and 35 psig.  How much space, in ACF, would this amount of gas take up if it's conditions were changed to 75°F and 62 psig? Assume you are operating in the Appalachian Basin Region.
```

```{admonition} **Solution:**  
:class: tip, dropdown  
Reading the question, we know that we are searching for the new volume of the gas.  Using the combined gas law, we know we can solve for this.  Lets first begin by writing out all of our known values.

\begin{gather*}
V_1 = 10ft^3 \\

T_1 = 62°F \\

P_1 = 35 psig
\end{gather*} 

\begin{gather*}
V_2 = ? \\

T_2 = 75°F \\

P_2 = 62 psig
\end{gather*} 

However, we can't directly plug these numbers into the combined gas equation because not all of them are in absolute units.  We need to convert the temperatures into Rankine by adding 459.67 and convert the psig values into psia by adding atmospheric pressure, which happens to be 14.4 psia since we are operating in the Appalachian Basin Region.

\begin{gather*}
T_1 = 62°F + 459.67 = 521.67°R \\

P_1 = 35 psig + 14.4 = 49.4 psia
\end{gather*} 

\begin{gather*}
T_2 = 75°F + 459.67 = 534.67°R \\

P_2 = 62 psig + 14.4 = 76.4 psia
\end{gather*} 

Now that we have all the variables converted into the correct units, we can solve for $V_2$.

\begin{gather*}
\frac{P_1 V_1}{T_1} = \frac{P_2 V_2}{T_2} \\

\frac{49.4 psia \cdot 10ft^3}{521.67°R} = \frac{76.4 psia \cdot V_2}{534.67°R} \\

0.94696 = 0.14289V_2 \\

V_2 = 6.627 ACF \approx \textbf{6.63 ACF}
\end{gather*} 
```

```{admonition} **Solving for Temperature and Pressure**
:class: note
While this example uses the combined gas law to solve for the volume, the combined gas law can also be rearranged to solve for the temperature and pressure as well.  So long as 5 of the 6 values are given, the 6th value can be solved for.
```

## Standard Cubic Feet

The standard cubic foot (SCF) was originally established to compare gas volumes regardless of temperature and pressure. By defining a standard volume of one cubic foot at 60°F and 14.73 psia, the SCF provides a fixed reference point. Gas volume measurements can be converted to standard cubic feet based on the measured temperature and pressure.  This allows comparison of gas volumes delivered and produced even if the conditions differ. The SCF makes it possible to determine if gas flow rates and totals align with contractual amounts. It is indispensable for custody transfer, billing, and reconciliation in the natural gas industry.

Because the temperature and pressure are held constant for an SCF, it allows for an SCF to be an analog for the number of moles contained in the gas.  This is typically not straightforward to see, but can be easily derived using the ideal gas law.  Because the ideal gas law isn't used extensively in the rest of this book, it will only briefly be covered here. The ideal gas law can be written as:

\begin{gather*}
PV = nRT \\
\end{gather*} 

\begin{align*}
& where: \\
  & \qquad P = Pressure \: (psia)\\
  & \qquad V = Volume \: (SCF)\\
  & \qquad n = moles \: (number \: of \: molecules) \\
  & \qquad R = Ideal \: Gas \: Constant \: (\frac{psia \cdot ft^3}{mol \cdot °R}) \\
  & \qquad T = Temperature \: (°R)\\
\end{align*}

Rearranging the equation, we get:

\begin{gather*} 
\\
n = \frac{P}{RT} \cdot V
\end{gather*} 

Since the pressure, temperature, and ideal gas constant are all constants, we can simplify this entire term into a single constant.  For this book, we'll call it C.

\begin{gather*} 
n = CV
\end{gather*} 

This equation directly relates the number of molecules (moles) we are trying to count with the volume in standard cubic feet times a constant.  This is a critical point to note that the SCF is indeed counting the number of molecules and not an actual volume.

### Example (Standard Cubic Feet)  
```{admonition} **Problem:**  
Assume you have a volume of 125 ft<sup>3</sup> of gas at 30°F and 752 psig.  How many standard cubic feet is this? Assume you are operating in the Appalachian Basin Region.
```

```{admonition} **Solution:**  
:class: tip, dropdown  
If this is the first time you are solving for SCF, you may think that there is not enough information to solve the problem.  However, if you remember that to calculate the SCF, the pressure must be assumed as 14.73 psia and the temperature must be 60°F mentioned above, the problem can now be solved for similar to the previous example.

\begin{gather*}
V_1 = 125ft^3 \\

T_1 = 30°F = 487.67°R \\

P_1 = 752 psig = 766.4 psia
\end{gather*} 

\begin{gather*}
V_2 = ? \\

T_2 = 60°F = 519.67°R \\

P_2 = 14.73 psia
\end{gather*} 

Knowing all the needed variables, we can solve for $V_2$.

\begin{gather*}
\frac{P_1 V_1}{T_1} = \frac{P_2 V_2}{T_2} \\

\frac{766.4 psia \cdot 125ft^3}{487.67°R} = \frac{14.73 psia \cdot V_2}{519.67°R} \\

V_2 = 6902 SCF \approx \textbf{6900 SCF}
\end{gather*} 
```

## Summary
Focusing on the math, it is easy to lose perspective on why we are doing this.  It was previously said that transactions happen according to the number of molecules that are transported and what those molecules are.  This chapter has shown a way of taking variables that are realistic to measure (Actual Volume, Temperature, and Pressure) and using math to calculate an equivalent for the number of molecules being transported across the pipeline (SCF).  While this isn't the whole story, it is a critical foundation to build upon.

## Questions
1. What is the new volume, **in ACF**, if you start with 30 ACF of natural gas at 40°F and 60 psig and convert to a state where the temperature is 100°F and 220 psig?  Assume you are operating in the Appalachian Basin Region.

2. What is the new temperature, **in °F**, if you start with 100 ACF of natural gas at 23°F and 75 psig and convert to a state where the space takes up 72 ACF at 20 psig?  Assume you are operating in the Appalachian Basin Region.

3. What is the volume, **in SCF**, of 1,200 ACF of natural gas at 50°F and 900 psig?  Assume you are operating in the Appalachian Basin Region.

4. What is the volume, **in SCF**, of 10,534 ACF of natural gas at 74°F and 832 psig?  Assume you are operating in the Appalachian Basin Region.

5. What is the volume, **in SCF**, of 425,921 ACF of air at 120°F and 600 psig?  Assume you are operating in the Appalachian Basin Region.