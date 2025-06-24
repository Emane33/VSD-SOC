- day 3 was done in name of Day 16

# Pre-layout timing analysis and importance of good clock tree

-  tracks.info of sky130_fd_sc_hd, where you define where your routes go:

![image](https://github.com/user-attachments/assets/c155fad6-c84b-4f1a-9e76-74e8b58a7460)

![image](https://github.com/user-attachments/assets/349bc326-c190-4883-803f-6804b9bac54a)

- grided magic using the info of li1 in tracks.info:

  ![image](https://github.com/user-attachments/assets/0131bf7b-898a-41d5-ae2d-cbdef5cdcc39)

  - as we see A and Y are in the horizontal so route can reach them :
 
  ![image](https://github.com/user-attachments/assets/9cdc76c4-4d0f-4560-836c-1157fe5bccca)

- to save magic file for lef:

  ![image](https://github.com/user-attachments/assets/fae8c69d-4980-4cb0-9782-fe902caeb0a5)

- now in the new file we created, we write this command:

![image](https://github.com/user-attachments/assets/2be393a8-6571-485e-b759-05f8b6da39ac)

- here is out new lef file:

![image](https://github.com/user-attachments/assets/057de31e-9e3c-4573-9507-1c3175833a14)

- copy the new generated lef file and required files to src in picorv32a:

![image](https://github.com/user-attachments/assets/9ac916a5-771a-4fff-9d27-7561d5491a94)

![image](https://github.com/user-attachments/assets/2f09fb02-f6d0-4b70-b80d-7424d66465f3)

- what should be in the config.tcl file:

![image](https://github.com/user-attachments/assets/abe5b9b8-cce2-4811-8d65-e032ff73615f)

- run this after prep command, then run_synthesis:

  ![image](https://github.com/user-attachments/assets/4e720928-aa4c-447e-b87c-f667ce4f9042)

-  design parameters to reduce the newwly introduced violations with the introduction of custom inverter cell:

![image](https://github.com/user-attachments/assets/8e8a6c58-fe2a-46e8-b45d-1ca35cf9f86c)

![image](https://github.com/user-attachments/assets/55ac8916-7808-49ac-b61f-c61df03e4586)

- command to view and change parameters for better timing, the re run synthesis:

![image](https://github.com/user-attachments/assets/7a3aeb5a-b324-4838-9269-607f72163bad)

![image](https://github.com/user-attachments/assets/9074e9e4-7160-4fa9-90d2-0ffd0d057c1d)

- the new parameters:

![image](https://github.com/user-attachments/assets/5826bf06-8c1b-485a-b5a9-f36e727a32a6)

![image](https://github.com/user-attachments/assets/b45f3c72-fbdd-4181-9ceb-cc37a8cd5094)

- if we run floorplan we will find an issue, to solve it:

![image](https://github.com/user-attachments/assets/732961e0-b411-4326-a719-708a5077a1ed)

![image](https://github.com/user-attachments/assets/683679cc-28d0-4429-a3f3-212effec37d0)

- after running placement we open magic:

![image](https://github.com/user-attachments/assets/7374c903-be38-4ef9-8977-5de56c030c38)

![image](https://github.com/user-attachments/assets/9d333b2b-3516-4db9-8e85-67d72f0ffcbb)

- after we search for sky130_vsdinv and then write expand:

![image](https://github.com/user-attachments/assets/703810c0-a932-4f84-bc7a-dac035c97baa)

- to do timing analysis for the initial run:

  ![image](https://github.com/user-attachments/assets/bd60be83-2e33-49d4-9644-344a23353ff8)

- created pre_sta.conf in openlane:

![image](https://github.com/user-attachments/assets/b1e5e207-5061-4cdf-b617-4a2694f53115)

- in picorv32a/src my_base.sdc was created:

  ![image](https://github.com/user-attachments/assets/554be03a-26b5-4990-be3b-a9cb8b1a018c)

- to run STA in terminal:

![image](https://github.com/user-attachments/assets/16774c00-ed69-47f0-830b-03b2c0d7ee9b)

![image](https://github.com/user-attachments/assets/9e6ced55-4b68-4063-98b6-cd4fe6310bb3)

![image](https://github.com/user-attachments/assets/25a1c328-df50-4a26-8f4c-1c2bcf706faa)

![image](https://github.com/user-attachments/assets/ed7570f2-74d7-4c9c-a3f1-a59e75db0f78)

- to reduce fanout which is causing more delay:

  ![image](https://github.com/user-attachments/assets/2bf576c0-7bdc-4554-9467-03f5a1ce805b)

![image](https://github.com/user-attachments/assets/8d3e909f-0f01-45f3-b406-1448ad5ac0aa)

- now re-run pre_sta:

![image](https://github.com/user-attachments/assets/ab67d320-9fec-4ac6-8f66-a7724384561f)

![image](https://github.com/user-attachments/assets/077426c1-2f38-4696-9322-4978d387e706)

- we have an issue that or3_2 is driving 4 fanout, to solve it:

  ![image](https://github.com/user-attachments/assets/6b60bb82-8c55-4dfd-aa03-2d580bf6be91)

![image](https://github.com/user-attachments/assets/558983b6-a843-46b3-bdbd-bc5b61170448)

![image](https://github.com/user-attachments/assets/44db79bd-4858-4b1f-968f-ed4277af85ce)

![image](https://github.com/user-attachments/assets/ac70b308-eabc-4cef-af5c-7617a3f01ed7)

- to replace the netlist with the new netlist generated after CEO timing:

![image](https://github.com/user-attachments/assets/92f1d91c-a5d2-4991-8d8a-b5a4ddcc40e2)

![image](https://github.com/user-attachments/assets/85c2e1ca-7848-4189-8ce1-b47ef587e095)

![image](https://github.com/user-attachments/assets/1bb20790-5dd7-4aa4-acfc-ad23ce3c7177)

![image](https://github.com/user-attachments/assets/c261ca18-9f8c-41ab-ad99-0eb7753dc1c9)

![image](https://github.com/user-attachments/assets/cda65865-687b-45fd-8c60-db19e3c253f4)

![image](https://github.com/user-attachments/assets/18d7c5cf-e264-4e1d-a35f-7d89e8d5c797)

![image](https://github.com/user-attachments/assets/c49dd15c-1f34-4098-b12a-ff265f1bf926)

- POST-CTS openroad timing analysis:

![image](https://github.com/user-attachments/assets/b7cdaf68-a516-4c49-be22-e8fb6064245f)

![image](https://github.com/user-attachments/assets/5b4ec142-7d82-46d0-b5a3-b6483d112afd)

![image](https://github.com/user-attachments/assets/b7e1fb4e-517c-49ea-93eb-f8a5e631ceaa)

![image](https://github.com/user-attachments/assets/17590a9b-7695-4f1e-9544-67316e833b21)

![image](https://github.com/user-attachments/assets/b393ab36-db0d-489b-8c0b-7686cfc7406e)
