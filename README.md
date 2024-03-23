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
Developed by:Swetha D
Register no:212223040222
module exp4(a,b,c,sum,carry,BO,DIFF);
input a,b,c;
output sum,carry,BO,DIFF;
assign sum=a^b^c;
assign carry=(a&b)|(b&c)|(c&a);  //Write syntax for full adder sum and carry in date flow modelling 
wire a0;
not (a0,a);
assign DIFF=a^b^c;
assign BO=(a0&b)|(b&c)|(a0&c);  //Write syntax for full subtractor Borrow and Difference in date flow modelling
endmodule
```

**RTL Schematic**

**Output Timing Waveform**

**Result:**
![Screenshot (8)](https://github.com/swetha23013979/FULL_ADDER_SUBTRACTOR/assets/153823422/aeda132e-2bc0-4a7a-97c6-5b6ae645709f)


![Screenshot (7)](https://github.com/swetha23013979/FULL_ADDER_SUBTRACTOR/assets/153823422/462cfef7-ae8d-4063-8df6-38757ee0def9)

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



