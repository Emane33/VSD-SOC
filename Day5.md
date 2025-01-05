# DFT techniques:

- verification: verify the functionality of design.
  
- testability: if a design is well-controlable and well-observable.
  
- DFT: technique which facilitates a design and to become testable after production.
  
- some issues can be found in fabrication like high temperature.

- Types of DFT:
  
 *for macros, we use MBist( memory block), where in the memory the test run to check if chip working or not.
  
*for flops, we use scan chains.
  
*for combintational, we generate test patterns.

- levels of testing after chip fabricated:
  
*chip level, when chip is manufactured.
  
*board level, when chips are integrated on the boards/package.
  
*system level, when several boards are assembled together ex.computer.

- we need it at the beginign of design flow during synthesis.
  
- what is controability?
  
from DFT point of view, we intend if both 0 and 1 are able to propogate te each node within the target pattern.

- what is observability?

the ability to meausure the state of a logic signal. when we say node is observed, we mean the value at the node can be shifted out throw the scan pattern and can be observed through the
scan ports.
