# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.
 

## Logic Diagram (using nand gate) and (using nor gate):
![image](https://github.com/KrishnaPrasad148/Experiment--02-Implementation-of-combinational-logic-/assets/147332763/e258ccc1-8a45-43c9-a023-c554db9e1fba)

![image](https://github.com/KrishnaPrasad148/Experiment--02-Implementation-of-combinational-logic-/assets/147332763/24081881-7a6b-4e1e-9781-816cfb09da76)

## Procedure
*Create a project with required entities.

*Create a module along with respective file name.

*Run the respective programs for the given boolean equations.

*Run the module and get the respective RTL outputs.

*Create university program(VWF) for getting timing diagram.

*Give the respective inputs for timing diagram and obtain the results.

## Program:
```
Developed by: Krishna Prasad.S
RegisterNumber: 23013480
```
```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
module combinational(a,b,c,d,w,x,y,z,fl,f2);
input a,b,c,d,w,x,y,z;
output fl,f2;
wire g1=((~a)&(~b)&(~c)&(~d)); 
wire g2=((a)&(~c)&(~d));
wire g3=((~b)&(c)&(~d));
wire g4=((~a)&(b)&(c)&(d)); 
wire g5=((b)&(~c)&(d));
assign fl=g1|g2|g3|g4|g5; 
wire g6=((x)&(~y)&(z));
wire g7=((~x)&(~y)&(z));
wire g8=((~w)&(x)&(y)); 
wire g9=((w)&(~x)&(y));
wire g10=((w)&(x)&(y)); 
assign f2=g6|g7|g8|g9|g10;
endmodule
```
## RTL realization

## Output:
## RTL realization of NAND AND NOR gates:
![image](https://github.com/KrishnaPrasad148/Experiment--02-Implementation-of-combinational-logic-/assets/147332763/5f5340da-d900-41c0-aff0-7b0286ff465e)

## Truthtable of NAND gate:
![image](https://github.com/KrishnaPrasad148/Experiment--02-Implementation-of-combinational-logic-/assets/147332763/dc22d006-fd2b-4f8c-ac2f-ece12daf9e5c)

## Truthtable of NOR gate:
![image](https://github.com/KrishnaPrasad148/Experiment--02-Implementation-of-combinational-logic-/assets/147332763/e5cbbaee-da99-4dbb-a80c-5722007d45af)

## Timing Diagram:
![image](https://github.com/KrishnaPrasad148/Experiment--02-Implementation-of-combinational-logic-/assets/147332763/dcd35ec6-b734-44aa-b58b-b5ab99df3178)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
