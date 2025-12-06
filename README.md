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
FULL ADDER:

![sum](https://github.com/user-attachments/assets/99671ba2-35b3-4419-95ad-b590efc7ac68)

FULL SUBTRACTER:

![difference](https://github.com/user-attachments/assets/32884fb3-87dc-4cd2-8c32-48eb2f7e8fa8)


**Procedure**

Full Adder:

i  . Open Quartus II and create a new project.

ii . Use schematic design to draw the full adder circuit. 

iii. The circuit consists of XOR, AND, and OR gates.

iv . Compile the design, verify its functionality using simulation.

v  . Implement the design on the target device and program it.

**Full Subtractor:** 

i  . Follow the same steps as for the full adder. 

ii . Draw the full subtractor circuit using schematic design. 

iii. The circuit includes XOR, AND, OR gates to perform subtraction. 

iv . And as usual Compile, simulate, implement, and program the design.

**Program:**
```
module Full_AS(
 input A, B, Bin, Cin,
    output Sum, Carry, Diff, Borrow
);
    
assign Sum    = A ^ B ^ Cin;
assign Carry  = (A & B) | (B & Cin) | (Cin & A);
assign Diff   = A ^ B ^ Bin;
assign Borrow = (~A & B) | (Bin & ~(A ^ B));

endmodule
```
Developed by: S.Visaniya
RegisterNumber: 25017540


**RTL Schematic**

<img width="833" height="536" alt="Screenshot 2025-12-05 115159" src="https://github.com/user-attachments/assets/b9b702b6-c02c-4ab9-b3d7-d81af79701c0" />


**Output Timing Waveform**

<img width="1920" height="1080" alt="Screenshot (50)" src="https://github.com/user-attachments/assets/a931a9ca-fe98-4e8e-9d43-4f675ecb1187" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



