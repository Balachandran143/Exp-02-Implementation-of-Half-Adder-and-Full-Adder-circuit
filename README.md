# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: 
RegisterNumber:  
### HALF ADDER:
```
module add(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
```
### FULL ADDER:
```
module fulladd(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```

### Output:
### HALF ADDER:
### RTL realization:
![Screenshot 2023-09-23 091757](https://github.com/Balachandran143/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/118886489/f7cc1006-e815-44bb-983d-8e88bcf749eb)

### TIMING DIAGRAM:
![Screenshot 2023-09-23 091952](https://github.com/Balachandran143/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/118886489/e00b6af9-88f2-4a39-b852-3f5660291c95)

### TRUTH TABLE:
![Screenshot 2023-09-23 092058](https://github.com/Balachandran143/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/118886489/2e9cc0a7-44dd-4741-9bfa-47a67d53449d)

### FULL ADDER:
### RTL realization:
![Screenshot 2023-09-23 092205](https://github.com/Balachandran143/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/118886489/e80a7217-fe74-4c16-a751-4fee1af677cf)
### TIMING DIAGRAM:
![Screenshot 2023-09-23 092331](https://github.com/Balachandran143/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/118886489/b5f260b6-8fe8-41a4-8640-2769a0b63ea2)
### TRUTH TABLE:
![Screenshot 2023-09-23 092357](https://github.com/Balachandran143/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/118886489/47866cf3-7a26-4ec0-ac90-71fba9a2c357)

### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using
Verilog programming.
