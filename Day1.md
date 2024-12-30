 Introduction to Verilog RTL design and Synthesis

-Design can be for one core or multiple cores
-how simultation works?
it looks for the changes on the input signal then evaluattion of output.

-what is synthesizer?
tool used to convert RTL to netlist 
-how to verify it?
use netlist and test bench in iverilog, it should has the same results as RTL design.
![image](https://github.com/user-attachments/assets/c1791a07-d553-40e6-863b-51892c843bb7)

-what is RTL Design?
behivoural representaion of required specefication.

![image](https://github.com/user-attachments/assets/721d2945-c0ea-4295-95be-ec832b78552c)

-what do we mean by synthesis?
convert RTL code into HW view.
-how?
RTL to gate level-> connection is made between gate-> result called netlist.

-what is .lib?
collection of logical modules, it include basic gates like AND but we can have different flavour of same gate like 3 input AND gate.

![image](https://github.com/user-attachments/assets/028edcd7-f1fe-46bd-ae97-7cb99ec58022)

-why do we need different flavour?
combinational delay logicl path determine the max speed of digital logic circuits, so we need cells that works fast to make Tcomb small.
![image](https://github.com/user-attachments/assets/4c58a7d2-3de8-459d-a905-6a9a6560bd71)
-But why do we need slow cells?
to make sure there is no Hold issues in FF, but for performance we need fast cells.
-fast cells VS slow cells:
fast cells are used for bad cicuits in term of power and area. while slow are used for sluggish circuits.

-what is constration?
the guided offered by synthesiser to select flavour of cells.

  Lab:-
we used tb_good_mux file
- first we got the output result in GTKWave:
  
![image](https://github.com/user-attachments/assets/9bd012d6-350d-4dd9-9f47-21462d3e0116)

-second the test bench code:

![image](https://github.com/user-attachments/assets/70c24372-e49d-4167-bb70-7a0c0e164c09)

-third yosys output:

![image](https://github.com/user-attachments/assets/6d316277-aeb9-4845-a3d2-167ff91229fa)

-forth synthesised netlist using gvim:

![image](https://github.com/user-attachments/assets/e1f54912-b275-4981-b01b-0024d63ee194)

