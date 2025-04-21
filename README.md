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







![Screenshot 2025-04-10 104412](https://github.com/user-attachments/assets/bae95ad2-fa63-4f52-9488-105e4d644c2f)








![Screenshot 2025-04-10 104456](https://github.com/user-attachments/assets/cf636639-e143-4be7-8f4b-f0dca6b22638)









**Procedure**

Write the detailed procedure here
1. Write the code in Quartus software by creating a new project wizard.
2. Run the program to get output.
3. Then open RTL viewer and download that image.
4. Open new file with University program VWF
5. Set end timer and execute, then download the waveform.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:somalaraju rohini RegisterNumber:212224240156
*/
expt4a-full adder
```
module exp_4a(sum, cout, a, b, cin);
    output sum;
    output cout;
    input a;
    input b;
    input cin;

	 wire w1,w2,w3;
	 assign w1=a^b;
	 assign w2=a&b;
	 assign w3=w1&cin;
	 assign sum=w1^cin;
	 assign cout=w2|w3;
endmodule
```
exp-4b-full subtractor
```
module exp_4b(df, bo, a, b, bin);
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
**RTL Schematic**


![Screenshot 2025-04-09 151949](https://github.com/user-attachments/assets/7c4cc2ae-ae23-4328-b633-620f337667b5)








![Screenshot 2025-04-09 153805](https://github.com/user-attachments/assets/09300570-5653-4d74-a811-d908173e2cee)







**Output Timing Waveform**







![Screenshot 2025-04-09 153352](https://github.com/user-attachments/assets/f2fc268a-29d9-4715-af78-0325951b951e)






![Screenshot 2025-04-09 154527](https://github.com/user-attachments/assets/7563377c-3581-4935-a6b8-b3af6c73b2ee)






**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




