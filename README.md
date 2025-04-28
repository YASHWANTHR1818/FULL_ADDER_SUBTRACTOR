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
**Program:**
module full(A,B,Cin,Bin,Sum,Carry,Diff,Borrow);
input A,B,Cin,Bin;
output Sum,Carry,Diff,Borrow;
assign Sum=A^(B^Cin);
assign Carry=(A&B)|(A&Cin)|(B&Cin);
assign Diff=A^(B^Bin);
assign Borrow=(~A&Bin)|(~A&B)|(B&Bin);
endmodule

module fs(a,b,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )));
endmodule

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
 Developed by:YASHWANTH R
 RegisterNumber:212224240188

**RTL Schematic**
![437082779-986caeea-b6bd-4bbd-922d-d63707d809b5](https://github.com/user-attachments/assets/5bf8549d-5cc2-4eed-b1a5-9d63800d276d)
![437081365-344f65bd-9c0a-46aa-9cb0-8cb062e6e853](https://github.com/user-attachments/assets/6a3a140f-0cd7-4147-9276-e5acfb47e07b)

**Output Timing Waveform**
![437081624-3ff3d96e-685f-4eee-8017-d45bfd07a1a8](https://github.com/user-attachments/assets/6bfe5107-c00c-4449-a48a-9c41561d0e8c)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



