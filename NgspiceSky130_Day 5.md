# CMOS power supply and device variation robustness evaluation

- we decreased the power supply in cmos which is represented in this chart:

![image](https://github.com/user-attachments/assets/03974aad-cd15-4f88-a443-eaad11c68de8)

- we noticed that the gain which is the change in output voltage over change in input voltage, is higher in 0.5v supply with 56% diffrence with 2.5v.

- also there is a 96% energy reduction from 2.5 to 0.5.

- however the falling and rising delays are high in 0.5 which make it slower.

  ----------------------------

  - due to fabrications issues we might not get the idle oxide thikness and gate wedith/lenght, this effects our Id according to the follwoin equation:
 
  ![image](https://github.com/user-attachments/assets/b10b10e4-cb1a-4f62-983e-cb063de934d6)

 - as you can see in the following code, we are making weak pmos and strong nmos by decreasing the pmos width and increasing it for nmos.

![image](https://github.com/user-attachments/assets/8b13c03a-3ea5-4dc7-902b-89abbb2a3b4b)

- the below chart shows the diffrence condtions for the previous code, we see shift in Vm, and decrease in NML and NMH regions.

![image](https://github.com/user-attachments/assets/c4f1ba2f-9371-4654-b238-075c980c1624)


  # Lab:-

  - as you can see we made the decreasing condition at the bottom:
 
  ![image](https://github.com/user-attachments/assets/3f80baa3-836b-4746-95c9-06b35504ba03)

  ![image](https://github.com/user-attachments/assets/ffb00a94-2058-4713-b0ce-c3cd23f50101)

- for device variation, pmos hold v for longer time thane nmos, which make it strong while nmos weak:

![image](https://github.com/user-attachments/assets/3d6afbf5-cf28-4f76-ba01-5323a07d1133)

![image](https://github.com/user-attachments/assets/b88bc29d-32ba-4b75-b14c-c466d3f75eae)
