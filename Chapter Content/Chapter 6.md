# Chapter 6: Real Gases

## What are Ideal Gases?

Throughout this book, an assumption was made without directly stating it and this chapter is meant to address it as this becomes important when measuring gas for actual billing, but may ultimately be an advanced concept for an introductory text for technicians.  In all the previous chapters, we have assumed that the gas we are dealing with is an <u>ideal gas</u>. An ideal gas is a theoretical construct used to model real gas behavior under certain conditions.  For this to apply, there are a few constraints that must be applied to the gas being measured.  While this can be quite technical, a simplified version of the considerations is listed below.

1. Molecules are small and spherical
2. All collisions between molecules are frictionless
3. The distance between molecules is larger than the molecules themselves
4. There are no intermolecular forces between molecules (charge repulsion)

However, it is bad to make these assumptions in the context of natural gas pipelines.  The two main reasons are:

1. There are a variety of different types of molecules in natural gas and they tend to form chains as opposed to being organized as spheres.
2. The primary reason that these assumptions are bad is because due to the high pressures in the pipelines, the number of collisions between molecules increases meaning the molecules are closer together and exerting forces on each other due to their different chemical properties/charges.

## Supercompressibility

The question now becomes, if making the ideal gas assumption is bad for our use case, what do we do?  The solution typically used is a factor known as supercompressibility. Supercompressibility is a "fudge factor" used to take into account the fact that the molecules in a natural gas system do not behave ideally and account for the difference between real and ideal gas.  The factors that affect supercompressibility can be broken down into three measured variables that you've already seen.

1. Pressure - Supercompressibility increases with increasing pressure because the molecules get closer together, behaving less ideally.
2. Temperature - Supercompressibility increases with decreasing temperature because the molecules get closer together.
3. Gas Composition/Quality - This has a mixed effect on supercompressibility, but in general, the more oblong molecules (longer chain hydrocarbons) there are, the more it deviates from ideal.

Supercompressibility for this book will be referred to as $z$; however, other natural gas texts and industry texts may refer to F<sub>pv</sub>, which is the square root of $z$. The reason $z$ is used in this book over F<sub>pv</sub> is that $z$ gives a more direct comparison to ideal gas.  For example, a z of 1.1 means that there are 10% more molecules present compared to the ideal gas equation.  When using supercompressibility with the ideal gas equation, the overall equation typically looks like this:

\begin{gather*}
\\
V_2 (SCF) = V_1 (ACF) (\frac{P_1}{P_2}) (\frac{T_2}{T_1}) z \\
\end{gather*} 

\begin{align*}
& where: \\
  & \qquad V_2 = Standard \: Volume \: (SCF)\\
  & \qquad V_1 = Actual \: Volume \: (ACF)\\
  & \qquad P_1 = Pressure \: of \: State \: 1 \: (psia) \\
  & \qquad P_2 = Pressure \: of \: State \: 2 \: (psia) \\
  & \qquad T_1 = Temperature \: of \: State \: 1 \: (°R) \\
  & \qquad T_2 = Temperature \: of \: State \: 2 \: (°R) \\
  & \qquad z = supercompressibility \: (no \: units) \\
\end{align*}

The equations and mathematics used to calculate z are typically the responsibility of the engineer and are outside of the scope of this book.  For this book, z will be a realistic value given the pressure, temperature, and gas quality and just needs to be applied to calculate the standard volume.  Typical values for z range from ~1 for low pressure gas to 1.15 for higher pressure gas. 

### Example (SCF with Supercompressibility)  
```{admonition} **Problem:**  
A diaphragm meter is operating at 20 psig and 50°F.  When you get on site, the index reads 110 ACF.  When you get on site, the index reads 110 ACF.  When you leave, the index reads 130 ACF.  How many standard cubic feet have passed in this time? Take into account supercompressibility, assuming z = 1.003.  Assume you are operating in the Appalachian Basin Region.
```

````{admonition} **Solution:**  
:class: tip, dropdown  
This problem is very similar to problems in chapter 4, the only difference being that supercompressibility needs to be taken into account and the ACF needs to be calculated by taking the difference of the index readings. 

\begin{gather*}
V_1 = 130 ACF - 110 ACF = 20 ACF \\

T_1 = 50°F = 509.67°R \\

P_1 = 20 psig = 34.4 psia
\end{gather*} 

\begin{gather*}
V_2 = ? \\

T_2 = 60°F = 519.67°R \\

P_2 = 14.73 psia

z = 1.003
\end{gather*} 

Knowing all the needed variables, we can solve for $V_2$.

\begin{gather*}
V_2 (SCF) = V_1 (ACF) \frac{P_1}{P_2} \frac{T_2}{T_1} z \\

V_2 (SCF) = 20 ACF \cdot \frac{34.4 psia}{14.73 psia} \cdot \frac{519.67°R}{509.67°R} \cdot 1.003 \\

V_2 = 47.77 SCF \approx \textbf{47.8 SCF}
\end{gather*} 

```{note}
For this example, the supercompressibility changed the result compared to ideal by 0.3%, a very small value.  This is reasonable since the pressure is very low.
```
````

## Questions
1. In layman's terms, what is supercompressibility as used in gas measurement

2. What assumptions are used in the ideal gas law/combined gas law and why are they bad assumptions to make for the natural gas pipelines?

3. What is the standard volume of a sample of gas that is at 60 psig, 80°F, and takes up 500 ACF? Please make sure to factor in supercompressibility.  Assume that z is 1.008 and you are operating in the Appalachian Basin.

4. A diaphragm meter is operating at 10 psig and 40°F.  From reading the index, you gather that 100 actual cubic feet has passed through the meter in the time you have watched it.  How much gas in standard cubic feet has passed through the meter during this time? Please make sure to factor in supercompressibility.  Assume that z is 1.002 and you are operating in the Appalachian Basin.

5. A rotary meter is operating at 100 psig and 90°F.  From reading the index, you gather that 34,200 actual cubic feet have flown through the meter.  The gas chromatograph tells you that the energy density is 1043 BTU/SCF. How much energy in dekatherms has flown through this meter?  Please make sure to factor in supercompressibility.  Assume that z is 1.013 and you are operating in the Appalachian Basin.

6. An ultrasonic meter is operating at 450 psig and 65°F.  You read from the software that 50,000 ACF of gas has passed in the last hour.  The gas chromatograph tells you that the energy density is 1060 BTU/SCF. How much energy in dekatherms has flown through this meter?  Please make sure to factor in supercompressibility.  Assume that z is 1.071 and you are operating in the Appalachian Basin.