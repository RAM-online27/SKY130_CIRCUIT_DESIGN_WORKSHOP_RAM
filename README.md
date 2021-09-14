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
    - ![](simulation/day1/A2.PNG)
  
    - ![](simulation/day1/A3.PNG)
  
  Vt - threshold voltage is the minimum Vgs voltage at which strong inversion occurs & contionuous n-channel is formed between source to drain.
  In the absence of Vsb, the threshold value Vt becomes Vto (Vt = Vto) but in the presence of Vsb, the threshold value of Nmos is increased to Vto+V1. **_At Cutoff Region, Vgs<=Vt & Id=0_**
  
  -**_Linear region_**
    - When Vgs is increased slightly beyond Vt (**_Vgs >= Vt_**). The MOSFET enters Linear or Resistive region.On providing voltagr Vsb, Drain current starts to flow from source to  drain & it increases with increase in Vds. 
  **The Drain current was derived to be** 
  
    - ![](simulation/day1/A4_1.PNG)
  
  Approximating (Vds^2)/2 = 0. As it is negligible.
  
    - ![](simulation/day1/A4_2.PNG)
  
  -**_Saturation region_**
   - When Vds is increased above (Vgs-Vt), **[Vds >= (Vgs-Vt)]** Mosfet enters into Saturation Region.The Drain Current does not increase with Vds & reaches steady value.
   - Here in the below example we assume Vgs = 1v , Vds = 0.05v , Vt = 0.45v for the MOSFET.let us analyse for various Vds Values
   
   - ![](simulation/day1/A5_0.PNG)
   
   - Here we can observe, as **Vgs-Vds >= Vt** ,the NMOS enters Saturation region.
   
   - The drain current equation is derived to be
   
   - ![](simulation/day1/A5_1.PNG)
   
  
 ### **_1.3 SPICE SIMULATION_**
   - An Introduction to SPICE SIMULATION was provided. Here we learnt about
     - Technology parameters (provided by foundry technology)
     - Netlist
     - Spice commands
     - These are provided as inputs to SPICE SIMULATION Software.The software simulates with the help of inputs & provides us neccessary characteristic.
    
   ![](simulation/day1/A6_1.PNG)
   
   The Netlist is used to decribe the cicuit.
   
   ![](simulation/day1/A7_0.PNG)
   
   The Typical Charactristic plot (Id vs Vds) of NMOS was simulated using SPICE Software. 
   
   ![](simulation/day1/L1.png)
   
  
## **_Day 2:Effects of Voltge Saturation Effect & Introduction to CMOS_**
- ### **_2.1 Velocity Saturation Effect_**.

  - ![](simulation/day2/A4.PNG)
  - Velocity saturation effect is one of the short channel effect.it is predominant in MOSFET having short channel length ( L<= 0.25u).
  - From the plot ,we coul observe that as Electric field is increased beyond a certain point, the Voltage does not increase & saturates to a steady value.
  - 
- ### **_2.2 Effects of Velocity Saturation Effect_**.

  - ![](simulation/day2/A1.PNG)
     - In this (Id vs Vds) graph we could see that in longer nodes the variation of drain current with respect to Vgs is of Quadratic nature & in shorter nodes the variation        drain current with respect to Vgs is of Linear nature.



  - ![](simulation/day2/A2.PNG)
    - In this (Id vs Vgs) graph, the Quadaratic increase of drain current with respect to Vgs for longer nodes is shown on the left & The linear increase of drain current with respect to Vgs for shorteer nodes is shown on the right.
   
  - ![](simulation/day2/A5.PNG)
    - hence for Mosfet with Shorter nodes, there exist 4 Regions of operation as compared to Mosfet with Longer nodes which has only three regions of operation
    - The Drain current is also modified to account for the Velocity saturation Effect.(Vdsat is a Technology parameter provided by the foundry).

  -  ![](simulation/day2/L1_1.png)  
     - The (Id vs Vds) plot obtained through Simulation for MOSFET with Short Channel(L=0.25u).
     - We can observe linear variation of drain current with respect to Vgs.  
      
  -   ![](simulation/day2/L2_1.png)
      - The (Id vs Vgs) plot obtained through Simulation for MOSFET with Short Channel(L=0.25u).
      - We can observe linear variation of drain current with respect to Vgs.  
    
- ### **_2.3 Introduction To CMOS Logic_**.
  -  ![](simulation/day2/B1.PNG)
     - This is the CMOS logic for the inverter.It is the Series arrangement of PMOS & NMOS,with Drains of the mosfets tied together 
     - Vgsp - Gate to source voltage of PMOS
     - Vdsp - Drain to source voltage of PMOS 
     - Vgsn - Gate to source voltage of NMOS
     - Vdsn - Drain to source voltage of NMOS
     - Vin - Input voltage to CMOS. it is the potential driven at Gate terminals of both NMOS & PMOS.
     - Vout - Output voltage provided to the load.
     - CL   - equivalent capacitance appearing at the load terminals.
     - Vss -  Ground teriminal
     - Vdd -  Supply voltage for NMOS
    
  -  ![](simulation/day2/B2.PNG)
     - Typical inverter logic is : if Vin = High , then Vout = Low & if Vin = Low , then Vout = high. 
     - In the image on the left, We can observe that Equivalent circuit for Vin=Vdd & Vout=0 (PMOS in OFF state & NMOS in ON state)
     - In the image on the right,We can observe that Equivalent circuit for Vin=0 & Vout=Vdd (PMOS in ON state & NMOS in OFF state)
     
  -  ![](simulation/day2/B3_1.PNG)
     - From Observations, Voltage & current Equations for NMOS & PMOS are derived from CMOS circuit.
     - (Id vs Vds) curves are plotted for Both NMOS & PMOS separately

  -  ![](simulation/day2/B6.PNG)
     - With the help of equations & (Id vs Vds) curves, the load curves of NMOS & PMOS are plotted as shown above.
     - We obtained this load ,so as understand the CMOS characteristic in terms of Vin & Vout.( dependency of Vgsn, Vdsn, Vgsp, Vdsp are elimiated in this plot)
  
  -  ![](simulation/day2/B7.PNG)
     - Load curves of both NMOS & PMOS are plotted on same graph
     
  -  ![](simulation/day3/A2.PNG)
     - CMOS Voltage transfer characteristics is finally plotted from load curves of NMOS & PMOS.
    
    
  
     

   
   
  
- Drain current Equation models for different Region of operation 
- Effects of Velocity Saturation Effect & plot
- Introduction to SPICE Simulation ,Netlist,Technology parameters,SPICE commands.
- Plot of Characteristic curves of MOSFET Simulated using SPICE. Emphasis was made on how to create Spice netlist, Spice commands & Technology parameters of MOSFET.
