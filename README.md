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
.

![Screenshot 2024-12-05 194245](https://github.com/user-attachments/assets/f8aecc00-0d36-40d2-82e9-4dbfaad40e7f)

![Screenshot 2024-12-05 194337](https://github.com/user-attachments/assets/f327b577-b9b0-4502-8ebe-8542d064f1a2)
**Procedure**

Write the detailed procedure here

Full Adder: Inputs: Three inputs: A, B (the two bits to be added), and Cin (the carry-in bit from a
previous addition). Outputs: Two outputs: Sum (the resulting sum) and Cout (the carry-out bit).
Logic: Sum = A ^ B ^ Cin (XOR operation). Cout = (A & B) | (A & Cin) | (B & Cin) (carry occurs if at
least two inputs are 1).
Full Subtractor: Inputs: Three inputs: A, B (the two bits, where A - B is calculated), and Bin (the
borrow-in from a previous subtraction). Outputs: Two outputs: Diff (the resulting difference) and
Bout (the borrow out bit). Logic: Diff = A ^ B ^ Bin (XOR operation). Bout = (~A & B) | ((~A | B) &
Bin) (borrow occurs if A is less than B or needs a borrow). Both circuits follow simple XOR logic for
the primary result and AND-OR logic to determine carry or borrow condition

**Program:**
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Vishnu Rathan B
RegisterNumber: 24001855
```
```
module fulladdsub(a,b,cin,bin,sum,carry,difference,borrow);
input a,b,cin,bin; output sum,carry,difference,borrow;
assign sum=a^b^cin;
assign carry=(a^b)&cin|a&b;
assign difference=a^b^bin;
assign borrow=~(a^b)&bin|(~a)&b;
```
**RTL Schematic**

![Screenshot 2024-12-05 194602](https://github.com/user-attachments/assets/9a53d4ee-c70d-41f4-92a4-068f7e132058)

**Output Timing Waveform**

![Screenshot 2024-12-05 194627](https://github.com/user-attachments/assets/424ca0d2-6a3d-42b3-8048-54ffdb44e11e)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



