# SKY130 CMOS CIRCUIT DESIGN & SPICE SIMULATION
![](simulation/Banner.jpg)
## **_Overview of the course_**
In this 'CMOS CIRCUIT DESIGN & SPICE SIMULATION WORKSHOP' conducted by [VLSI System Design]( https://www.vlsisystemdesign.com/).We have learned About MOSFET construction,Regions of Operation,characteristic curves ,Drain current equation models.Factors such as velocity saturation effect that affect MOSFET operation was also discussed .CMOS logic for inverter is introduced & it's Voltage transfer characteristics are studied.Effects on varying the PMOS channel dimensions on Switching threshold voltage,Delays,Noise margins are studied,Emphasis was made on Robustness of CMOS during the study.Finally the effect of varying power supply input of CMOS on Voltage transfer characteristics,Gain,Energy consumption & performance(delays) were studied.All the above topic were discussed in detail theoretically & are also simulated using SPICE SIMULATION.The Simulation results obtained are found to be inaccordance with the Theory that was discussed.
## **_Summary of the 5 Day Workshop-Daywise_**
## **_Day 1:Intoduction to MOSFET & Spice Simulation_**
- ### **_1.1 MOSFET(NMOS)BASICS_**.
  
    

 ![](simulation/day1/A1.PNG)
  - NMOS Construction  
    - MOSFET has four terminals G= GATE D= DRAIN S=SOURCE B=BODY
    - Gate oxide is made up of SiO2 layer that acts as insolation.
    - Metal gate is place over the gate oxide layer 
    - it has a P-type Substrate  
- ### **_1.2 Regions of operation & conditions needed to operate in the region_**
  - Typically MOSFET has three regions of operation 
    - Cutoff region
    - Linear or Resistive region
    - Saturation region
    
  - **_Cutoff region_**
  ![](simulation/day1/A2.PNG)
  
  ![](simulation/day1/A3.PNG)
  
  Vt - threshold voltage is the minimum Vgs voltage at which strong inversion occurs & contionuous n-channel is formed between source to drain.
  In the absence of Vsb, the threshold value Vt becomes Vto (Vt = Vto) but in the presence of Vsb, the threshold value of Nmos is increased to Vto+V1. **_At Cutoff Region, Vgs<=Vt & Id=0_**
  
  -**_Linear region_**
  When Vgs is increased slightly beyond Vt (**_Vgs >= Vt_**). The MOSFET enters Linear or Resistive region.On providing voltagr Vsb, Drain current starts to flow from source to  drain & it increases with increase in Vds. 
  **The Drain current was derived to be** 
  
  ![](simulation/day1/A4_1.PNG)
  
  Approximating (Vds^2)/2 = 0. As it is negligible.
  
  ![](simulation/day1/A4_2.PNG)
  
  -**_Saturation region_**
   When Vds is increased above (Vgs-Vt), **[Vds >= (Vgs-Vt)]** Mosfet enters into Saturation Region.The Drain Current does not increase with Vds & reaches steady value.
   Here in the below example we assume Vgs = 1v , Vds = 0.05v , Vt = 0.45v for the MOSFET.let us analyse for various Vds Values
   
   ![](simulation/day1/A5_0.PNG)
   
   Here we can observe, as **Vgs-Vds >= Vt** ,the NMOS enters Saturation region.
   
   The drain current equation is derived to be
   
   ![](simulation/day1/A5_1.PNG)
   
  
 ### **_1.2 SPICE SIMULATION_**
   
   ![](simulation/day1/A6_1.PNG)
   
   ![](simulation/day1/A7_0.PNG)
   
   ![](simulation/day1/L1.png)
   
  
   
   
   
  
- Drain current Equation models for different Region of operation 
- Effects of Velocity Saturation Effect & plot
- Introduction to SPICE Simulation ,Netlist,Technology parameters,SPICE commands.
- Plot of Characteristic curves of MOSFET Simulated using SPICE. Emphasis was made on how to create Spice netlist, Spice commands & Technology parameters of MOSFET.
