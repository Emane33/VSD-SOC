#  Library Cell design using Magic and Characterization using Ngspice

- clone the following: https://github.com/nickson-jose/vsdstdcelldesign.git

 - design steps:

![image](https://github.com/user-attachments/assets/1c8419a6-5cb8-4c5d-b789-49a6c3353246)

![image](https://github.com/user-attachments/assets/082b1114-c160-4568-855e-5c3531f2f042)

- to know what is this element, hover over it and press s:

  ![image](https://github.com/user-attachments/assets/94678967-4089-4fa4-bf49-8c0652813ca3)

![image](https://github.com/user-attachments/assets/64f7cdf9-e998-442c-b3de-6e943cd3f2d2)

- extract spice:

  ![image](https://github.com/user-attachments/assets/ab3471a7-1468-4340-8253-5c113c467f45)

- using vim sky130_inv.spice we open it:

  ![image](https://github.com/user-attachments/assets/ad5b7e8e-33f1-4fa1-966c-c37073ee31d0)

- after edititing:

![image](https://github.com/user-attachments/assets/c72a5794-cb85-4d11-85ac-a4f2400c8430)

![image](https://github.com/user-attachments/assets/7a224dc8-14ee-48e4-8d67-7021763f35a0)

- after simulation:

![image](https://github.com/user-attachments/assets/0dd3ba0b-3acd-43aa-891b-7e3d2fd851cf)

![image](https://github.com/user-attachments/assets/be829c49-626e-4812-aed0-a44525e87d61)

- plot y vs time a:

![image](https://github.com/user-attachments/assets/6a55dac0-8b3f-4341-b316-0eb6f708de8d)

t_rise: represent the rising time which from 20% to 80%, so 20%= 2.148
t_fall: represent the falling time from 80% to 20%, so 80%= 1.329
t_pLH: cell rise delay represent diffrence in time between 50% output rise to 50% input fall, which equals = 3.114
t_pHL: cell fall delay represen the diffrence in time between 50% output fall to 50% input rise, which equals = 8.693
# find problem in DRC:

- if you want to know about magic:

  http://opencircuitdesign.com

  - what is technology file?

  it is a file that tells magic everything need to know about process and rules of it.

  - waht is CIFoutput?
 
     cifoutput section of the technology file describes how to generate mask layers from Magic's abstract layers.

- why do we need it?

  The layers stored by Magic do not always correspond to physical mask layers. For example, there is no physical layer corresponding to (the scmos technology file layer) ntransistor; instead, the actual circuit must be built up by overlapping poly and diffusion over pwell. When writing CIF (Caltech Intermediate Form) or Calma GDS-II files, Magic generates the actual geometries that will appear on the masks used to fabricate the circuit.

 - downloading the zip file and extract it:

![image](https://github.com/user-attachments/assets/bf43f577-2749-4cad-b827-b0aa101ce298)

 - content of it:

![image](https://github.com/user-attachments/assets/b5dd6bad-908c-48df-84a6-04bb30707ed4)

- to view magicrc file( the starter description of magic):

  ![image](https://github.com/user-attachments/assets/03614882-22a5-47a7-9c85-475144b2bcb4)

- content of it:

  ![image](https://github.com/user-attachments/assets/9254d74a-2af4-4c24-82cc-8996e32c3f77)

![image](https://github.com/user-attachments/assets/92c0de54-4e71-4888-90b9-0ff4c9837f22)

- open in magic but with better graphics:

![image](https://github.com/user-attachments/assets/b753d1b2-c5e7-48cb-8a70-b6d0e92b66b4)

![image](https://github.com/user-attachments/assets/092859ca-2a96-4549-9ab6-aab5aedc531a)

- open from file manually:

![image](https://github.com/user-attachments/assets/eb35ba74-ff36-45d1-aea2-b01f283b5e8d)

![image](https://github.com/user-attachments/assets/665c7538-8309-4fa8-9fca-4280a32a3f7d)

- you can get details from here:

  ![image](https://github.com/user-attachments/assets/be4a46f9-7686-42ee-a927-19ae34740919)

- CU doesn't exist in skywater thats why they are not implemented

  
