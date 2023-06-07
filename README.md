# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory:
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

## Logic Diagram:
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. ###Using NAND gates NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted. F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

Using OR gates NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms. F2=xy’z+x’y’z+w’xy+wx’y+wxy
## Procedure:
Step 1:

Create a project with required entities.

Step 2:

Create a module along with respective file name.

Step 3:

Run the respective programs for the given equations.

Step 4:

Run the module and get the respective RTL outputs.

Step 5:

Create university program(VWF) for getting timing diagram.

Step 6:

Give the respective inputs for timing diagram and obtain the results.
## Program:
```
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: ATHMAJ VENUGOPAL
RegisterNumber:212222240014  
*/
```
```
F1:

module ff(a,b,c,d,f1);
input a,b,c,d;
output f1;
assign f1 = (~b&~d) | (~a&b&d) | (a&b&~c);
endmodule

F2:

module de (w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2 = (x&y)|(w&y)|(~y&z);
endmodule 
```
## RTL realization:
### F1
![image](https://github.com/ATHMAJ03/Experiment--02-Implementation-of-combinational-logic-/assets/118753139/b8b805f9-5fa3-4e7d-b205-84dbd7c6c1a6)
### F2
![image](https://github.com/ATHMAJ03/Experiment--02-Implementation-of-combinational-logic-/assets/118753139/a8a580dc-8bd0-4016-b766-6113b04797c4)

## Output:
## Timing Diagram:
### F1
![image](https://github.com/ATHMAJ03/Experiment--02-Implementation-of-combinational-logic-/assets/118753139/cc95558a-392e-41fe-898e-340f3b5bc7a5)
### F2
![image](https://github.com/ATHMAJ03/Experiment--02-Implementation-of-combinational-logic-/assets/118753139/fe767a7b-fc2e-4f7a-88dc-4c47626322b3)
## Truth Table:
![image](https://github.com/ATHMAJ03/Experiment--02-Implementation-of-combinational-logic-/assets/118753139/c59ea9e9-5042-4b16-bddb-908dbb31fc15)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
