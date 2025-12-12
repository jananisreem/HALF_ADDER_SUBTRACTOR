# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
 module EXP3(
    input  wire a, b,    
    output wire sum,      
    output wire carry     
);

    assign sum   = a ^ b;  
    assign carry = a & b;   

endmodule

module EXP4(
    input  wire a, b, cin,  
    output wire sum, carry   
);

    // Logic equations
    assign sum   = a ^ b ^ cin;                  
    assign carry = (a & b) | (b & cin) | (a & cin); 

endmodule
 
Developed by:JANANI SREE M
RegisterNumber:25015867

**RTL Schematic**
<img width="942" height="608" alt="Screenshot 2025-12-12 191834" src="https://github.com/user-attachments/assets/27894813-7639-43e5-b281-07cfd5f8dc36" />
<img width="997" height="590" alt="Screenshot 2025-12-12 191816" src="https://github.com/user-attachments/assets/c79e96f1-1b8c-4cc6-b8b7-390520810127" />

**Output/TIMING Waveform**
<img width="1313" height="843" alt="Screenshot 2025-12-12 191857" src="https://github.com/user-attachments/assets/d67b03f7-5660-4c5a-87ff-b1cce207d914" />
<img width="1324" height="860" alt="Screenshot 2025-12-12 191919" src="https://github.com/user-attachments/assets/1cc47ce0-c466-443e-86a1-c1285dc8e957" />

**Result:**
Thus, the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
