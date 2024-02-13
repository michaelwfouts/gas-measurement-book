# 1 - Orifice Meters

## Introduction to Orifice Meters

Orifice meters operate on a fundamental principle of fluid dynamics: as a fluid (in this case, natural gas) passes through a constricted opening, its velocity increases, and a pressure differential is created between the upstream and downstream sides of the constriction. The orifice plate, which is the central component of the orifice meter, is a thin plate with a precisely sized hole drilled in the center. It is placed in the path of the flowing gas within a pipeline. This setup forces the gas through the small opening, leading to a measurable drop in pressure across the plate.

The amount of this pressure drop is directly related to the flow rate of the gas. By applying Bernoulli's principle and the continuity equation, the flow rate can be calculated based on the measured pressure differential and the physical characteristics of the gas. Various corrections must be applied to account for factors such as temperature, pressure, and the composition of the gas to ensure accuracy in measurement.  These types of calculations are done by flow computers/PLCs and are verified by engineers.  Performing such calculations are largely outside of the scope of the day-to-day responsibilities of a gas measurement technician.

Orifice meters are favored for their simplicity and cost-effectiveness. They require no moving parts, which minimizes maintenance and increases durability. Furthermore, they can be designed to meet specific requirements by adjusting the orifice plate's diameter.  However, they have very low turndown ratios, making them non-ideal for highly variable flows. Additionally, accurate installation and calibration are crucial. The orifice meter must be properly aligned within the pipeline, and the pressure taps used to measure the differential pressure must be precisely positioned to ensure accurate readings.  This also means that any defect in the plate, no matter how small, may have an effect on the overall measurement.

For a brief overview and visual of how orifice meters work, please watch the following video:

https://www.youtube.com/watch?v=oUd4WxjoHKY

## Types of Orifice Meters

Orifice meters come in various configurations, each designed to meet specific operational requirements and applications. The three primary types of orifice meters are single chamber, dual chamber, and in-pipe orifice meters. Understanding the differences between these types is crucial for selecting the appropriate metering solution for a given application.

### Single Chamber Orifice Meters
Single chamber orifice meters are the most straightforward and common type of orifice metering system. They consist of a single metering chamber where an orifice plate is installed directly in the flow line. The fluid flow is measured by the differential pressure created across the orifice plate as the fluid passes through. Single chamber orifice meters are known for their simplicity and ease of installation. They are typically used in applications where space is limited and where the flow conditions are stable. The primary advantage of this type is its cost-effectiveness and the relatively easy access it provides for inspection, maintenance, and orifice plate changes. However, the downside is that any maintenance or inspection requires the flow to be stopped, which can be a significant drawback in continuous operation systems.

### Dual Chamber Orifice Meters
Dual chamber orifice meters, also known as bypass meters, include two chambers: a main metering chamber and a secondary chamber that allows for the orifice plate to be inspected, maintained, or replaced without interrupting the flow of fluid. This is achieved by diverting the flow from the main chamber to the bypass chamber, ensuring that operations can continue uninterrupted. This design is particularly useful in applications where flow cannot be stopped, such as in high-demand gas distribution systems. Dual chamber meters are more complex and expensive than single chamber meters, but the benefits of non-stop operation and ease of maintenance often justify the additional cost.

### Orifice Unions
Orifice unions differ from the previously mentioned orifice meter types by integrating the orifice plate within a union fitting that connects two sections of pipe. Orifice unions are highly favored in applications where space is at a premium and where the fluid flow measurement does not demand the complexity or accuracy/precision of a chambered orifice meter system.

The main drawback of orifice unions comes in their inspection criteria.  To inspect a plate inside of an orifice union, the pipe must be taken apart at the flange, requiring the pipe to be taken out of service and possibly moved and the bolts to then be retorqued afterwards.  This is why this type of meter has largely fallen out of favor and is only used is very few cases where accuracy is less of a concern and measurement is, typically temporary.  Even for temporary applications though, portable ultrasonic flow meters are beginning to take up more market share in this niche.

## Beta Ratio

The beta ratio is defined as the ratio of the diameter of the orifice ($D_i$​) to the diameter of the pipe ($D_o​$), expressed as:

\begin{gather*}
\\
\beta = \frac{D_i}{D_o}
\\
\end{gather*} 

\begin{align*}
& where: \\
  & \qquad D_i = Inside \: Diameter \: of \: Plate\\
  & \qquad D_o = Inside \: Diameter \: of \: Pipe \: (Not \: Outside \: Diameter \: of \: Plate)\\
\end{align*}

The value of the beta ratio is critical for several reasons:
1. Flow Calculation Accuracy: The beta ratio influences the coefficient of discharge ($C_d$​) of the orifice meter, which is used in the calculation of the flow rate. The   Cd​accounts for losses in the meter and varies with the beta ratio, Reynolds number, and the physical characteristics of the orifice plate.
2. Range of Measurement: The beta ratio determines the range over which the orifice meter can accurately measure flow. Typically, the beta ratio is chosen to be between 0.2 and 0.75 for optimal accuracy and minimal pressure loss. A lower beta ratio means less pressure drop and higher energy efficiency but can reduce measurement accuracy and sensitivity.
3. Pressure Drop: The size of the orifice relative to the pipe size affects the pressure drop across the meter. A larger beta ratio results in a greater pressure drop for a given flow rate, which can be undesirable in applications where maintaining pressure is critical.
4. Turn Down Ratio: The beta ratio affects the turn down ratio of the orifice meter, which is the range of flow rates over which the meter can accurately measure. A carefully selected beta ratio allows for a wider range of accurate flow measurement.

Acceptable beta ratios range from 0.3 to 0.7.  This final number will typically be determined by an engineer based on the factors above {cite}`beta_ratio`.

### $D_r$ (Diameter at Reference Temperature)
Understanding the distinction between $D_r$​, the diameter at a reference temperature, and  $D_{nominal}$, the nominal or internal diameter of an orifice plate under design criteria, is crucial for accurate flow calculations. The $D_r$ value represent the inside diameter of the plate ($D_i$ in the $\beta$ equation) at a reference temperature (typically 60°F).  Because orifice plates are made of metal, they undergo physical changes with temperature variations and this impacts flow measurement accuracy.  Typically, both the $D_r$ and $D_{nominal}$ values are written explicitly on the plate and neither need to be measured with calipers.  However, it is important to know that when ever performing flow calculations, the $D_r$ value is the one that should be used and input into any flow computers as AGA3 equations take into account changes in temperature.

## Flow Calculations

The flow rate through an orifice meter can be calculated via several methods.  In the natural gas industry, the typical standard is to use the equations outlined in AGA3.  However, these calculations are more complicated than needed for a technician level undersatnd of flow measurement and instead, the flow equation described in this book will be a more general equation used for flow of any fluid (including liquids) through an orifice meter provide by ISO 5167-1:2003. This equation incorporates several factors, including the physical dimensions of the orifice plate, the properties of the fluid, and the measured pressure drop across the orifice. This equation is represented as:

\begin{gather*}
\\
q_{m} = \frac{C_{d}}{\sqrt{1-\beta^{4}}} \; \epsilon \; \frac{\pi}{4} \; d^{2} \; \sqrt{\frac{2 \; \Delta p}{\rho_{1}}}
\\
\end{gather*} 

\begin{align*}
& where: \\
  & \qquad q_{m} \: = \: actual \: volumetric \: flowrate, \: ACF \: per \: Second\\
  & \qquad C_{d} \: = \: coefficient \: of \: discharge, \: dimensionless, \: typically \: between \: 0.6 \: and \: 0.85\\
  & \qquad \beta \: = \: Beta \: Ratio\\
  & \qquad \epsilon \: = \: expansibility \: factor, \: 1 \: for \: incompressible \: gases \: and \: most \: liquids,  \: dimensionless\\
  & \qquad d \: = \: internal \: orifice \: diameter \: under \: operating \: conditions, \: ft\\
  & \qquad \rho_{1} \: = \: fluid \: density \: in \: the \: plane \: of \: upstream \: tapping, \: lbf/ft³\\
  & \qquad \Delta \: p \: = \: differential \: pressure \: measured \: across \: the \: orifice, \: psia\\
\end{align*}

Source: https://en.wikipedia.org/wiki/Orifice_plate

One point of clarification here is the $\epsilon$ is related to $z$, the supercompressibility factor mentioned in the Lecture Section.  However, they are different concepts.  The expansibility factor accounts for the density change of a gas due to pressure reduction as it passes through the orifice. It corrects for the assumption of constant density used in the simplified flow rate equations. The term "supercompressibility factor" is sometimes used interchangeably with the expansibility factor, but it can also refer more broadly to the factor used to correct for real gas behavior compared to ideal gas behavior.

One important note to make is that the permanent loss in pressure drop caused by the orifice plate is often small due to the low density of natural gas compared to more viscous fluids (mostly liquids).  Because of this, it is often seen that the pressure drop is measured in a unit called inches of water column. The conversion from psi to inches of water column is about 27.7 inches of water column to 1 psia.

## Uni-Directional vs Bi-Directional Plates
The distinction between beveling in unidirectional and bidirectional orifice plates is primarily due to their intended direction of flow measurement and the need to optimize flow conditions for accuracy and equipment longevity. Here's a closer look at why these design choices are made:
### Unidirectional Orifice Plates
Unidirectional orifice plates are designed for flow measurement in one direction only. The bevel on a unidirectional orifice plate serves several purposes:
1. Minimizing Pressure Loss: The bevel is designed to reduce permanent pressure loss by facilitating a smoother transition for the fluid as it accelerates into the orifice and then decelerates and recovers pressure downstream. This smoother transition reduces turbulence and the associated energy loss.
2. Reducing Wear and Tear: The sharp edge of the orifice, where the flow enters, is more susceptible to erosion and wear because of the high-velocity and potentially abrasive action of the fluid. The bevel is placed on the downstream side to minimize the impact on the plate's sharp edge and to protect the integrity of the measurement by keeping the upstream edge intact.
3. Improving Measurement Accuracy: A well-defined flow profile, which is essential for accurate flow measurement, is easier to achieve with a beveled edge on the downstream side. The bevel helps maintain a stable flow pattern across the orifice.

One crucial fact about uni-directional plates is their orientation.  The smaller diameter side of the beveled edge goes upstream and the larger edge goes downstream.  Without proper training and knowledge of an orifice meters, people often think that an orifice plate should act as a funnel, focusing the gas through the meter, but this is INCORRECT.  Instead, the plate should provide a hard stop for the gas and the beveled edge allows for a better flow profile to develop downstream.
When measuring the beta ratio for a beveled orifice plate, the beta ratio ($\beta$) is determined based on the diameter of the orifice at the point where the fluid flow is constricted, which is the upstream side (the smaller diameter side) of the bevel. 

### Bidirectional Orifice Plates
Bidirectional orifice plates, on the other hand, are designed to measure flow accurately in both directions. Because of this dual functionality:
1. No Beveling: These plates cannot have a bevel like unidirectional plates because adding a bevel would favor flow in one direction over the other. To ensure accurate measurement for flow in both directions, the edges on both sides of the orifice must be sharp. This design helps maintain a consistent and predictable differential pressure drop regardless of the flow direction, which is crucial for accuracy in bidirectional flow scenarios.
2. Uniform Wear and Tear: While bidirectional plates might experience more uniform wear over time since flow can occur in both directions, the absence of a bevel means that there could be slightly higher pressure loss and potential for wear at the orifice edges. However, this compromise is necessary to maintain bidirectional measurement capabilities.

## Plate Inspections
As a Gas Measurement Technician, you're primary responsibility will be to maintain the health of the meter.  The orifice plate is the most important piece of equipment in this measurement technique and to make sure it is operating properly, needs to be inspected regularly.  This section covers several techniques used to ensure an orifice plate is in good operating condition and what to look for.

### Visual Inspection
One of the most common ways issues are identified with orifice plates is simply by looking at them.  A visual inspection can often identify issues with the plate.  The most common issues to look for include the following:
1. Scratched - Being exposed to the gas stream means that dirt and debris can flow through and scratch the orifice plate.  The upstream section of the orifice plate specifically is fabricated to be a specific smoothness to help with the development of the flow profile through the meter.  If there are scratches on the upstream side, then the accuracy of the orifice meter can be affected.
2. Nicked - Should dirt and debris flow through the meter, the weakest point of the plate is at the thinnest point, at the edge of the bevel.  This makes it possible for the inside beveled edge to chip off, creating issues with the measurement.
3. Dirt/Grease - If dirt or grease flows through the meter, it is not uncommon for the plate to begin to have a build up of dirt/a sheen of grease on it.  This can alter the flow profile going through the orifice meter and effect measurement.  Regular cleaning of the orifice plate should be scheduled if this is the case to ensure the highest accuracy possible.
4. Bent - If a large amount of gas tries to flow through the meter, the high differential pressure can cause the plate to bend/warp.  This greatly effects the accuracy of the measurement and can even effect the ability to remove the plate to be inspected in the first place.  There are methods for determining if the plate is bent enough that it has to be replaced (Departure from Flatness: referred to in next section).  However, from a practical stand point, most companies will replace a plate if any warping occurs because the amount of money in gas that flows through the meter is much more than the price of a new plate.
5. Sharp Bevel - For Uni-Directional orifice plates, the bevel needs to be sharp in order for the proper flow profile to develop.  While there is no definitive way to see if a bevel is sharp, a common check is to see if the beveled edge will leave a scratch on the back of your fingernail or use it to feel the ridges of their fingerprint.

### Departure from Flatness
Orifice plates can become bent should they be exposed to high flow rates and high differential pressures.  Therefore, a measurement known as the Departure from Flatness was created in order to numerically evaluate if an orifice plate is too bent to be put into operation.  The equation is given below:

\begin{gather*}
\\
Maximum \: Tolerance = 0.005(D_o-D_i)
\\
\end{gather*} 

\begin{align*}
& where: \\
  & \qquad D_o = Inside \: Diameter \: of \: Pipe \: (Not \: Outside \: Diameter \: of \: Plate)\\
  & \qquad D_i = Inside \: Diameter \: of \: Plate\\
\end{align*}

Source: https://asgmt.com/wp-content/uploads/2018/03/038.pdf

From a practical standpoint, if there is any warping of the plate, most companies will simply replace the plate because the amount of money in gas that flows through the meter is much more than the price of a new plate.  However, whenever a new plate is installed, typically a technician will perform a departure from flatness calculation to ensure the plate was manufactured correctly.

### Measure of Eccentricity
The Measure of Eccentricity is a check not typically performed every plate inspection.  Rather, it is done when new plates are installed to verify no manufacturing defects are present.  This measurement ensures that the orifice is places in the exact middle of the plate.  In other industries and use cases, orifice plates with holes that are off center can be common, but this is not such the case for natural gas.  Because of this, verify the plate is perfectly centered by taking eight caliper measurements comparing the width of the orifice plate on exact opposite sides of an orifice plate, rotating 45° between measurement pairs.

### Measure of Roundness
The Measure of Roundness is another check that is typically only performed when changing plates to ensure no manufacturing defects are present.  This check ensures that the orifice hole is indeed a circle and not an ellipse.  To do this, use calipers to measure the bore hole diameter at four different angles, typically rotating measurement 45° each time, and ensure they are within tolerance depending on the standard you are following.

### Verification of Beta Ratio
One of the most important parts of any inspection is to verify the beta ratio.  The internal bore diameter is often etched somewhere on the plate and making sure this number is input correctly into your flow computer is imperative for accurate measurement.  Should this number be off by as much as a quarter of an inch, over a years time, millions of dollars worth of gas can be improperly measured.

## Questions
1. Calculate the $\beta$ value of your orifice plate.

2. Perform a plate inspection on your orifice plate.  Please make sure to record your results to:  
    a. Visual Inspection  
    b. Departure from Flatness  
    c. Measure of Eccentricity  
    d. Measure of Roundness  

3. For your plate, calculate the standard volumetric flow rate using the ISO 5167 equation.  Assume the parameters below. Note: you may have to assume some values not explicitly given. Please give your sources for these.  
    $C_d$  = 0.75  
    $\epsilon$ = 0.9  
    $\Delta p$ = 100 in $H_20$  

4. What are the purposes of the taps on the sides of the orifice meter?