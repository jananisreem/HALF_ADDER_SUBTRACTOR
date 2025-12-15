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
HALF ADDER
module half_adder (
    input wire a, b,      // Inputs
    output wire sum,       // Sum output
    output wire carry      // Carry output
);

    // Logic equations
    assign sum   = a ^ b;  // XOR for sum
    assign carry = a & b;  // AND for carry

endmodule
HALF SUBTRACTER 
module half_subtractor (
    input  wire a, b,        // Inputs
    output wire diff, borrow  // Outputs
);

    // Logic equations
    assign diff   = a ^ b;    // XOR for difference
    assign borrow = ~a & b;   // Borrow when a < b

endmodule

Developed by:JANANI SREE M
RegisterNumber:25015867

**RTL Schematic**
<img width="1239" height="819" alt="Screenshot 2025-12-15 171517" src="https://github.com/user-attachments/assets/a7ac0553-4180-41e3-a33c-bfd9bbec9cf9" />
<img width="1456" height="893" alt="Screenshot 2025-12-15 171627" src="https://github.com/user-attachments/assets/59d60016-7e13-483e-accd-60ea5fc51dde" />
**Output/TIMING Waveform**
<img width="1453" height="873" alt="image" src="https://github.com/user-attachments/assets/e965f77e-438d-44d7-9a28-1b4fa1e738cd" />
<img width="1456" height="908" alt="image" src="https://github.com/user-attachments/assets/736507d8-d1ad-476b-8006-cd5ddae42b37" />
 
**Result:**
Thus, the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
