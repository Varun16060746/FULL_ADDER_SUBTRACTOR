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
full adder
![exp4(add)](https://github.com/user-attachments/assets/ea1232de-034e-4e27-9e0d-78bb5b483e3a)
full subractor
![exp](https://github.com/user-attachments/assets/14a3eef5-3c50-431a-8c32-8145ea773de5)

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: VARUN A RegisterNumber:212224050057
*/
full adder
~~~
module exp4(A,B,C,sum,carry);
input A,B,C;
output sum,carry;
assign sum=A^B^C;
assign carry=((A&B)|(A&C)|(B&C));
endmodule
~~~
FULL SUBTRACTOR
~~~
module exp4a(A,B,C,dif,bor);
input A,B,C;
output dif,bor;
assign dif=A^B^C;
assign bor=(~A&C)|(~A&B)|(B&C);
endmodule
~~~

**RTL Schematic**
##full adder
<img width="1026" height="632" alt="image" src="https://github.com/user-attachments/assets/9b50d0a0-3ea3-4e41-a7a6-2d7a5e832a27" />

## full subtractor
<img width="628" height="431" alt="image" src="https://github.com/user-attachments/assets/bd77b68d-59d5-4885-85b9-13936b8362a2" />

**Output Timing Waveform**
full adder

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e827ce3c-e861-4940-80bb-78818968e159" />

full sub
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b924b448-95d3-4416-946d-2f6c7e3e3b05" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software hence the output was verified



