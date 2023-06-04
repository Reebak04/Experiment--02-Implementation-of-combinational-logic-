# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:

To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
 Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

## Logic Diagram
Using NOR gates NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Procedure
The input and output variables are allocated with letter symbols. The exact truth table that defines the required relationships between inputs and outputs is derived. The simplified Boolean function is obtained from each output. The logic diagram is drawn.

## Program:
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: Tejusve Kabeer.F
RegisterNumber: 212222100054

### F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
```python
module f1(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire p,q,r,s,t;
assign p = (~A & ~B & ~C & ~D);
assign q = (A & ~C & ~D);
assign r = (~B & C & ~D);
assign s = (~A & B & C & D);
assign t = (B & ~C & D);
assign F1 = p | q | r | s | t;
endmodule
```
### F2=xy’z+x’y’z+w’xy+wx’y+wxy
```
module imp(w,x,y,z,F2);
input w,x,y,z;
output F2;
wire p,q,r,s,t;
assign p= (x & ~y & z);
assign q= (~x & ~y & z);
assign r= (~w & x & y);
assign s= (w & ~x & y);
assign t= (w & x & y);
assign F2= p | q | r | s | t;
endmodule
```
*/

## Output:

## RTL

### F1
![image](https://github.com/Reebak04/Experiment--02-Implementation-of-combinational-logic-/assets/118364993/078a8fab-54a8-47a7-836d-a7ed5cf49517)
### F2
![image](https://github.com/Reebak04/Experiment--02-Implementation-of-combinational-logic-/assets/118364993/286a2688-8d48-4594-9460-05c28d665eac)
## Timing Diagram

### F1
![image](https://github.com/Reebak04/Experiment--02-Implementation-of-combinational-logic-/assets/118364993/804e2710-e610-4bd2-b14e-8b208082f604)
### F2
![image](https://github.com/Reebak04/Experiment--02-Implementation-of-combinational-logic-/assets/118364993/f47bcd88-719f-4785-9f29-681bb9757ca5)
## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
