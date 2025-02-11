# CMOS Switching threshold and dynamic simulations

- we compared between two cmos one where widths for nmos and pmos are the same and the other cmos is not, we used Static behavior evaluation of a CMOS inverter analysis

![image](https://github.com/user-attachments/assets/14f2a987-6b68-49cf-b1fa-66e85245304c)

- first what do we mean exactly by robustness?


In the context of a CMOS inverter, robustness refers to the ability of the inverter to perform reliably under various conditions and disturbances.

- we started with Switching Threshold which is  The input voltage at which the output voltage is exactly halfway between the high and low logic levels.
This threshold is crucial for ensuring reliable switching, and also Id is the same value for both nmos and pmos but with different directions, becuz both in saturation:

![image](https://github.com/user-attachments/assets/5601dd5a-bf67-4dbf-a7a0-6ba600da7195)

- becuz Id for pmas = Id for nmos we evaluated the follwoing equation, it helps in determining the appropriate dimensions and parameters for the transistors to achieve a desired switching threshold:

![image](https://github.com/user-attachments/assets/506eb726-6533-4f31-82c2-a0718f1b0103)

- next we increased the size of pmos to find the suitable one, which is 1.2v becuz the falling and rising are the closest to each other, but other numbers have benefits:

![image](https://github.com/user-attachments/assets/5dec2730-cb6a-4d00-8c62-701e61192cdf)

How to Use the Table in Physical Design

- Choosing Transistor Sizes:

The table helps in selecting the appropriate PMOS and NMOS sizes to achieve desired performance characteristics.
For example, if you want a balanced rise and fall delay, you might choose a size ratio where the rise and fall delays are closest to each other.
Optimizing Performance:

If minimizing rise delay is critical, you might choose a higher Wp/Lp ratio (e.g., 5 Wn/Ln), which shows the lowest rise delay (37ps).
Conversely, if fall delay is more critical, you might choose a lower Wp/Lp ratio (e.g., Wn/Ln), which shows the lowest fall delay (71ps).

- Balancing Threshold Voltage:

The switching threshold voltage Vm is crucial for ensuring reliable operation. The table shows how Vmchanges with different size ratios.
For instance, if you need a switching threshold close to 1.2V, you would choose the size ratio corresponding to Vm  =1.2V.

- Trade-offs:

The table illustrates the trade-offs between rise delay, fall delay, and switching threshold voltage. Designers can use this information to make informed decisions based on the specific requirements of their circuit.

# Lab

- new mosfet with different widths for nmos and pmos:

![image](https://github.com/user-attachments/assets/dc8fd121-393e-43d0-bf57-bbf0f72d670e)

![image](https://github.com/user-attachments/assets/d5dcf6ca-a9dd-469a-a395-4b60a8588d73)

- transistor analysis, where it starts from 0 to 1.8, shift is 0, rise time is 0.1ns , puls of 2ns and total period time of 4ns:

![image](https://github.com/user-attachments/assets/d52d8ba0-46af-4bbd-a5f2-36c465a48690)

![image](https://github.com/user-attachments/assets/3f1e0de7-a31c-479f-afdb-479f669cfd98)

- falling and rising delay is around 0.9 in, first square for rising and the second for falling:

  ![image](https://github.com/user-attachments/assets/0f970ea3-9697-431e-b29b-a12d4f46263b)

