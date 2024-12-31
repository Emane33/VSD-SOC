Timing libs, hierarchical vs flat synthesis and efficient flop coding styles

-what is constitues of gate?

MOSFET utilise for specifiying the circuits physically and charachterizing them elcetrically.

-what is 130 in sky130 library?

nanometer, the distance between channels in MOSFET.

-what is D-FF?

flip flop works as memory element in digital design.

-what is hierarchical and flat design?

used for coherntcy, it uses the full components like full adder, while in flat design it is only gates.

![image](https://github.com/user-attachments/assets/2e361ca6-5502-4192-b758-66d7bd639655)

flat:

![image](https://github.com/user-attachments/assets/bd851097-bb56-4477-9769-72ab99492ecc)

Lab:-

introduction to time lib:

-tt for typical , 025C for temp, 1v80 voltage which is 1.8

![image](https://github.com/user-attachments/assets/2e4ea214-1ce8-4792-a6b7-3e7b96f83b76)

hierarchy synthesis code and schematic: 
![image](https://github.com/user-attachments/assets/1a54a2ee-b57d-4304-868a-6fa6277ee2aa)
![image](https://github.com/user-attachments/assets/32f51034-6cee-44b6-9d28-75485d24e563)

flat synthesis code and schematic:
![image](https://github.com/user-attachments/assets/c801bc0b-9e43-43da-a427-7e7d355af9e8)
![image](https://github.com/user-attachments/assets/3d485335-eeb5-4dd4-b140-9651211783b1)

sub-model level synthesis:
when we have multiple income of same module or massive module 
![image](https://github.com/user-attachments/assets/0f60381f-fb64-4e4f-a8aa-5b6332584861)
![image](https://github.com/user-attachments/assets/a2bc4c1c-efc1-4e1a-8899-ba86e4332e0c)

D-FF:-
Asynch with reset:
![image](https://github.com/user-attachments/assets/7047f858-edba-47bb-925f-efe79cfb8ac0)
![image](https://github.com/user-attachments/assets/c6785f13-ddab-47d4-9c6e-e6c65cd58b22)

Asynch with set:
![image](https://github.com/user-attachments/assets/e595404b-d395-4c06-998b-607f1e7ef7d8)
![image](https://github.com/user-attachments/assets/d69b4291-c326-4cef-8516-3bf49f52ef39)

Synch with reset:

![image](https://github.com/user-attachments/assets/c5333ca7-3f11-46f6-a463-4423c9f856a6)

![image](https://github.com/user-attachments/assets/1f32f51e-a7b4-483e-abff-ee891743a64f)

Synthesising:-

mul 2:

![image](https://github.com/user-attachments/assets/508219d8-d98e-4a04-9c85-2b970a3ce442)
![image](https://github.com/user-attachments/assets/045e78e8-298f-470b-88fa-50c1399cca61)
![image](https://github.com/user-attachments/assets/009844b9-7fda-48e4-b47f-92e576618f18)

mul8:

![image](https://github.com/user-attachments/assets/11cadd37-dae3-4ea0-abce-1552b156444e)
![image](https://github.com/user-attachments/assets/59ab46fb-62f8-4e14-b2a5-90faca780678)
![image](https://github.com/user-attachments/assets/a5472674-913f-4e63-a9cd-42c1f6172f01)

