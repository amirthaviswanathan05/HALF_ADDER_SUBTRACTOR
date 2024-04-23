# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

#AIM:

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

#Equipments Required:

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

#Half Adder

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

#Half Subtractor

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

#Procedure:

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.

# Program:

## Half-adder:
```
module half_adder(a,b,sum,carry);
input a,b;
output sum,carry; 
assign sum = a^b;
assign carry = a & b;
endmodule
```
## Half-subtractor:
```
module halfsub_top(a,b,D,Bo);
input a,b;
output D,Bo; // Outputs sum and carry for half adder:Outputs difference D,Borrow Bo for half subtractor
assign D = a ^ b;
  assign Bo = ~a & b;
endmodule
```

```
Developed by : Amirthavarshini V
Registration numbr : 212223040014
```

# Truth Table :
## Half-adder:
![318335599-60a9abae-d18e-4818-b5ef-8952db99af48](https://github.com/amirthaviswanathan05/HALF_ADDER_SUBTRACTOR/assets/149035397/57224de0-4a0d-4492-9672-752740568d6c)
##Half-subtractor:
![318335651-1ea5f214-b822-49fe-ad71-ccd4cd0d05b6](https://github.com/amirthaviswanathan05/HALF_ADDER_SUBTRACTOR/assets/149035397/3742744e-eec4-4804-9e4f-30b884707449)



# RTL Schematic:
![318334898-f6224e20-50a1-409a-8bc1-f2ef269ba441](https://github.com/amirthaviswanathan05/HALF_ADDER_SUBTRACTOR/assets/149035397/d33b4ced-8965-4f80-ac45-96f1355f1d7f)

# Output/TIMING Waveform:
![318334951-8dc652fc-3540-4585-94ba-69fa4c2b946f](https://github.com/amirthaviswanathan05/HALF_ADDER_SUBTRACTOR/assets/149035397/2a4f9085-033e-4ca0-b3e5-71385b9ffc0c)
![318334978-c9d7d3a6-97d9-4b6e-b49d-92cf274e6677](https://github.com/amirthaviswanathan05/HALF_ADDER_SUBTRACTOR/assets/149035397/fcf87b7e-be84-40b1-bb21-9f4c9692aebd)

# Result:
Hence the output was verified successfully.
