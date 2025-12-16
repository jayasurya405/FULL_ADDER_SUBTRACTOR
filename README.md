<img width="1920" height="1080" alt="Screenshot 2025-12-16 192519" src="https://github.com/user-attachments/assets/f173802a-2f92-4826-9721-8226b08f48c4" /># FULL_ADDER_SUBTRACTOR

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
```Full Adder```
<img width="373" height="292" alt="Screenshot 2025-12-16 193515" src="https://github.com/user-attachments/assets/ed864fc9-af4c-4b92-b4d4-da1191a93cbe" />
```Full Subtractor```
<img width="187" height="315" alt="Screenshot 2025-12-16 193535" src="https://github.com/user-attachments/assets/d8de37cd-b2f9-4d51-b855-b6b7ed70aa62" />

**Procedure**
```
1.Open Quartus Prime and create a new project using the New Project Wizard.

2.Create a Verilog HDL file and write the code for Full Adder and Full Subtractor.

3.Save the file and set it as the Top-Level Entity.

4.Compile the design and verify that there are no compilation errors.

5.Create input combinations using VWF/ModelSim for simulation.

6.Verify the output with the truth table to confirm correct operation.
```



**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: RegisterNumber:25017693
```
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
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
```
**RTL Schematic**
<img width="1920" height="1080" alt="Screenshot 2025-12-16 192519" src="https://github.com/user-attachments/assets/ee3bb82c-de32-4388-b004-5bcf4ff72ab4" />

<img width="1920" height="1080" alt="Screenshot 2025-12-16 192753" src="https://github.com/user-attachments/assets/8c3496ad-c23e-4554-8540-643d7a144a30" />


**Output Timing Waveform**

<img width="1920" height="1080" alt="Screenshot 2025-12-16 192623" src="https://github.com/user-attachments/assets/0c8dad1c-2c6b-4d52-8f87-5cc40044868e" />

<img width="1920" height="1080" alt="Screenshot 2025-12-16 192849" src="https://github.com/user-attachments/assets/c291c1df-01ce-4ef5-b127-300993cf4d48" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



