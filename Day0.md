# Day0
tools installtion : yosys , gtkwave, magic, VB(linux ubuntu) , iverilog.


introduction:
![image](https://github.com/user-attachments/assets/b48a4ba3-d995-44b9-8834-498bfd0f1772)

1- The first step in creating a processor is to decide the specification.

2- Then, a soft copy of the hardware (HW) is created, which is RTL using Verilog.

3- We divide the Verilog code into:

-Processor (synthesis into gate-level netlist)

-Peripheral (synthesis to macros)

-IPs (convert analog to digital but not synthesis, using MOSFETs)

4- SoC integration: defining GPIOs.

5- When we use Verilog for the processor, it is a microprocessor. If we add peripherals, IPs, and GPIOs, it becomes a microcontroller.

6- Then we move to physical design, like floorplanning, etc.

7- Tape-out: the process of sending the GDSII file after DRC/LVS checks to the factory.

8- Tape-in: receiving your own chip.

9- At the end, we put pins around the chip to function.
