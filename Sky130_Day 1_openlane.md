# Inception of open-source EDA, OpenLANE and Sky130 PDK

![image](https://github.com/user-attachments/assets/1f606aa3-66d0-4d98-a161-4bd0b49f433c)

- what is RLT to GDSII flow?

The RTL to GDSII flow is the standard design process used in semiconductor engineering to transform a high-level Register Transfer Level (RTL) description of a digital circuit into a GDSII file, which is the final layout format used for manufacturing an integrated circuit (IC).

- stages:

1- RTL Design & Verification: The design is described in Hardware Description Language (HDL) like Verilog or VHDL at the Register Transfer Level, Functional verification is done using simulation tools (e.g., Synopsys VCS, Cadence Xcelium), Formal Verification (FV) ensures RTL matches the golden reference.

2- Logic Synthesis: RTL is converted into a gate-level netlist using a standard cell library, Tools: Synopsys Design Compiler, Cadence Genus, Optimizations for area, power, and timing are applied.

3- Floorplanning: Defines the chip’s die size, macro placement, and power grid, Ensures efficient placement of memory, IP blocks, and I/O pads.

4- Placement: Standard cells from the synthesized netlist are placed optimally, Global Placement: Rough placement for timing/area, Detailed Placement: Fine-tuning for legal cell positions.

5- Clock Tree Synthesis (CTS): Builds a balanced clock distribution network to minimize skew, Ensures all flip-flops receive the clock signal with minimal delay variation.

6- Routing: Metal interconnects are created to connect all placed cells, Global Routing: Establishes approximate paths, Detailed Routing: Finalizes metal layers (e.g., M1–Mx).

7- Physical Verification & Signoff: Design Rule Checking (DRC): Ensures manufacturability (e.g., spacing, width rules), Layout vs. Schematic (LVS): Confirms netlist matches layout, Timing Signoff: Static Timing Analysis (STA) checks setup/hold times (using PrimeTime), Power Analysis: IR drop and electromigration checks.

8- GDSII Generation: The final layout is exported in GDSII (a binary file format for mask fabrication), Sent to the foundry ( Samsung, etc.) for tape-out and manufacturing.

- what is OpenLane?

  OpenLane is an open-source, automated RTL-to-GDSII flow for digital ASIC (Application-Specific Integrated Circuit) design. It is maintained by the OpenROAD project and is widely used in academia, research, and open-source chip design initiatives, OpenLane integrates multiple open-source EDA (Electronic Design Automation) tools to automate the entire process of transforming RTL (Verilog/VHDL) into a manufacturable GDSII layout, making it accessible to designers without expensive proprietary toolchains.

- what does it support for PDKs?

it Works with SkyWater 130nm, GF180nm, and others.

- OpenLane ASIC flow:

  ![image](https://github.com/user-attachments/assets/c3a48dd2-bc26-417f-a253-5791f1ff5643)


# SKY130_D1_SK3 - Get familiar to open-source EDA tools

- used  this repo as refrence:https://github.com/fayizferosh/soc-design-and-planning-nasscom-vsd?tab=readme-ov-file

- for this workshop we will be using sky130A as pdk

  ![image](https://github.com/user-attachments/assets/03c9e845-b177-4ee0-a54d-95b31d2faf29)

- open_pdks: Automatic setup of PDKs for open-source tools from foundry sources, source files from: https://github.com/RTimothyEdwards/open_pdks.git

- sky130A :  the pdk that whast used for our open source  environement:

  ![image](https://github.com/user-attachments/assets/fae77774-c7da-47e5-8f18-c23b1a37d095)

- lib.lef: contains technology like cells, timining..etc

- libs.tech: files specefic to the tool

- opening  openlane in docker:

  ![image](https://github.com/user-attachments/assets/c9c0e04d-e88d-4747-8697-95bfdeaf6559)

- using interactive mode( OpenLane's Interactive Mode allows designers to pause, inspect, and modify the design at different stages of the RTL-to-GDSII flow instead of running everything automatically in one go. This is useful for debugging, optimization, and learning how each step affects the design):

  ![image](https://github.com/user-attachments/assets/651b28dd-85e5-40e1-8348-8532fa129a57)

 - entring the required package:

  ![image](https://github.com/user-attachments/assets/d9d879c8-269a-43ca-b286-268c9f60985f)

- we are going to use picorva32 design

  ![image](https://github.com/user-attachments/assets/1f36bd4d-9fb4-4de5-91be-cf1a86ff3c9b)

![image](https://github.com/user-attachments/assets/149f7e87-2e9c-4115-8b51-7b6879558cbb)



- running synthesis using run_synthesis command to calculate DFF percent:-

 - on blue is counter FF while orange is number of cells:

![image](https://github.com/user-attachments/assets/f999347c-7a03-4728-ae38-cdd8d1a80b0b)


-  Flop Ratio and DFF perecent is 1613/15134 * 100 = 10.65%
