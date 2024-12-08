# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

## **AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

## **Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

## **Full Adder and Full Subtractor**

## **Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

## **Figure -1 FULL ADDER**

## **Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin


## **Truthtable**
### ![fa (2)](https://github.com/user-attachments/assets/14e38e27-ec41-4169-9860-6fe858de058b)
### ![fs (2)](https://github.com/user-attachments/assets/a01963c3-8ea8-493e-a9be-32bbc06c8d3b)

## **Procedure**

Write the detailed procedure here
1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.
## **Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
*/
### Full Adder:
### module fa(a,b,c,sum,carry);
### input a,b,c;
### output sum,carry;
### wire w1,w2,w3;
### assign sum=a^b^c;
### assign w1=a&b;
### assign w2=b&c;
### assign w3=c&a;
### assign carry=w1|w2|w3;
### endmodule
### Full subtractor:
### module fs(df,bo,a,b,bin);
### input a,b,bin;
### output df,bo;
### wire w1,w2,w3;
### assign w1=a^b;
### assign w2=(~a&b);
### assign w3=(~w1&bin);
### assign df=w1^bin;
### assign bo=w2|w3;
### endmodule
### Developed by: Sri mathi S
### Register number: 24004689 
## **RTL Schematic**
### ![full adder](https://github.com/user-attachments/assets/b135ad44-8364-4928-8ccc-7a993b75a834)
### ![full subtractor](https://github.com/user-attachments/assets/d0c79ddb-6daa-4d84-bbfa-de5c88aab468)


## **Output Timing Waveform**
### ![fa](https://github.com/user-attachments/assets/e4db0b8e-1b4c-4c5a-b0ca-ab08e0b23657)
### ![fs](https://github.com/user-attachments/assets/22683dc5-e95b-4ee6-a767-ae86960a5a12)

## **Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



