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

 ![image](https://github.com/user-attachments/assets/f80c3c15-a87f-4db2-8fec-9ff17780055d)
 
 ![image](https://github.com/user-attachments/assets/2edd2303-7f09-43ce-811b-dd5a00007a45)



**Procedure**
# Full Adder:
1.Open Quartus II and create a new project.

2.Use schematic design entry to draw the full adder circuit.

3.The circuit consists of XOR, AND, and OR gates.

4.Compile the design, verify its functionality through simulation.

5.Implement the design on the target device and program it.
# Full Subractor:
1.Follow the same steps as for the full adder.

2.Draw the full subtractor circuit using schematic design.

3.The circuit includes XOR, AND, OR gates to perform subtraction.

4.Compile, simulate, implement, and program the design similarly to the full adder.


**Program:**
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by:YASHWANTH R

RegisterNumber: 212224240188
*/
```

```
module fulladd_top(a,b,c,sum,carry,BO,DIFF);
input a,b,c;
output sum,carry,BO,DIFF;
assign sum=a^b^c;
assign carry= a&b | a&c | b&c;
wire a0;
not (a0,a);
assign BO= b&c | a0&c | a0&b;
assign DIFF=a^b^c;
endmodule
```
**RTL Schematic**
![437082779-986caeea-b6bd-4bbd-922d-d63707d809b5](https://github.com/user-attachments/assets/5bf8549d-5cc2-4eed-b1a5-9d63800d276d)
![437081365-344f65bd-9c0a-46aa-9cb0-8cb062e6e853](https://github.com/user-attachments/assets/6a3a140f-0cd7-4147-9276-e5acfb47e07b)

**Output Timing Waveform**
![image](https://github.com/user-attachments/assets/98f5bc9b-f1cf-4f8d-ba66-8577b0b0e143)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



