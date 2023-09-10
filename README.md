# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM :
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## EQUIPMENT REQUIRED :
Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime
## THEORY :
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). 

There are two types of subtractors.
1. Half Subtractor

2. Full Subtractor

## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## PROCEDURE :
1. Use module projname(input,output) to start the Verilog programmming.

2. Assign inputs and outputs using the word input and output respectively.

3. Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4. Use each output to represnt onre for differnce and the other for borrow.

5. End the verilog program using keyword endmodule.

## PROGRAM :
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: 212222240073
RegisterNumber:  Pradeep raj P

HALF SUBTRACTER :

module exp_4(a,b,diff,borr);
input a,b;
output diff,borr;
assign difference = (a^b);
assign borrow = (~a&b);
endmodule

FULL SUBTRACTER :

module exp_41(a,b,Bin,diff,borrow);
input a,b,Bin;
output diff,borrow;
assign diff = (a^b^Bin);
assign borrow = ~a&b|(~(a^b)&Bin);
endmodule

```

##  RTL REALIZATION :

### Half subtracter
![image](https://github.com/Pradeeppachiyappan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118707347/b9b09e81-0c54-4a4a-aa03-330dc6bcdabd)

### Full subtracter
![image](https://github.com/Pradeeppachiyappan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118707347/5d73dda5-c766-403b-8c94-909307b30e63)

## TRUTH TABLE :
### Half subtracter
![image](https://github.com/Pradeeppachiyappan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118707347/284bd523-6e27-4433-9a99-ff6886f83ae1)

### Full subtracter
![image](https://github.com/Pradeeppachiyappan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118707347/8a36177f-9ed6-417b-a5fd-7d692d262665)

## OUTPUT WAVEFORM :

#### Half subtracter
![image](https://github.com/Pradeeppachiyappan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118707347/f297c0f9-60a4-410f-88af-cdb5bd89413d)

#### Full subtracter
![image](https://github.com/Pradeeppachiyappan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118707347/d6087300-9885-4b94-92c4-9676f36acbb8)

## RESULT :
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
