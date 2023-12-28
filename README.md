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
1.Connect the supply (+5V) to the circuit.
2.Switch ON the main switch.
3.If the output is 1, then the led glows.

## Program:
/*
Half subtractor:

module ex4(a,b,diff,borr);
input a,b;
output diff,borr;
assign diff=(a^b);
assign borr=((~a)&b);
endmodule 

Full subtractor:

module ex41(a,b,bin,diff,borr);
input a,b,bin;
output diff,borr;
assign diff=a^b^bin;
assign borr=((~a)&b)|(b&bin)|((~a)&bin);
endmodule 

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: SHANMUGAKARTHIK G
RegisterNumber: 212223220105 
*/

## Output:

## Truthtable
Half Subtractor:
![image](https://github.com/Shanmugakarthik05/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149762972/9bd41eed-2a1d-499b-806b-f21a400f5eb3)

Full Subtractor:
![image](https://github.com/Shanmugakarthik05/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149762972/c35c1d1c-5f1a-4209-a955-0d27f076104a)


##  RTL realization
Half Subtractor:
![image](https://github.com/Shanmugakarthik05/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149762972/5d1b9787-a070-4648-a722-2e122f8e459f)

Full Subtractor:
![image](https://github.com/Shanmugakarthik05/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149762972/d1e19052-db7c-4f42-818b-09d02fe3a872)


## Timing diagram 
Half Subtractor:
![image](https://github.com/Shanmugakarthik05/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149762972/a45187d5-602a-45d0-81e7-a73b6c3111de)

Full Subtractor:
![image](https://github.com/Shanmugakarthik05/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149762972/b6c943d1-4eb5-4d9d-bb4b-87b3d8d67775)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
