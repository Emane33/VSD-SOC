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
