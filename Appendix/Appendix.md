# Appendix

## Chapter 1: How the Gas Industry Works

### Additional Natural Gas Entities
While the simplified example of how natural gas gets transported in {doc}`Chapter 1<../Chapter 1 - How the Gas Industry Works/Chapter 1>` provides the needed framework to begin to understand measurement, there are several additional entities that someone who enters that natural gas profession will need to become familiar with.  Those include: 

1. Gathering and Processing: Once natural gas is extracted from wells, it may need to undergo gathering and processing. This is post production/extraction and can be considered part of upstream or midstream depending on the companies. Gathering pipelines transport the gas from individual wellheads to a central collection point or processing facility. At processing plants, the gas is treated to remove impurities, such as water vapor, carbon dioxide, and sulfur compounds, to meet quality specifications for transportation and commercial use.

2. Transmission: After processing, the natural gas enters the transmission stage. Transmission pipelines, owned by transmission companies or pipeline operators, form an extensive network that spans long distances. These high-pressure pipelines transport large volumes of natural gas from production areas to distribution points or major consumption regions. Transmission operations, including compression stations and storage facilities, play a crucial role in maintaining the flow and balancing supply-demand dynamics.

3. Local Distribution Companies (LDCs): This was briefly mentioned in the chapter, but LDCs (sometimes colloquially called utility companies), serve as the primary interface between the wholesale market and end customers. LDCs purchase natural gas from producers or wholesalers and deliver it to residential, commercial, and industrial customers through local distribution systems. LDCs maintain the infrastructure of pipelines, meters, and service connections required for distributing gas to end users.  Since there is an additional custody transfer point between the LDC and the house/businesses they deliver to, an additional meter is put in the process (typically a diaphragm meter for houses and diaphragm/rotary for larger applications) where the LDC can calculate how much to gas is used by their end customer.

```{tip}
For additional figures and explanations about entities in the natural gas industry, please refer to Chapter 1 of Natural Gas Measurement Handbook by Gallagher {cite}`natural-gas-measurement`.
```

### Additional Wholesale Market Information
On the wholesale market, there are several players at hand including Natural Gas Producers, LDCs, and Power Generators/Industrial Consumers.  However, the Marketers and Traders who facilitate these contracts and transactions are often not taught about, yet play an incredibly important role in the financial operations of the industry. Natural gas marketers and traders act as intermediaries between producers and end customers. They buy natural gas from producers and sell it to other market participants, such as local distribution companies, industrial consumers, or other marketers. Marketers and traders often operate on a regional or national scale and play a crucial role in facilitating transactions and managing the logistics of natural gas supply.  When the natural gas marketers and traders buy this gas, it is typically done in the form of contracts.  These contracts establish the terms and conditions of the trade, including the volume of gas, delivery locations, pricing mechanisms, and contract durations. Common contract types include:

- Spot Contracts: Spot contracts involve the immediate delivery of natural gas at current market prices. They are often used for short-term or immediate needs, and the prices are determined by supply and demand dynamics.
- Futures Contracts: Futures contracts are agreements to buy or sell natural gas at a predetermined price for delivery at a specified future date. They allow market participants to hedge against price fluctuations and manage their exposure to market risks.
- Long-Term Contracts: Long-term contracts are typically multi-year agreements between producers and buyers. These contracts provide stability and security in the supply of natural gas over an extended period. They often include fixed or indexed pricing mechanisms.

## Bonus Content

### Communications

Gas measurement deals significantly with the electronic transfer of data.  Below is a figure representing a high-level transfer of data from the measurement device back to the databases where the information is stored.

```{figure} ../Assets/communication-diagram.png
---
name: communication-diagram
---
High-Level Gas Measurement Data Communication Diagram
```

1. Field Equipment - Captures measurements from sensors for use by other systems.  Examples include meters (orifice, ultrasonic, turbine, etc.), transmitters (temperature, pressure, and DP) and gas quality equipment (gas chromatographs, moisture analyzers, oxygen analyzers, etc.)

2. RTU (Remote Terminal Unit) or PLC (Programmable Logic Controller) - These devices collect the data generated from field equipment on site. Typically do some calculations as well (like SCF and Dekatherms) as well as having logic for controlling pieces of equipment such as control valves and actuators.

3. Communication Networks - Transports the data that the RTU or PLC collects to some other location.  Examples include telephone lines, IP (ethernet), microwave communication, radio communication, satellites, or cell networks.

4. FEP (Front End Processor) - FEP pulls pulls for information and manages the field communications to try and make sure data isn't missed and comes in at optimal times.  This keeps a list of RTU's, communication settings, and manages to pull data when pieces of equipment can't communicate.

5. SCADA (Supervisory Control and Data Acquisition) - This processes the data coming in for status, alarming, and performs advanced calculations.

6. Real Time Interface - Allows user visibility and control of the system.  These tend to be bare-bones displays so the system will run as fast as possible.  Some exceptions to that include safety where you want units to be as easy to identify as possible.  This is the screen you would typically see a person in Gas Control use.

7. Historical Database - These are tables of information that are used for reporting and billing.

### Precision vs Accuracy

Precision and accuracy are two important concepts in measurement. Precision refers to the closeness of repeated measurements to each other, while accuracy refers to how close a measurement is to the true value. A common way to think about these is to imaging a bullseye shooting target. Now suppose you fire several shots at the target.

Precision refers to how tightly grouped the shots are, regardless of where they hit the target. If your shots all hit close together in roughly the same spot, you have high precision. Even if the whole group is far from the bullseye, the shots are still precise in relation to each other.  Accuracy refers to how close your shots are to the actual bullseye. You could fire a shot that hits the bullseye dead center - that would be highly accurate. However, if the rest of your shots are scattered far away from the bullseye, then your overall accuracy is low even though that one shot was accurate.  For good marksmanship (and good measurement), you need both precision and accuracy. Precision ensures your shots are clustered together. Accuracy ensures that tight grouping is centered right on the bullseye.

In gas measurement, the precision of the measurement device, such as a pressure transmitter, determines how consistently it can measure the same pressure of gas across multiple trials. However, high precision alone is not enough - the meter also needs to be accurate to ensure the measured pressure reflects the actual actual. An inaccurate pressure transmitter, even if very precise, will systematically over- or under-estimate the pressure, and ultimately the gas volume. This can lead to significant costs over time for both natural gas suppliers and consumers. Gas measurement needs to balance precision and accuracy. Suppliers rely on accurate measurements to properly bill customers, while consumers rely on them to verify they were charged the right amount. Highly precise but inaccurate meters could lead to unfair over- or under-billing. With proper calibration and maintenance, natural gas equipment can achieve both the precision and accuracy needed for fair and equitable measurement.

When thinking about these qualities in gas measurement equipment, typically, precision is handled by the equipment manufacturer.  It is up to them in order to ensure that their devices are able to get repeatable measurements for the same conditions.  However, accuracy is often in the hands of the operating company, and more importantly, the technicians.  It is normal for measurement equipment to go under wear from normal operations, which can offset what the meter reads.  The technicians need to test equipment and determine if the measurement devices are accurate, and if not, perform a linearization (correction at the RTU level) or calibration (correction at the equipment level) to get the measurements back into tolerance.