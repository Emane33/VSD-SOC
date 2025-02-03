# DC and Timing Analysis

- what is pvt?

Integrated circuits are designed in such a way that they can function 
in a wide variety of temperatures and voltages, rather than a single 
temperature and voltage.

- pvt:
  
- process:  There are millions of transistors on the single-chip as we are 
going to lower nodes and all the transistors in a chip cannot have the 
same properties. Process variation is the deviation in parameters of 
the transistor during the fabrication.

- temp: When a chip is operating, the temperature can vary 
throughout the chip. This is due to the power dissipation in the MOStransistors.

- voltage:  As we are going to the lower nodes the supply voltage for a 
chip is also going to less. Let’s say the chip is operating at 1.2V. So, 
there are chances that at certain instances of time this voltage may 
vary.

![image](https://github.com/user-attachments/assets/177f7faa-bcd8-4218-a1d0-8605683d7e1b)

# Lab:-

- installing openSTA from : https://github.com/The-OpenROAD-Project/OpenSTA.git

![image](https://github.com/user-attachments/assets/3a3c3928-ba51-4718-9273-9c95375d5978)


- Static timing analysis using OpenSTA:

- Timing Ananlysis Using In line Commands
  
![image](https://github.com/user-attachments/assets/d987f3eb-2bc4-4632-90c9-098b075d8d21)


- Timing Analysis using TCL file

![image](https://github.com/user-attachments/assets/d28756ef-0ddb-4519-a8ba-377c2e7bdebc)

- Basics  timing analysis

 ![image](https://github.com/user-attachments/assets/a7cbfd84-b9bf-497e-a441-81b7e8f2d758)

- PVT Corner Analysis (Post-Synthesis Timing)

  ![image](https://github.com/user-attachments/assets/1d508d70-92ba-407d-beb7-8f0944ba1e0b)

- WNS
  
  ![image](https://github.com/user-attachments/assets/42aaeee8-54aa-42b8-b102-556f78bc9de1)

- TNS

![image](https://github.com/user-attachments/assets/5f0acbc9-1dd9-4965-b244-3999a0efa149)

- Worst hold slack

  ![image](https://github.com/user-attachments/assets/af9cb23f-bac2-4ec4-b5e6-4c1f2ce063a5)

- Worst setup slack

  ![image](https://github.com/user-attachments/assets/d34764c2-a038-48af-a222-eb681714bc6a)
