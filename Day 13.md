# Post-synthesis simulation

- what is the diffrence between synthesizable and non- synthesizable constructs in verilog.

Synthesizable Constructs: Can be converted into hardware, used for actual design implementation.

Non-Synthesizable Constructs: Cannot be converted into hardware, used for simulation and verification.

- what is the diffrence between post and pre synthesis?

Pre-Synthesis: High-level RTL description, focuses on functional verification, idealized timing, easier to modify.

Post-Synthesis: Gate-level netlist, focuses on timing and physical implementation, accurate timing, more difficult to modify.

- GLS: a brief introduction
  
 The term "gate level" refers to the netlist view of a circuit, usually produced by logic synthesis.

 So while RTL simulation is pre-synthesis, GLS is post-synthesis. 

 The netlist view is a complete connection list consisting of gates and IP models with full functional 
and timing behavior. 

RTL simulation is a zero delay environment and events generally occur on the active clock edge. 

GLS can be zero delay also, but is more often used in unit delay or full timing mode. 

What are we going to synthesize the netlist with?

We will be using synopsys’s DC shell(Design Compiler)

# Lab:-

- Run synthesis targeting vsdbabysoc

  ![image](https://github.com/user-attachments/assets/a704e1f4-8718-48c5-b7db-c64fd2bd81e5)

![image](https://github.com/user-attachments/assets/901a9fc6-8cfb-49f4-a675-6139819e0bfe)

![image](https://github.com/user-attachments/assets/b6d64e7e-03c8-4ead-b06a-984c1505b759)

![image](https://github.com/user-attachments/assets/4eb5f2b6-87dd-4c6a-be07-1289bba0a28f)

- Map D Flip-Flops to Standard Cells

![image](https://github.com/user-attachments/assets/983496b4-7d2c-49c6-b4c9-9c7d0286a90b)

-  Perform Optimization and Technology Mapping

![image](https://github.com/user-attachments/assets/8a979b59-2c1f-4027-ab57-b47b87b41e65)

- Perform Final Clean-Up and Renaming

  ![image](https://github.com/user-attachments/assets/3510fbc6-ba92-4fef-bc8f-08fc366f51e9)

- Check Statistics

  ![image](https://github.com/user-attachments/assets/0e8ed825-2bf1-4886-af40-f309c9fa7852)

![image](https://github.com/user-attachments/assets/65344456-1243-4851-bc23-e2a28312ca51)

- Write the Synthesized Netlist

  ![image](https://github.com/user-attachments/assets/505a7150-a26d-4a22-91ae-0590dc90c41a)

- gtkwave

![image](https://github.com/user-attachments/assets/96884c74-07ca-4c24-aa7a-8e9654944e57)
