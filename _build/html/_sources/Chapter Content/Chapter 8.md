# Chapter 8: Meters

## Meters

Meters are essential devices in natural gas measurement. Typically, they directly quantify the volumetric flow rate (ACF) of gas in a pipeline or process system.  Each works on different operating principles to measure real-time flow with precision and accuracy. Meters have specialized sensor designs, materials, and electronics to provide stable and reliable data.  This chapter serves as an introduction to each of these types of meters and their pros and cons.

## Turndown Ratio

While most people can intuitively understand the maximum flow rate limitations of meters (such as pipe size), what is often much less understood is the minimum flow rate limitations.  Depending on the technology of the meter (sensing elements) there is a low limit at which the sensing device can no longer differentiate a flow from the normal background noise in the process.  This has many factors that contribute to it, such as the resolution of the sensors, changes in fluid dynamics through the meters, and statistical uncertainty.  Some meters can have quite high minimum flow rates meaning that without proper design, gas can flow by undetected by the meters, resulting in improper billing.  The term typically used to describe the range of a meter is the turndown ratio.  The turndown ratio is simply the maximum flow rate divided by the minimum flow rate as shown below.

\begin{gather*}
\\
Turndown \: Ratio = \frac{Maximum \: Flowrate}{Minimum \: Flowrate} \\
\end{gather*} 

With large changes in flow rate over a station's lifetime being quite common, the design of the measurement station can vary greatly.  Due to large uncertainty with initial estimates as times, meters with larger turndown ratios will typically be preferred over those with smaller ones.  However, every station should be designed on a case-by-case basis by an engineer.

## Meter Types

There are several types of meters to measure the actual volume of gas flowing through a pipeline, each with distinct advantages and disadvantages.  This section is meant to provide a brief overview of the different meters out there to give an understanding of what is currently used and why.

### Positive Displacement Meters

Positive displacement meters work by mechanically confining and moving fixed volumes of gas through the meter body. As gas fills a chamber of known volume, that captured volume is forced through the meter into the downstream line. This directly measures the flow in volumes over time.

A metaphor that helps explain how this works involves filling up an empty pool with a 5-gallon bucket.  If you put a single 5-gallon bucket of water in the pool, the pool now has 5 gallons of water.  If you put three 5-gallon buckets of water in an empty pool, you now have 15 gallons of water in the pool.  Positive displacement meters work by forming some confined space of fixed volume and noting how many times that bucket of volume gets moved.  The two types that will be discussed here are diaphragm and rotary meters.

#### Diaphragm Meters

Diaphragm meters are a type of positive displacement flow meter used for natural gas measurement. They contain two or more flexible diaphragms that move back and forth. As gas fills the chambers behind the diaphragms, it displaces and flexes them. The diaphragms then recoil, forcing the gas through the meter.  This oscillating diaphragm action essentially divides the gas into fixed packets of known volume. The number of diaphragm cycles indicates the total volume passed. 

Diaphragm meters  are typically used in low flow applications (0.5 to 10 MSCFD) and low pressure applications (5-10 psig).  However, they do boast one of the highest turndown ratios at 80:1 due to the fact that they can measure incredibly small volumes (known as pilot loads).  The typical application includes house meters used in residential applications.  They are very cheap and have a high accuracy; however, due to the low pressure, sometimes sediment or water can fill the diaphragms, resulting in over measuring and due to the low flow requirements, these are used in limited applications.

#### Rotary Meters

Rotary meters are a type of positive displacement flow meter used extensively for natural gas measurement. They contain two figure-8 shaped impellers mounted on a rotating shaft inside the meter body. As gas passes through, it causes the impellers to spin proportionally to the flow rate.The impeller shaft drives gears connected to a counter. The number of impeller revolutions indicates the total gas volume.

Rotary Meters are typically used in low to medium flow applications (5-1000 MSCFD), but with a very flexible pressure range from 20-1480 psig depending on the model.  Rotary meters have a mediume turndown ratio, ranging from 10:1 to 80:1.  Applications include store meters (Walmarts/Warehouses) and low flow measurement for producers.  These meters are relatively cheap and due to the wide pressure ranges of the meters, can be used in a wide variety of applications.  Due to the mechanical nature of the meters, they can be maintained for long lifespans; however, industry is shifting away from repair in favor of replace where the economics make sense.  However, this meter can lock up if spun too fast and requires some maintenance to keep accuracy high.

### Orifice Meters

Orifice meters are a common flow measurement technology relying on differential pressure created by gas passing through an opening. They contain an orifice plate with a circular opening inserted into the flow. This creates a restriction that increases velocity and reduces pressure.  The differential pressure between upstream and downstream of the orifice is measured and indicates flow rate. Orifice meters work based on the principals of conservation of energy and continuity of flow.  The following video gives a good visualization of how an orifice meter works.

https://www.youtube.com/watch?v=oUd4WxjoHKY

Orifice meters are used in low to medium flow applications (200 to 3000 MSCFD) and medium to high pressure applications (150-1480 psig).  The critical downfall of orifice meters is that they have a very low turndown ratio of 3:1.  They do offer some flexibility as orifice plates, which are typically very cheap, can be changed out to better match predicted flow rates, this still requires manual intervention and additional design.  They are typically used with producers as the plates are easy to pull and clean when dealing with dirty gas and in transmission application when cheap measurement is needed.  The advantages of the orifice meter includes the fact that it is cheap and with certain meter designs, can have the plate taken out during operation without blowing down the pipeline to verify accuracy and perform maintenance.  However, these meters typically have a higher measurement error (2%) compared to other systems.  The plates are easy to have chipped or dirtied and there is no technology to identify these and routine maintenance is needed to verify.  It also creates a permanent pressure drop (though not always an issue) and the low turndown ratio makes them only able to be used in very set flow rate applications.

### Turbine Meters

Turbine meters work by using the flow of gas to spin a turbine rotor inside the meter body. The rotor turns a shaft coupled to a magnetic pickup or mechanical counter that generates output pulses proportional to frequency of rotation.  As velocity increases, the rotor spins faster. The rotation rate measured by the frequency sensor corresponds to the gas flow rate. 

Turbine meters are used in medium to high flow applications (100-10,000 MSCFD) and medium to high pressure applications (150-1480 psig).  They have a lower turndown ratio at about 10:1, mostly due to the fact that there is a high amount of error at very low flows.  They are used in producer high flow applications and transmission medium/high flow applications.  However, current designs are often using ultrasonic meters instead of turbine meters in new installations where economics makes sense. These meters typically have swappable turbine modules should they need to be replaced, which makes offsite maintenance easy.  However, due to the mechanical nature of these meters, they typically create issues in application.  Most common is that when testing these meters, the meter run will be blown down too quickly resulting in damage to the blades of the meter that go undiagnosed.  The meters also require oiling in order to keep the mechanical parts in good shape.

### Coriolis Meters

Coriolis meters operate differently than any other meter on this list.  They measure mass flow directly (instead of actual volume) by using oscillating tubes that bend and twist in response to the momentum of the flowing fluid.  This means they are able to directly measure a SCF value without temperature or pressure transmitters. As gas passes through vibrating tubes, it causes deflections proportional to mass flow.  Sensors on the inlet and outlet tubes measure the resulting phase difference. This difference is caused by the Coriolis effect from the gas momentum and indicates mass flow.

https://www.youtube.com/watch?v=XIIViaNITIw

Coriolis meters can be used for very low to high flow rates, but typically are only used in very low to medium flows (10-3,000 MSCFD).  The pressure ratings range from 150-1480 psig.  Coriolis meters boast the highest turndown ratio of any meter on this list because they are able to measure very small flow rates.  These meters are used in transmission low flow as well as refineries and chemical plants.  These meters are the first on the list that are considered "Smart Meters" meaning they have several auxiliary sensors to run diagnostics on the meter's health which can be remotely read without being on-site.  Additionally, there is logic to point out issues and suggest courses of action within the meter.  These meters are additionally very accurate.  However, the major drawback of these meters is their cost, typically being several times that as other alternatives.

### Ultrasonic Meters

Ultrasonic flow meters measure flow rate by sending ultrasonic sound waves diagonally across a pipe through the flowing gas. This creates a small time difference between the upsteam and downstream signals that indicates flow velocity.  They work by measuring the transmission time difference between upstream and downstream ultrasonic pulses. This transit time difference is proportional to flow velocity. The cross-sectional area of the pipe yields the volumetric flow rate.

https://www.youtube.com/watch?v=Bx2RnrfLkQg

Ultrasonic meters are used for medium to very high flow rates (500-300,000 MSCFD) and medium to high pressure applications (150-1480 psig).  One of the limiting factors of this technology is that it can't accurately measure at lower pressures.  It has a respectable turndown ratio of 50:1.  Applications include transmission high flow.  This is another smart meter, gathering several diagnostics about the component operations to identify if there are any issues with measurement before they happen.  Ultrasonic meters are considered high accuracy meters and boast the fact that there are no moving parts in the meter, allowing it to be full line.  However, this meter is very expensive and if anything does go wrong with it, the meter tube needs to be rolled out to inspect the inside, which can cause calibration concerns due to misalignment during reinstallation.

### Summary Table

Below is a quick look at each meter, comparing their capabilities.

|Category|Diaphragm|Rotary|Turbine|Orifice|Coriolis|Ultrasonic|
|---|---|---|---|---|---|---|
|**Flow Rates (MSCFD)**|0.5 to 10|5 to 1000|100 to 10000|200 to 3000|10 to 3000|500 to 300,000|
|**Pressure Rating** (not operating pressures) ANSI class 150-600 | 5-10 psig (low pressure).  Can go as high as 100 in older applications, but not typical. | 175-1480 psig (low to high)| ~150-1480 psig (medium to high)| ~150-1480 psig (medium to high)| ~150-1480| ~150-1480 psig (medium to high). Technologies now allowing us to measure lower pressures |
|**Turndown Ratio**| High (80:1)| Medium (10:1 to 80:1)| Low (10:1)| Low (3:1)| High (100:1)| High (50:1)|
|**Type of Meter**| Positive Displacement | Positive Displacement | Inferential | Inferential | Mass | Inferential |
|**Typical Applications**| 1. House Meter | 1. Store Meter (Factories/Wal-Mart) <br> 2. Producer or Transmission Low Flows | 1. Producer High Flows <br> 2. Transmission Medium/High Flows | 1. Producer (Dirty Gas because easy to clean plate) <br> 2. Transmission, wherever they need cheap measurement (Feed Compressor Engines)| 1. Transmission Low Flow, but high pressure <br> 2. Refineries and chemical plants | 1. Transmission High Flows |
|**Advantages**| · Cheap <br> · High Turndown Ratio <br> · High accuracy <br> · Pilot loads |· Cheap <br> · Can be used in a variety of applications <br> · Can be maintained| · Swappable modules | · Cheap <br> · Can take out the plate without putting the run out of service| · Smart Meter Diagnostics <br> · Doesn’t lock up <br> · High accuracy  | · Smart Meter Diagnostics <br> · High Accuracy <br> · Full Line Meter |
|**Disadvantages**| · Can fill up with water| · Can lock up if spun too fast or obstructions go through <br> · Requires Oil to maintain moving parts | · Causes pressure drop <br> · When testing, very easy to break or not test properly <br> · Low turndown ratio for high flows <br> · Requires oiling | · Higher measurement error <br> · Easy to have plates chipped or dirtied <br> · Creates Pressure Drop <br> · Low Turndown Ratio (change plates to meet operational needs) | · Higher cost for low flow | · Expensive |

## Testing Procedures

Every meter has its unique testing procedure.  This book does not contain all the individual testing methodologies, but it does cover one of the most common testing methods known as proving.

### Proving
A meter prover is a specialized calibration device used to validate the accuracy of gas flow meters. Provers provide an independent, traceable measurement standard against which a meter is checked.  Each utilizes a calibrated reference volume to compare meter readings.  Two of the most common proving devices are the master meter and the sonic nozzle.

1. Master Meter (Transfer Prover) - A master meter is a highly accurate reference flow meter used as a field proving standard. It is installed in series with the meter under test. The master meter and test meter measure the same flow.  By comparing volumes measured by the master meter against those measured by the test meter, a meter calibration factor can be derived. This corrects for any error in the test meter at various flowrates.  A figure of this configuration can be seen below

```{figure} ../Assets/master-meter-prover.png
---
name: master-meter
---
Two Valve Manifold Diagram
```

2. Sonic Nozzle - A sonic nozzle prover is a gas flow calibration standard that utilizes a smoothly contoured convergent-divergent nozzle to create a choked sonic flow. Typically, natural gas from the pipeline is used for testing.  This gas accelerates through the narrowed throat of the nozzle, reaching sonic velocity, a constant given gas conditions.  This creates a fixed flow area and constant mass flow rate dependent only on upstream pressure and temperature. The exact flow is calculated from the inlet gas conditions based on rigorous models.  A figure of this configuration can be seen below.

```{figure} ../Assets/sonic-nozzle-prover.png
---
name: sonic-nozzle
---
Two Valve Manifold Diagram
```

This method is largely falling out of favor due to the environmental impacts of blowing natural gas directly to atmosphere.

## Questions
1. What is the turn down ratio of the following meters with the given maximum and minimum flow rates?  
    a. Max – 1,200 MCFH; Min – 300 MCFH  
    b. Max – 100,000 MCFD; Min – 5,000 MCFD  
    c. Max – 45,000 MCFH; Min – 900 MCFH  
    d. Max – 200 MCFD; min – 2 MCFD

2. Please briefly describe how a positive displacement meter works.  Name the two main types of positive displacement meters and list the pros and cons of each.

3. Please briefly describe how an orifice meter works.  Additionally, describe the pros and cons of an orifice meter.

4. Please briefly describe how a turbine meter works.  Additionally, describe the pros and cons of a turbine meter.

5. Please briefly describe how a Coriolis meter works.  Additionally, describe the pros and cons of a Coriolis meter.

6. Please briefly describe how an ultrasonic meter works.  Additionally, describe the pros and cons of an ultrasonic meter.

7. Explain what the proving process is and why it is important.  Additionally, name two devices that can be used to prove a meter.