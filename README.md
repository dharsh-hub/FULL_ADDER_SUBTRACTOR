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

**truthtable**

full adder:

![image](https://github.com/user-attachments/assets/ec9a1f37-4b00-4b38-abd6-cf80a5de9bd2)

full subtracter:

![image](https://github.com/user-attachments/assets/9a9fd269-4410-48bb-bd43-e8a113be3f8d)



**Procedure**

Write the detailed procedure here

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.

**Program:**
```
module exp4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
wire s1,c1,c2;
xor(s1,a,b);
and(c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);
endmodule


module exp4a(df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: DHARSHINI S RegisterNumber: 24900238
*/

**RTL Schematic**

full adder:

![Screenshot 2024-11-19 211403](https://github.com/user-attachments/assets/ba6c7ee7-e10a-46b0-bddb-030c5fa0937b)

full subtracter:

![Screenshot 2024-11-19 213105](https://github.com/user-attachments/assets/ae34977d-88c5-4437-add2-416709401141)



**Output Timing Waveform**

full adder:

![Screenshot 2024-11-19 211951](https://github.com/user-attachments/assets/2bce6650-0c14-4c56-aaa3-d854ba749d04)

full subtracter:

![Screenshot 2024-11-19 213402](https://github.com/user-attachments/assets/5f1e996e-30d8-43a2-b68f-30b7a2689d9d)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



