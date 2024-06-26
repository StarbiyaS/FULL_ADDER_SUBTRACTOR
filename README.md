# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**
 
Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
**Full adder**

![image](https://github.com/StarbiyaS/FULL_ADDER_SUBTRACTOR/assets/144870533/6fe24a79-f843-4b9d-ac52-47de7d365f33)

**Full subtractor**

![image](https://github.com/StarbiyaS/FULL_ADDER_SUBTRACTOR/assets/144870533/6cf3aadf-31fe-47fb-96bc-422a73325db5)


**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: STARBIYA S RegisterNumber:212223040208
**full adder**
```
 module exp4(a,b,c,sum,carry);
 input a,b,c;
 output sum,carry;
 xor(sum,a,b,c);
 assign carry=a&b | b&c | a&c;
 endmodule
```
**full subtractor**
```
 module exp4(diff,carry,a,b,c);
 input a,b,c;
 output diff,carry;
 xor(diff,a,b,c);
 assign carry= (~a)&c | (~a)&b | (b&c);
 endmodule
```
**RTL Schematic Full adder:**

![image](https://github.com/StarbiyaS/FULL_ADDER_SUBTRACTOR/assets/144870533/2e4a632c-c76c-4e23-ae63-37b0ae3e9a38)


**Full subtractor**


![image](https://github.com/StarbiyaS/FULL_ADDER_SUBTRACTOR/assets/144870533/86002a58-aac4-412f-aa16-de8a50a13635)


## Output Timing Waveform

**Full adder**


![image](https://github.com/StarbiyaS/FULL_ADDER_SUBTRACTOR/assets/144870533/6f12528c-2a73-4189-8555-6aa763bff6eb)


**Full subtractor**


![image](https://github.com/StarbiyaS/FULL_ADDER_SUBTRACTOR/assets/144870533/b6504851-c494-4911-8c27-3b13b1d0798b)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



