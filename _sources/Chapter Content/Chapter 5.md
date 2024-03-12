# Chapter 5: Gas Quality

## The Math of Gas Quality

Gas quality refers to the composition and properties of natural gas. It encompasses the specific hydrocarbon components (and non-hydrocarbon components) that make up a gas stream or sample.

Natural gas primarily consists of methane, but also contains varying amounts of heavier hydrocarbons such as ethane, propane, butane, and pentanes. Measuring the percentage of each of these gases involves compositional analysis using chromatography. This separates and identifies the component concentrations.

Gas quality is a key factor in commercial transactions.  If you'll recall from earlier in the text, it was said that transactions happen based on the number of molecules and the type of molecules that are delivered.  Chapter 4 laid the foundation for calculating the number of molecules and gas quality is the component that addresses the second half of the problem: what type of molecules are delivered.

When contracts are written, they typically refer to the Dekatherm (Dth), a unit of energy.  It is this value that ultimately needs to be calculated to identify the amount of money that trades hands.  A Dekatherm is defined as 1,000,000 BTUs, another energy unit where a BTU (British Thermal Unit) is defined as the amount of energy it takes to raise 1 lb of water 1°F. {cite}`eia2023`

The gas quality and composition is typically measured using a gas chromatograph. A gas chromatograph (typically referred to as a GC) is an analytical instrument that works by separating the different components in a gas sample. An automated sampler injects the gas sample into a heated column. A carrier gas (typically helium) then carries the sample through the machine. Each compound reaches the end of the column at a different time, known as its retention time. A detector generates an electronic signal as each component exits. Comparing retention times to known standards allows for the identification and quantification of the concentrations of each species in the sample (typically, at least an 11 component analysis). The critical piece of information that a GC provides is the energy density in BTU/SCF (often just called BTU in industry).  This value ranges from about 970-1150 for gas delivered to the end customer.

To calculate the number of Dekatherms, one can use the following equation:

\begin{gather*}
\\
Dekatherm = \frac{Standard \: Volume \: (SCF) \cdot Energy \: Density \: (\tfrac{BTU}{SCF})}{1,000,000}
\end{gather*}

### Example (Basic Dekatherm Calculation)  
```{admonition} **Problem:**  
Assume you have 1,250,000 SCF of gas at 1050 $\tfrac{BTU}{SCF}$.  How many Dekatherms is this? 
```

```{admonition} **Solution:**  
:class: tip, dropdown  
This problem can be simply solved using the equation above.

\begin{gather*}
\\
Dekatherm = \frac{Standard \: Volume \: (SCF) \cdot Energy \: Density \: (\frac{BTU}{SCF})}{1,000,000}
\\
\\
Dekatherm = \frac{1,250,000 SCF \cdot 1050 \tfrac{BTU}{SCF}}{1,000,000}
\\
\\
Dekatherm = 1,312.5 Dth \approx \textbf{1310 Dth}
\end{gather*}
```

### Example (Complete Dekatherm Calculation)  
```{admonition} **Problem:**  
Assume you have 36,450 ACF of natural gas at an operating pressure of 650 psig and a temeprature of 50°F.  Your gas chromatograph shows that this gas is 1070 $\tfrac{BTU}{SCF}$.  Assuming you are operating in the Appalachin Basin Region, how many Dekatherms is this? 
```

```{admonition} **Solution:**  
:class: tip, dropdown  
This problem blends the topics from this chapter with those learned in Chapter 4.  The first goal for solving this problem is to calculate the number of SCF this gas represents.  We can then use the energy density to calculate the total number of dekatherms.

1. Calculate the SCF

\begin{gather*}
V_1 = 36,450 ACF \\

T_1 = 50°F = 509.67°R \\

P_1 = 650 psig = 664.4 psia
\end{gather*} 

\begin{gather*}
V_2 = ? \\

T_2 = 60°F = 519.67°R \\

P_2 = 14.73 psia
\end{gather*} 

Knowing all the needed variables, we can solve for $V_2$, which is the intermediate step for this problem to ultimately find the number of dekatherms.

\begin{gather*}
\frac{P_1 V_1}{T_1} = \frac{P_2 V_2}{T_2} \\

\frac{664.4 psia \cdot 36,450 ACF}{509.67°R} = \frac{14.73 psia \cdot V_2}{519.67°R} \\

V_2 = 1,676,343.38 SCF
\end{gather*} 

2. Calculate the Dekatherms

\begin{gather*}
\\
Dekatherm = \frac{Standard \: Volume \: (SCF) \cdot Energy \: Density \: (\frac{BTU}{SCF})}{1,000,000}
\\
\\
Dekatherm = \frac{1,676,343.38 SCF \cdot 1070 \tfrac{BTU}{SCF}}{1,000,000}
\\
\\
Dekatherm = 1,793 Dth \approx \textbf{1790 Dth}
\end{gather*}
```

### Math Summary

This portion rounds out the basic calculations for solving for Dekatherms, the unit most often dealt with when it comes to contract negotiations and payments.  This value is represents a count of the number of molecules and what molecules are in the gas.  It is important to note that this is the simplified version of the math and more complex variations of the math are used in the real world (and are mentioned in a later chapter).  However, this showcases a solid foundation to build future knowledge.

## A Broader Perspective on Gas Quality

```{note}
The following section is the authors adaptation and interpretation of a talk given at the Appalachian Corrosion Short Course originally presented by Alysia Salva.
```

Before the early 2000's, natural gas consisted of a very predictable composition, often being extracted from relatively shallow wells.  This gas typically contained consistent, high levels of methane, often over 90%, with minimal impurities such as carbon dioxide and nitrogen.  This created a reliable set of operations to process this gas and deliver a consistent product to end customers.

However, this consistency did not hold forever. In the 2000's a shale gas boom happened in the United States from the technological innovations in horizontal drilling and fracking.  This flooded the pipelines with shale gas, which was significantly different than the conventional gas from shallow wells that had preceded.  Shale gas has more varied composition than conventional natural gas, often containing higher concentrations of heavier hydrocarbons like ethane, propane, and butanes.  This makes the processing of the gas more complex as additional units need to be added to the processing plant in order to deliver the same quality of gas customers have come to expect.

This problem has been becoming even more complex over the years with the addition of sources such as Coal Bed Methane, Landfill Gas Wells, Renewable Natural Gas, and Liquefied Natural Gas coming onto pipelines, each with its own unique composition.  This creates challenges for operations that must work to treat and blend these gases together in order to deliver gas that meets customer demand.  As a reference, below is a table giving a relative comparison of these natural gas types to the conventional shallow well natural gas.

|Type|BTU|N<sub>2</sub>|CO<sub>2</sub>|O<sub>2</sub>|C<sub>2</sub>+|
|---|---|---|---|---|---|
|Shale|↑|-|-|-|↑|
|Coal Bed Methane|↓|↑|↑|↑|↓|
|Liquefied Natural Gas|↑|-|↓|↓|↓|
 
## Tariffs
Tariffs refer to the rates and fees charged by natural gas pipelines and utilities for their services transporting and distributing natural gas. Tariffs are established by pipelines and utility companies and approved by regulatory agencies like FERC or state public utility commissions.  A typical component of these tariffs is to include a statement about about the gas quality inside of the pipeline.  These set boundaries for the quality of gas that the pipeline operates within and acts as a goal to achieve "pipeline quality" gas.  Pipeline quality gas is a vague term and differs from company to company, but is typically meant to refer to gas that is within the acceptable limits of the operators tariff.  The table below shows a few examples of what restrictions tariffs may have on gas quality.

|Pipeline|Heat Value BTU/SCF: Min/Max|Oxygen: Max %|Total Inerts: Max %|Carbon Dioxide: Max %|Nitrogen: Max%|Liquefiable Hydrocarbon Dew Point|Hydrogen Sulfide Max Gr/100 CF|Total Sulfur: Max Gr/100 CF|
|---|---|---|---|---|---|---|---|---|
|Company A|Dry Gas: 987/1100|0.20%|5.00%|3.00%|4.00%|Free of hydrocarbons in liquid form| 0.25 Gr | 20 Gr.|
|Company B|967/1110|0.10%|4.00% (carbon dioxide and nitrogen)|3.00%|3.00%|Max 0.05 GPM of C6+ hydrocarbons|0.25 Gr|20 Gr|
|Company C|970/-|0.20%|4.00% total inerts/0.10% carbon monoxide|2.50%|-|Free of hydrocarbons in liquid form|0.30 Gr|10 Gr|

### Dry vs. Wet Natural Gas
Because of the wide range of natural gas that can be marketed, companies often set up a difference between their "Dry" and "Wet" pipelines in order to give more marketability while keeping the gas quality and corrosion concerns to a minimum.  These types of pipelines will have different ranges of acceptable gas qualities, but the large difference between the two is that wet gas contains significant amounts of heavier hydrocarbon components like ethane, propane, butane, and pentane while dry gas is almost entirely methane (>90%).  The heavier hydrocarbon composition makes the gas burn much hotter, creating end user issues, and can form dew droplets in the pipeline, creating corrosion issues.

A common misnomer is that the core difference between dry and wet gas is the amount of water in them.  While it is true the acceptable amount of water is higher in wet gas, the core difference between the two is the hydrocarbon content since that is the marketable product being sold.

## Analyzers

One can only manage the gas in their pipeline as well as they know what is in the pipeline.  This makes identifying the individual components of the gas incredibly important. I'll briefly mention some analyzers here in order to gain a perspective of what is commonly measured on natural gas pipelines.

### Gas Chromatographs
Gas Chromatographs are the workhorses of gas quality, providing the means to measure the individual hydrocarbons of interest.  Their inner workings were previously explained in detail, but I'll add that they are typically used to provide at a minimum an 11 component analysis.  This includes the hydrocarbons from C1-C6+ (methane, ethane, propane, n-butane, isobutane, n-pentane, isopentane, neopentane, and a lump sum of C6+ hydrocarbons) as well as carbon dioxide and nitrogen.  Both of these components are important to measure because they are considered diluents to the final product of natural gas and have no real economic value in the pipeline decreasing the BTU and therefore, the total Dekatherms being transported.  Carbon dioxide in particular is important to measure because it can mix with water in the pipeline to create carbonic acid which causes corrosion in the pipeline.

### Sulfur Analyzers
There are many different species of sulfur that occur inside pipelines, such as H<sub>2</sub>S and mercaptans.  These components can create sulfuric acid when mixing with existing water inside of the pipeline causing incredibly corrosive environments.

### Oxygen Analyzers
While oxygen itself is typically only found in small quantities in the pipeline, it typically acts as an accelerant for other corrosion reactions that happen inside of the pipeline creating a compounding effect on the degradation of pipe.

### Moisture (H<sub>2</sub>O) Analyzers
By far, one of the most important components to measure on the pipeline for corrosion concerns is water.  Without the presence of water, it makes it very difficult for acids to form from other compounds preventing the amount of corrosion that can happen inside of the pipeline.

## Questions
1. What is the energy, in dekatherms, of 1,402,321 SCF of natural gas with an energy density of 1053 BTU/SCF?

2. What is the energy, in dekatherms, of 52,000 ACF of natural gas at 714 psig and 55°F if the reading from the gas chromatograph is 1033 BTU/SCF?  Assume you are operating in the Appalachian Basin Region.

3. What is the energy, in dekatherms, of 98,000 ACF of natural gas at 178 psig and 82°F if the reading from the gas chromatograph is 1112 BTU/SCF?  Assume you are operating in the Appalachian Basin Region.

4. Why did the discovery of new natural gas sources (Shale, Renewable Natural Gas, shallow well gas, etc.) create issues with existing pipeline operations?

5. What is a tariff as related to the natural gas industry and how does it relate to gas quality?

6. What is the difference between dry and wet natural gas?

7. Please name at least three component analyzer types (i.e. the component they measure) typical to a natural gas operation.  Additionally, please describe why it is important to measure each of these components (how do they effect operations)? 