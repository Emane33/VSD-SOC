# Introduction to the BabySOC

- What is SoC?
  
A System on Chip (SoC) is an integrated circuit that consolidates all the essential components of a computer or other electronic system onto a single chip.
This includes the central processing unit (CPU), memory, input/output ports, and secondary storage, along with other specialized functions

- why we use it?
  
By integrating multiple components onto a single chip, SoCs reduce the need for separate chips and interconnections, leading to more compact and efficient designs.

- what is the diffrence between SoC and motherboard?
  
Motherboard: A large, complex PCB that connects and integrates all the components of a computer or electronic device.
SoC: A small, highly integrated chip that consolidates all essential components of a system onto a single chip.

- SoC structure: An SoC consists of hardware functional units, including microprocessors that run software code,
as well as a communications subsystem to connect, control, direct and interface between these
functional modules

- SoC Design flow:
  
![image](https://github.com/user-attachments/assets/f540cc70-3307-40b9-b634-7b260e535170)

# introduction to BabySoC

- what is BabySoC?
  
VSDBabySoC is a small yet powerful RISCV-based SoC. The main purpose of designing such a small SoC is to test three open-source IP cores together for the first time and calibrate the analog part of it.
 VSDBabySoC contains one RVMYTH microprocessor, an 8x-PLL to generate a stable clock, and a 10-bit DAC to communicate with other analog devices.

![image](https://github.com/user-attachments/assets/362dd0eb-b6ff-4e8f-9352-8f5cf6cde05e)

- what are its components:
  
RVMYTH: RVMYTH core is a simple RISCV-based CPU

PLL: A phase-locked loop or PLL is a control system that generates an
output signal whose phase is related to the phase of an input signal.
PLLs are widely used for synchronization purposes, including clock
generation and distribution

DAC: A digital-to-analog converter or DAC is a system that converts a
digital signal into an analog signal. DACs are widely used in modern
communication systems enabling the generation of digitally-defined
transmission signals.

# Lab:-

