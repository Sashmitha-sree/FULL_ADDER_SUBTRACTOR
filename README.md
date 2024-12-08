# Name:Sashmitha Sree
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
![Screenshot 2024-12-08 212319](https://github.com/user-attachments/assets/283fecbf-d0bc-4190-9e43-26d110b17662)

![Screenshot 2024-12-08 212253](https://github.com/user-attachments/assets/b6568b17-4da3-452e-8d37-bc4aed34a8ba)


**Procedure**
1.Type the program in Quartus software .

2.Compile and run the program .

3.Generate the RTL schematic and save the logic diagram.

4.create nodes for inputs and outputs to generate the timing diagram .

5.for different input combinations generate the timing diagram.

**Program:**

```
*Full adder*
 module de4(a,b,c,sum,carry);
 input a,b,c;
 output sum,carry;
 xor(sum,a,b,c);
 assign carry=a&b | b&c | a&c;
 endmodule

*Full subractor*
module de42(diff,carry,a,b,c);
input a,b,c;
output diff,carry;
xor(diff,a,b,c);
assign carry= (~a)&c | (~a)&b | (b&c);
endmodule
```
**RTL Schematic**
![add](https://github.com/user-attachments/assets/0f23a90c-cfe8-455a-828d-2b1728477d84)

![sub](https://github.com/user-attachments/assets/6b9bcd6e-c441-4fb1-8b40-4e68c7dea6fa)


**Output Timing Waveform**
![addd](https://github.com/user-attachments/assets/b063ef22-641c-4c64-aee5-9b0d0320bf99)
![suubb](https://github.com/user-attachments/assets/9c5b5380-b2ed-43ee-b53c-c9c7c2597029)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



