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
