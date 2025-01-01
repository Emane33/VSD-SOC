Combinational and Sequential Optimizations

-is synthesis a push-button solution?

No, becuz you will need it in some places and other not, it depends on your design.

-the more your design become affected by tool methodologies, the more chance of you losing grip over your design vision.

Optimization methdology:-

* sharing resources
  
![image](https://github.com/user-attachments/assets/71f08b52-e2e8-4821-88c8-482f3e73153c)

* cost function:

-synthesis tool preforms optimization by minimizing cost functions( cost for design rule and other for optimization).

-cost function comes in different flavour depend on the EDA tool vendor.

-optimization cost function consist of four parts:

/ max delay cost: has the greatest weight, it is the sum of product of delays and their weight.

/ min delay cost: sum of all min delays where delay is  diffrence between expected delay and actual delay.

/ max power cost: sum of static and dynamic powers multiply by their weight.

/ max area cost: sum of all areas multiply by their weight.

-what is the diffrence between combinational and sequential optimization:

combinational depend on the boolean algebra while sequential depend on it with timing diagram analysis.

Lab:-

optimise 2 inout AND gate:

![image](https://github.com/user-attachments/assets/3cf58019-09b7-4198-9b41-eba63df7e5a0)

optimise 2 input OR gate:

![image](https://github.com/user-attachments/assets/fa50173b-e9ae-42d7-9c0b-e33344d77072)

optimise 3 input AND gate:

![image](https://github.com/user-attachments/assets/6eb6cb00-49e3-42bd-b8f9-b1b4f7ab86a8)

optimise DFF:

![image](https://github.com/user-attachments/assets/6f908217-b2e1-4f72-9b34-351ad0334e29)

![image](https://github.com/user-attachments/assets/54b37850-bc81-4862-8f19-c558b8ad8576)

![image](https://github.com/user-attachments/assets/05caf0ef-4a51-460f-9539-593fd8259c95)

optimise DFF2 where irresepecte to clock and reset q is always one:

![image](https://github.com/user-attachments/assets/e2dc8708-284b-4902-bff9-fca6e5b5cd30)

![image](https://github.com/user-attachments/assets/b3407f7a-ece9-4c14-af9d-feb5d4db2a4a)

![image](https://github.com/user-attachments/assets/b28d0918-1f29-4bb7-870f-476e9b81e05c)

optimise DFF3:

![image](https://github.com/user-attachments/assets/62ec0336-8cd1-4db6-9074-dd5634bdca25)

![image](https://github.com/user-attachments/assets/b7f32758-9ab5-4db9-87a4-bb56c477bde3)

![image](https://github.com/user-attachments/assets/ffcdd4c0-6e6a-44a5-9ceb-e61959e86bae)

optimise unused bits with a counter where q takes bit 0:

![image](https://github.com/user-attachments/assets/c90cf349-c5af-4f27-92ef-03a4934f0b76)

![image](https://github.com/user-attachments/assets/c7bc7238-686a-4b8d-9f21-c56f9be6dc0b)

![image](https://github.com/user-attachments/assets/b3c81b7c-8ca6-4950-8488-3b243812dff7)

optimise unused bits with counter where q takes all bits:

![image](https://github.com/user-attachments/assets/8da70df6-c29e-4f5c-80d3-94adbd572c8a)

![image](https://github.com/user-attachments/assets/2bf84fe9-68f8-4c3f-bf7f-509f25519dd0)

![image](https://github.com/user-attachments/assets/0794c64a-2b5b-46df-9e67-dfc3774da90e)
