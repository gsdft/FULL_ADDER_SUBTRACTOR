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

FULL ADDER

<img width="348" height="301" alt="image" src="https://github.com/user-attachments/assets/fe318bf8-12c3-4d66-afdb-ed54c4b4285c" />

FULL SUBRACTOR

<img width="346" height="235" alt="image" src="https://github.com/user-attachments/assets/7f5db924-d0ec-4df7-9f9a-e4254293602a" />

**Procedure**

 1. Type the program in Quartus software.
 2. Compile and run the program.
 3. Generate the RTL schematic and save the logic diagram.
 4. Create nodes for inputs and outputs to generate the timing diagram.
 5. For different input combinations generate the timing diagram.

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

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

FULL ADDER

<img width="588" height="307" alt="image" src="https://github.com/user-attachments/assets/dc4d9049-a9c3-4af8-b9a3-ec3223b33603" />

FULL SUBTRACTOR

<img width="582" height="311" alt="image" src="https://github.com/user-attachments/assets/615dd2c1-62f6-4b84-9cdc-731855e0a6b6" />

**Output Timing Waveform**

FULL ADDER

<img width="596" height="308" alt="image" src="https://github.com/user-attachments/assets/93366a61-015a-42aa-a98a-7d19b75919c1" />

FULL SUBRACTOR

<img width="595" height="312" alt="image" src="https://github.com/user-attachments/assets/7dd28faa-385f-466b-ac3a-b4128e474102" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



