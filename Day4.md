GLS, blocking vs non-blocking and Synthesis-Simulation mismatch

- we conduct zero delay simulation, as we are focusing on synthesis and simulation mismatch at pre-layout level.
- also used in dynamic timing analysis as it is able to take in account various clock and reset at the same time, and thus give insight about synch performance which STA ( start timing analysis) is not meant for.

Blocking assignments:
- execution of blocking assignments can be viewed as one step process:
* evaluate the RHS( right hand side expression) and update LHS of blocking assignments without interruption from any other verilog statments.
* A blocking assignments 'blocks' trailing assignments in the same always block from occuring until current assignment has been completed.

![image](https://github.com/user-attachments/assets/ba3aead4-5fdf-43c5-9be8-765ae01da859)

Nonblocking assignments:
- it is like (<=) operator.
- they are only made to register data types and therefore only permittes inside of procedural blocks, such as intial block and always block.
- non blocking assignments are not permitted in continous assignment.
- it doesn't block other verilog statments from being evaluated.
- execution can be viewed as two-step process:
* evalutaion the RHS of nonblocking statments at the begining of the time step.
* update the LHS of nonblocking statments at the end of time step.

![image](https://github.com/user-attachments/assets/e0ea71cc-7c01-4109-b898-919f47e1527e)

RTL coding guidelines:
- do not blocking assignmets in the same always block.
- do not make assignments to the same variable from more than one always block.
- combinational( always@*) -> blocking (=) assignments.
- sequential( always @posedge) -> nonblocking ( <=) assignments.
- always sperate sequentioal and cominational logic.

Simulation synthesis mismatch:
- incomplete sensitivity lists, synthesizer may ignore them, but simulator won't.
- compelete sensitivity list with misordered assignments( ex. modeling sequential logic using blocking assignment).
- timing delay.

Lab:-

- synthesis simulation mismatch:
  
ternary_operator_mux:

![image](https://github.com/user-attachments/assets/daab4142-b824-4b85-b10a-820f89c0aa0e)

![image](https://github.com/user-attachments/assets/e4e445e6-feff-4e20-ac1a-15a08038e67e)

*there is 6,7,8 which shows it is GLS 

![image](https://github.com/user-attachments/assets/d990bc34-6270-43e8-9d94-fff60eeabb0d)

bad mux:

![image](https://github.com/user-attachments/assets/d0cda97c-661c-438d-8513-9e6d5e121448)

![image](https://github.com/user-attachments/assets/d8babe96-b2e3-41ac-a0a1-edb90e76f8f0)

![image](https://github.com/user-attachments/assets/cee69d88-9439-4ada-8554-a0b17035228f)

GLS:

![image](https://github.com/user-attachments/assets/0de1c951-5c80-4320-8514-7ca51be84ab9)

- blocking and nonbloking:

![image](https://github.com/user-attachments/assets/fe2540cc-c3f6-49c6-ab8f-a481af379a03)

![image](https://github.com/user-attachments/assets/8d149a74-87a4-4322-88e2-79059eae6a79)

![image](https://github.com/user-attachments/assets/727679e9-d2fe-45fb-9be1-5877761956b8)

GLS:

![image](https://github.com/user-attachments/assets/0b2b3829-0346-4e41-8663-f12701ce8f6b)
