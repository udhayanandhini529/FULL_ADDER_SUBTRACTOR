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

<img width="456" height="388" alt="image" src="https://github.com/user-attachments/assets/9973fd22-f83f-46e5-b97b-132c8637cf65" />

FULL SUBTRACTOR

<img width="463" height="324" alt="image" src="https://github.com/user-attachments/assets/abad6f49-55d7-42b9-9de4-5b71a302f69c" />


**Procedure**

Write the detailed procedure here
1.Type the program in Quartus software.
2.Compile and run the program.
3.Generate the RTL schematic and save the logic diagram.
4.Create nodes for inputs and outputs to generate the timing diagram.
5.For different input combinations generate the timing diagram.


**Program:**

/* Program to design a full subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:25007306
*/i)FULL ADDER

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
assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));
endmodule

**RTL Schematic**
FULL ADDER

<img width="781" height="388" alt="image" src="https://github.com/user-attachments/assets/5ea11c3d-1fe6-4477-af36-97b4f401af7b" />

FULL SUBTRACTOR

<img width="776" height="404" alt="image" src="https://github.com/user-attachments/assets/6f436e43-0d30-4c54-b083-d0194821e71b" />


**Output Timing Waveform**
FULL ADDER

<img width="783" height="396" alt="image" src="https://github.com/user-attachments/assets/64538c30-9fe6-4750-94ec-969157db3cfa" />

FULL SUBTRACTOR

<img width="774" height="403" alt="image" src="https://github.com/user-attachments/assets/a51d0ab7-5b5a-4d21-a5bd-183ec19d5a73" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



