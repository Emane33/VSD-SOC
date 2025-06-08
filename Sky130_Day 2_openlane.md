# Good floorplan vs bad floorplan and introduction to library cells

- we can see the floorplan variables with their defaults in floorplan.tcl in configuration folder for OpenLane:

![image](https://github.com/user-attachments/assets/6f5258e7-701d-4708-b005-96346d71723a)

- in picorv32a the variables of OpenLane are sets in its configration file:

 ![image](https://github.com/user-attachments/assets/87676a88-b9a8-4f96-9a4b-11396adfba56)


- to run floorplan we change run_synthesis to run_floorplan

- content of floorplan def:

  ![image](https://github.com/user-attachments/assets/a2d5ecd1-4b63-4bef-af51-07ed3c66e221)

- as we see die width is 660685 while height is 671405, if we divide them by 1000 we get their siezes in microns

- area of die in microns is  660.685 ∗ 671.405 = 443587.21 square microns

- floorplan in magic:

![image](https://github.com/user-attachments/assets/caf114a6-a0d2-4d78-ac52-5069da6a2c9b)

- port layer setting through config.tcl:

  ![image](https://github.com/user-attachments/assets/59493124-20b6-465f-871f-a49405f74d9a)

  - Decap ceels and Tap cells:
 
    ![image](https://github.com/user-attachments/assets/de708e0b-9da7-4e6e-ac6f-6072dd6030c6)


- now we use run_placement command

  ![image](https://github.com/user-attachments/assets/243c582c-9a78-42a2-8b9d-995609a9eff1)

- standard cells legally placed:

![image](https://github.com/user-attachments/assets/753b7b73-afc1-4394-9e9e-fcdc495d18cb)
