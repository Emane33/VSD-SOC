# Velocity saturation and basics of CMOS inverter VTC


![image](https://github.com/user-attachments/assets/3ce80c94-85a9-463e-850f-f7896a692814)

- we split the graph due to different action in the two regions, the split point is vds = vgs - vt, if vds exceed them it enters saturation region
other wise it has a linear behaviour.

- in the saturation region, the MOSFET is fully on, and the current flowing through it is at its maximum and relatively constant, mostly controlled by the gate-source voltage Vgs
. It's like a fully open faucet letting water flow freely.

-In the linear (active) region, the MOSFET operates as a controllable resistor. The current flowing through it is directly proportional to the drain-source voltage Vds
 and can be finely adjusted by varying Vds
 and Vgs. It's like adjusting the flow of water by partially opening the faucet.

 ![image](https://github.com/user-attachments/assets/fa5aec52-1b55-44bc-bddf-739733b1f68a)

- here we compare different MOSFET lengths and widths.

- as first observation, at 2.5 v we see a quadratic dependence with increase in gate voltage as in the equation.

  ![image](https://github.com/user-attachments/assets/507621af-d10e-4748-b351-5006fc2aeef8)

 on the other hand, we see a quadratic increase, but then it turns to linear due the velocity saturation effect.

![image](https://github.com/user-attachments/assets/18ff12be-e1b7-40e8-ae5b-2974445b5d2c)

- with more deep analysis, by changing vin to be from 0 to 2.5 v with 0.1 step  while vds to same but with 2.5 as step, we can see the difference clearly
where in the right is the shorter channel mosfet with linear increase and on the left the quadratic increase for the longer mosfet.

- but what is velocity saturation effect?

  The velocity saturation effect in MOSFETs occurs when the electric field along the channel becomes so strong that the velocity of the charge carriers (electrons or holes) reaches a maximum limit, known as the saturation velocity.
   Beyond this point, increasing the electric field does not result in a proportional increase in carrier velocity.

![image](https://github.com/user-attachments/assets/cc8c6a21-0160-4914-a0f2-e32ddb13802d)

- with this model eq we come up with, we can understand the diffrenet operations of mofset depending on the channel.

- vds for resistive, vgt for saturation and vdsat for velocity saturation.

  ![image](https://github.com/user-attachments/assets/0b9c82f8-29d5-4fdf-8f18-79fea95ce427)


- velocity saturation lead to device saturate early.

# Lab
