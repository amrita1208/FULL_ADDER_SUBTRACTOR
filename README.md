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

<img width="525" height="444" alt="{BC8722C2-07EA-4CFE-B04A-01A145383A55}" src="https://github.com/user-attachments/assets/11a0a796-c8fd-4077-b00b-732fca004467" />

full subtractor

<img width="503" height="336" alt="{161A784C-4C43-4D06-B17F-75BEECCD7A3F}" src="https://github.com/user-attachments/assets/041eeccb-76c0-4b5f-b402-e4a10b9ad27f" />

**Procedure**

1.Type the program in Quartus software
.
2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram


**Program:**

Program to design a full adder and full subtractor circuit and verify its truth table inquartus using Verilog programming.

i)FULL ADDER

module fa(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule

ii)FULL SUBTRACTOR

module fs(a,b,bin,difference,borrow);

input a,b,bin;

output difference,borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));

endmodule

**RTL Schematic**

full adder

<img width="760" height="288" alt="{48455A5F-1F79-417D-A956-1F65316E24A4}" src="https://github.com/user-attachments/assets/95cfeef7-748d-4950-9f12-8b14625c4e66" />

full subtractor

<img width="639" height="355" alt="{12D419D1-7B2D-400F-990D-58344C9DE53F}" src="https://github.com/user-attachments/assets/914f42ad-d8ae-4c34-94b3-f33310a0a635" />

**Output Timing Waveform**

full adder

<img width="1164" height="473" alt="{B4CB4D1A-A7B3-443F-92D6-3E461B2C530A}" src="https://github.com/user-attachments/assets/108e2b34-7cf6-47cd-a056-18e284b55824" />

full subtractor

<img width="1263" height="567" alt="{94694D2D-70CF-4575-BE01-4DF757202533}" src="https://github.com/user-attachments/assets/f677b276-b4c9-43f9-a1a3-55a8a056171d" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



