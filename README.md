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
<img width="1050" height="738" alt="Screenshot 2026-03-10 094639" src="https://github.com/user-attachments/assets/79d6b375-fe21-4a3f-8e64-47f2d10fbd85" />

<img width="1102" height="719" alt="Screenshot 2026-03-10 094649" src="https://github.com/user-attachments/assets/b28a81ac-9acc-4ce5-838e-9300962b6320" />




**Procedure**


1.Type the program in Quartus software
2.Compile and run the program
3.Generate the RTL schematic and save the logic diagram
4.Create nodes for inputs and outputs to generate the timing diagram
4.For different inputs combinations generate the timing diagram



**Program-1:**
```

module deexp3(
    input A, B, Cin,
    output Sum, Carry
);

    assign Sum   = A ^ B ^ Cin;
    assign Carry = (A & B) | (Cin & (A ^ B));

endmodule
```



**RTL Schematic-1**
<img width="1920" height="1080" alt="Screenshot (187)" src="https://github.com/user-attachments/assets/d040065f-7748-47a1-9675-804f7fe65263" />


**Output Timing Waveform-1**
<img width="1920" height="1080" alt="Screenshot (186)" src="https://github.com/user-attachments/assets/5a111b8a-dc4e-45d9-9518-3ab7028e796c" />

**Program-2:**

```
module deexp3a(
    input A, B, Bin,
    output Difference, Borrow
);

    assign Difference = A ^ B ^ Bin;
    assign Borrow     = (~A & B) | (~A & Bin) | (B & Bin);

endmodule
```


**RTL Schematic-2**
<img width="1920" height="1080" alt="Screenshot (188)" src="https://github.com/user-attachments/assets/e14edf25-38f7-4ac1-9f0b-f3b57092c3f3" />





**Output Timing Waveform-2**

<img width="1920" height="1080" alt="Screenshot (189)" src="https://github.com/user-attachments/assets/e29b205a-093c-4f7e-a448-be57ef2dade7" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



