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

/* Program to design a full subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

**FULL ADDER**
```
module EXPERIMENT4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
wire sl,cl,c2;
xor(sl,a,b);
and(cl,a,b);
xor(sum,sl,cin);
and (c2,sl,cin);
or(cout,c2,cl);
endmodule
```

**FULL SUBTRACTER**
```
module EXPERIMENT4B(df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2, w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule
```
Developed by: SUDHARSANAN U
RegisterNumber: 24900788
*/

**RTL Schematic**

**FULL ADDER**

![Screenshot 2024-11-26 101852](https://github.com/user-attachments/assets/d22632d6-a1e6-4628-85dd-1032a2da3ef3)

**FULL SUBTRACTER**

![Screenshot 2024-11-26 103017](https://github.com/user-attachments/assets/e4dc40be-5868-4fec-bd1e-17c6728e673f)

**Output Timing Waveform**

**FULL ADDER**

![Screenshot 2024-11-26 102132](https://github.com/user-attachments/assets/40c9f6a1-5073-42f6-bd4b-b38576d35bad)

**FULL SUBTRACTER**

![Screenshot 2024-11-26 103219](https://github.com/user-attachments/assets/f5f83243-e76c-4404-b99a-c39f4d163d42)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



