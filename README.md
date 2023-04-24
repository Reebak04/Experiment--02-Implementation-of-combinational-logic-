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
 

## Logic Diagram
## Procedure
## Program:
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: Tejusve Kabeer.F
RegisterNumber: 212222100054
```python
module cpmbine(a,b,c,d,f);
input a,b,c,d;
output f;
wire p,q,r;
assign p=(~c & b & a);
assign q=(~d & c & c & a);
assign r=(c & ~b & a);
assign f=(~(~p & ~q & ~r));
endmodule

module combine1(a,b,c,d,f);
input a,b,c,d;
output f;
wire p,q,r;
assign p=(c & ~b & a);
assign q=(d & ~c & a);
assign r=(c & ~b & a);
assign f=((p | q & |r));
endmodule
```
*/

## Output:

## RTL

###F1
![Screenshot (50)](https://user-images.githubusercontent.com/118364993/233889662-994e5857-2994-48a0-b619-1e10365249bd.png)

###F2
![Screenshot (51)](https://user-images.githubusercontent.com/118364993/233889715-d1897588-8644-4388-bccd-d841da215321.png)

## Timing Diagram

###F1
![Screenshot (52)](https://user-images.githubusercontent.com/118364993/233889967-48ef4e70-1ed0-4875-9d16-7f3be0444b47.png)

###F2
![Screenshot (53)](https://user-images.githubusercontent.com/118364993/233890139-551bcd5e-0899-4d8e-a155-b0f3ac664154.png)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
