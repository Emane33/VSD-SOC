# Good floorplan vs bad floorplan and introduction to library cells

- we can see the floorplan variables with their defaults in floorplan.tcl in configuration folder for OpenLane:

![image](https://github.com/user-attachments/assets/6f5258e7-701d-4708-b005-96346d71723a)

- in picorv32a the variables of OpenLane are sets in its configration file:

 ![image](https://github.com/user-attachments/assets/87676a88-b9a8-4f96-9a4b-11396adfba56)

- before run floorplan, we check the config article by checking latest file generate it:

  ![image](https://github.com/user-attachments/assets/0d61c220-33ba-41b2-83dc-92db3e40eb15)

- to check core util are the same( in yellow) also metal layers are in green, there is alwyas +1 layer in floorplan defualt so the original in picorv32a congif.tcl:

 ![image](https://github.com/user-attachments/assets/97826c96-5e18-496d-b570-7e1b47d43742)

![image](https://github.com/user-attachments/assets/778513e6-28cc-42f1-b127-00fb571748a9)

![image](https://github.com/user-attachments/assets/49603c6b-2d16-47a3-a580-935d8542d919)

- to run floorplan we change run_synthesis to run_floorplan( just show these parts becuz the rest is for placement which we will see later):

  ![image](https://github.com/user-attachments/assets/f38310b2-38d2-4ef4-9a50-413a9aaeb059)
  
![image](https://github.com/user-attachments/assets/de885bf0-72d0-441d-b3a8-c165b5466664)

- content of floorplan def:

![image](https://github.com/user-attachments/assets/fb70e399-86ad-4041-8902-0a1cbd91df36)

- as we see die width is 731615-0 while height is 742335-0, if we divide them by 1000 we get their siezes in microns

- area of die in microns is  731.615 ∗ 742.335 = 543,103.421 square microns

- command to run floorplan in magic:

![image](https://github.com/user-attachments/assets/41b4db0d-de93-4fb3-acfb-91452151a654)

- port layer setting through config.tcl:

  ![image](https://github.com/user-attachments/assets/59493124-20b6-465f-871f-a49405f74d9a)

  - Decap ceels and Tap cells:
 
    ![image](https://github.com/user-attachments/assets/de708e0b-9da7-4e6e-ac6f-6072dd6030c6)

- now we use run_placement command

  ![image](https://github.com/user-attachments/assets/243c582c-9a78-42a2-8b9d-995609a9eff1)

- standard cells legally placed:

![image](https://github.com/user-attachments/assets/753b7b73-afc1-4394-9e9e-fcdc495d18cb)
