# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

HALF SUBTRACTOR:
module HalfSub(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference=(a^b);
assign borrow=(~a&b);
endmodule


FULL SUBTRACTOR:
module FullSub(a,b,c,difference,borrow);
input a,b,c;
output difference,borrow;
assign borrow=(~a&(b^c)|(b&c));
assign diggerence=(a^b^c);
endmodule

Developed by: Deepika.K
RegisterNumber: 212222050009 
*/
LOGIC GATES
![logic gate Ex4](https://user-images.githubusercontent.com/128984662/232322397-fc569004-c38a-4155-865a-4ed44c21eaee.jpeg)

## Output:
## Truthtable
HALF SUBTRACTOR
![Ex4 HS truthtable](https://user-images.githubusercontent.com/128984662/232322602-022d4a97-7b7e-4e73-b154-45cc39e55ff3.jpeg)
FULL SUBTRACTOR
![Ex4 FS truthtable](https://user-images.githubusercontent.com/128984662/232322876-b878f147-55ec-4c50-826e-3ec3a8f5cdb9.jpeg)

##  RTL realization
HALF SUBTRACTOR
![ex4 HS rtl](https://user-images.githubusercontent.com/128984662/232323079-fff37973-c2ec-4585-9f73-0d2b870e29cc.jpeg)
FULL SUBTRACTOR
![Ex4 FS rtl](https://user-images.githubusercontent.com/128984662/232323142-3eaef6c7-0ccf-47eb-ae19-fd1ffa3e4088.jpeg)

## Timing diagram 
HALF SUBTRACTOR
![ex4 HS timing diagram](https://user-images.githubusercontent.com/128984662/232323196-ffd0eb29-7041-4c1f-ac07-91b33f777a99.jpeg)
FULL SUBTRACTOR
![ex4 FS timing diagram](https://user-images.githubusercontent.com/128984662/232323244-ca5ebbac-3753-4c67-84a3-c53012a85d97.jpeg)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
