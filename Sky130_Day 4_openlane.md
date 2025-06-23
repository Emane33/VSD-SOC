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

