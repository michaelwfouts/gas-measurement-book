# Chapter 3: The Chemistry of Gas Measurement

Natural gas is composed primarily of methane, but also contains varying amounts of other hydrocarbons. The exact chemical composition of natural gas can vary depending on the source.  Understanding the properties of each of these compounds and how they interact with physical variables is at the core of gas measurement.  This chapter serves to be as an exposition of the concepts with the math to be detailed in further chapters.

## Molecules
A molecule is two or more atoms bonded together. The atoms combine to form a new unified particle with its own physical and chemical properties.  Atoms are one of the basic building blocks of matter and are typically referred to by their periodic table name.  Examples include carbon (C), hydrogen (H), oxygen (O), and nitrogen (N). For example, the methane molecule consists of 5 atoms bonded together - 1 carbon atom and 4 hydrogen atoms. This gives it the chemical formula of CH<sub>4</sub>, representing the number of each atom in the compound.

This is important to the natural gas industry because of money.  In the natural gas industry in particular, they charge customers based on the <u>number</u> of molecules that flow through the pipe and <u>what</u> those molecules are.  This will get more firmly defined as Standard Cubic Feet (SCF) and Dekatherms (Dth) in later chapters.

## Measurements to count the Molecules
Molecules are incredibly small.  In fact, if you were to line up 1,000,000 water molecules end to end, they would be about the thickness of a human hair. {cite}`molecules-in-cubic-inch` This makes counting them individually completely out of the question.  The question is now: what can we measure in order to estimate the number of molecules in our pipeline?  The answer are four variables: Temperature, Pressure, Actual Volume, and Gas Quality.  The rest of this chapter will be dedicated to explaining each of these in a little more detail, with the exception of Gas Quality, which gets it's own chapter.

## Absolute Units
Before continuing, there is one topic that needs to be expanded upon and is crucial to the later mathematical calculations: Absolute units. Absolute units are units of measurement that are based on natural physical constants or properties, rather than relative points. These will be noted as different units are introduced going forward, but the key similarity between all absolute units is <u>the smallest possible value is 0</u>.  By avoiding negative numbers in the scale, it allows the math to become much simpler as they all have a fixed, universal reference point.

## Temperature
Temperature is a physical property that measures how hot or cold an object is. More specifically, it is a measure of the average kinetic energy of molecules within an object. Kinetic energy is the energy of motion, specifically from the molecules vibrating inside of an object. As an object gains thermal energy, its molecules move faster as they gain kinetic energy as shown by an increase in temperature. Lower temperature means lower average kinetic energy, as particles slow down.
Since gas measurement is about measuring these molecules, temperature is one of the critical properties to measure to see how the molecules are behaving and interacting with one and other inside of the pipe.

When measuring temperature in the United States, typically either the Fahrenheit scale (relative units) or the Rankine scale (absolute units) are used.  A degree change in both the Fahrenheit and Rankine scales are equivalent; however, there is an offset of 459.67°  between the two units to make 0°R the smallest value on the Rankine scale.  In the metric system, the scales used to measure temperature are Celsius and Kelvin; however, this book will focus on the United States customary units.  Below is a table showing some important values of temperature in each scale.

|Description|°F|°R|
|---|---|---|
|Boiling Point of Water|212|671.67|
|Freezing Point of Water|32|491.67|
|Absolute Zero|-459.67|0|

The equations used to convert between the two are:

$$
°F = °R - 459.67
$$

$$
°R = °F + 459.67
$$

## Pressure
Pressure is a fundamental physical force that quantified the perpendicular force applied over a surface. It refers to the force exerted per unit area on an object or by the object.
On a microscopic scale, pressure results from molecules colliding with a surface.  To think of this in terms of a natural gas pipeline, as more molecules are forced into the pipeline, more collisions happen with the wall of the pipe, increasing the pressure on the surface of the pipe.

An important concept to understand about gas measurement is atmospheric pressure. This refers to the pressure exerted by the weight of the air in Earth's atmosphere. It results from the gravitational attraction of the planet pulling air molecules down towards its surface.

At sea level, the average atmospheric pressure in United States customary units is approximately 14.7 psi (pounds per square inch or lb/in<sup>2</sup>). This means the force pressing perpendicularly across every square inch of surface is 14.73 pounds. As altitude increases, there are fewer air molecules above exerting a downward force, so atmospheric pressure decreases. For example, Mount Everest at 29,029 feet has an atmospheric pressure of 4.84-4.89 psia. {cite}`mt_everest_2015`.

It is important to note that there are versions of this measurement for both absolute and relative units.  For example, psia stands for "pounds per square inch absolute" while psig stands for "pounds per square inch gauge.  Psia refers to the absolute pressure measured relative to a perfect vacuum (0 psia) and it includes the atmospheric pressure. Psig refers to the gauge pressure measured relative to the local atmospheric pressure (0 psig) excludes atmospheric pressure.  For example,  if a tire gauge shows the pressure is 32 psig, that means the tire pressure is 32 psi above the ambient atmospheric pressure.  To convert between absolute and gauge units, use the following formula:

$$
Absolute \: Pressure \: (psia) = Gauge \: Pressure \: (psig) + Atmospheric \: Pressure \: (psia)
$$

One piece of information that typically must be assumed when dealing with pressure is assuming what the atmospheric pressure is.  Since it varies with location, it can affect the overall calculations to count the number of molecules inside the pipeline.  Financially speaking, this is typically done during contract negotiations mentioned in {doc}`Chapter 1<../Chapter 1 - How the Gas Industry Works/Chapter 1>`.  

This text considers two options. The first is that Atmospheric Pressure is that of sea level (14.73 psia).  This is a common reference point because the ocean is one continuous body of water and its surface has a similar height, regardless of where in the world one is.  The second is known as the average atmospheric pressure in the Appalachian Basin Region (14.4 psia).  This is used for this text because this book was originally written in West Virginia, in the middle of this region, and gives an understanding of local air pressure. However, this number could be adapted to any local operating area.

## Volume
Volume is a fundamental physical quantity that measures the three-dimensional amount of space an object or substance occupies. It quantifies how much a container can hold or the magnitude of a space.  Gas particles spread out to fill any container, and their volume changes substantially under different conditions.  In the context of natural gas pipelines though, the walls of the pipe act as a rigid barrier to give a defined volume to the gas.

While there is typically only one way for measuring volume with United States customary units, colloquially speaking, there are two "volumes" that are used in the natural gas industry and I want to take this moment to clarify the distinction between the two.

The first is Actual Cubic Feet (ACF) which is a measure of the physical space something takes up.  For example, if you have a box that is 1 ft on each side, the total volume of space that the box takes up is 1 ACF.  

The second value is referred to as the "Standard Cubic Foot" (SCF).  However, note that the SCF <u>is NOT a volume unit of measurement</u>.  The idea comes from the fact that the temperature and pressure are held constant.  By doing this, the SCF becomes analogous to the number of molecules of gas and not the physical space it takes up.  This is described in more detail in the next chapter as well as a mathematical explanation.

Colloquially speaking, in industry, the difference between an ACF and SCF is not explicitly ever said.  However, most of the time a cubic foot is mentioned, it is about an SCF.  Often Roman Numerals or letters are accompanied by the number of cubic feet to account for the fact that an SCF of gas is very small in a practical sense (for example, the average home uses 196 SCF of gas a day) {cite}`natural-gas-the-facts`.  Some common examples of units are shown below.

|Unit|Meaning|
|---|---|
|MCF|Thousand Standard Cubic Feet|
|MMCF|Million Standard Cubic Feet|
|BCF|Billion Standard Cubic Feet|

## Questions
1. Convert the temperatures from the units given to the units requested.  
    a. 80°F to °R   
    b. 120°F to °R  
    c. 250°R to °F  
    d. 423°R to °F  
    e. -12°F to °R  

2. Convert the pressures from the units given to the units requested, assuming you are operating in the **Appalachian Basin Region**.  
    a. 100 psig to psia  
    b. 489 psia to psig  
    c. 0 psig to psia  


3. Convert the pressures from the units given to the units requested, assuming you are operating at **Sea Level**.  
    a. 145 psig to psia  
    b. 32 psia to psig  
    c. 0 psig to psia  


4. What is the difference between actual cubic feet and standard cubic feet?


5. Please share a safety contact pertinent to either recent events at large or in your personal life.