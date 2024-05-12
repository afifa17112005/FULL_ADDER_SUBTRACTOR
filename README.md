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

**Procedure**

Write the detailed procedure here

**Program:**
```
module fulladdsubb(a,b,cin,sum,carry,BO,DIFF);
input a,b,cin;
output sum,carry,BO,DIFF;
assign sum = (a ^ b ^ cin);
assign cout = (a & b) | (b & cin) | (a & cin);
//Write syntax for full adder sum and carry in date flow modelling 
assign DIFF = a ^ b ^ cin;
assign BO =  (~a & b) | (~(a ^ b) & cin);
//Write syntax for full subtractor Borrow and Difference in date flow modelling
endmodule
```

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: Afifa A
RegisterNumber:212223040008
*/

**RTL Schematic**
![Screenshot 2024-03-19 143153](https://github.com/afifa17112005/FULL_ADDER_SUBTRACTOR/assets/147080931/98b2683e-cb71-46ca-a96e-c1d4b77806e3)

**Output Timing Waveform**
![Screenshot 2024-03-19 143116](https://github.com/afifa17112005/FULL_ADDER_SUBTRACTOR/assets/147080931/8f0c4ac0-0e51-4d28-96c7-39ac6dd11e18)

**Result:**

program implemented Full-Adder-and-Full-Subtractor-circuits successfully executed



