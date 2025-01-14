# VSDBabySoC Modelling

- What does modelling mean?(electronics terminology)

Modeling and simulation is the use of a physical or logical representation of a given system to generate
data and help determine decisions or make predictions about the system.
Models are representations that can aid in defining, analyzing, and communicating a set of concepts.

- what is the diffrence between modeling and simulation?

Modeling: Focuses on constructing a simplified representation of a system to understand and predict its behavior.

Simulation: Focuses on executing the model to observe and analyze the system's behavior over time.

- what are we modeling?

Some initial input signals will be fed into vsdbabysoc module, That will get the pll start generating the proper CLK for the circuit. The clock signal will make the rvmyth to execute instructions and some
values are generated, these values are used by DAC core to provide the final output signal named OUT. So we have 3 main elements (IP cores) and a wrapper as an SoC and of-course there would be also a testbench module out there.

#  VSDBabySoC IPs

- RVMYTH - Risc-V based MYTH (Microprocessor for You in Thirty Hours)
RISC stands for Reduced instruction set computer
RISC-V(pronounced “risk-five”) ISA is defined as a base integer ISA, which must
be present in any implementation, plus optional extensions to the base ISA.
Each base integer instruction set is characterized by the width of the integer
registers and the corresponding size of the address space and by the number of
integer registers. There are two primary base integer variants, RV32I and RV64I.

- A phase-locked loop (PLL) is an electronic circuit with a voltage or voltage-driven oscillator that constantly
adjusts to match the frequency of an input signal.
PLLs are used to generate, stabilize, modulate, demodulate etc

![image](https://github.com/user-attachments/assets/a8e77849-ae7f-4dcf-be8b-e099d153a059)

- A Digital to Analog Converter (DAC) converts a digital input signal into an analog
output signal.
The digital signal is represented with a binary code, which is a combination of bits
0 and 1. A Digital to Analog Converter (DAC) consists of a number of binary inputs
and a single output. In general, the number of binary inputs of a DAC will be a power of two.

● There are two types of DACs :

○ Weighted Resistor DAC: A weighted resistor DAC produces an analog output, which is almost equal to the
digital (binary) input by using binary weighted resistors in the inverting adder
circuit. In short, a binary weighted resistor DAC is called as weighted resistor
DAC.

![image](https://github.com/user-attachments/assets/2028ce41-497c-4514-b95a-c5f74683e2b5)

○ R-2R Ladder DAC: The R-2R Ladder DAC overcomes the disadvantages of a binary weighted
resistor DAC. As the name suggests, R-2R Ladder DAC produces an analog
output, which is almost equal to the digital (binary) input by using a R-2R ladder
network in the inverting adder circuit.

![image](https://github.com/user-attachments/assets/b9bae67f-660d-48ce-931a-cb71742ba60c)

# Lab:-

- modelling RVMYTH(RISC-V)

![image](https://github.com/user-attachments/assets/fda0e949-cc86-4ba1-9cdd-478fff6758f4)

- modelling DAC

![image](https://github.com/user-attachments/assets/b88eb4a1-d8fd-445a-92a5-f2e6ed2ba948)

- modelling pll

![image](https://github.com/user-attachments/assets/c98f24ac-776c-4271-b062-4d352c5d29b9)

- simulate risc_v and pll 

![image](https://github.com/user-attachments/assets/71e84899-5d8c-4519-afdc-1668770f4538)


- simulate  DAC and RVMYTH

![image](https://github.com/user-attachments/assets/e578a084-76a7-4f73-aaca-e093e0a9430b)
