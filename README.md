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

## Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
 ## Program:
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Thirukaalathessvarar S
RegisterNumber:  212222230161
*/
```
 ## Full Adder
```
module fulladder(a,b,c,S,K);
input a,b,c;
output S,K;
wire d,e,f;
xor (d,a,b);
xor (S,d,c);
and (e,c,d);
or (K,e,f);
endmodule
```
 ## Half adder
 ```
 module halfadder(a,b,s,c);
 input a,b;
 output s,c;
 xor (s,a,b);
 and (c,a,b);
 endmodule
 ```
## OUTPUT :

## RTL Diagram :
 ### Full adder
 ![full add rtl](https://user-images.githubusercontent.com/121166390/228719416-82d9d0f4-4d04-49c5-8f1c-33f0fad79bcf.png)

 ### Half adder
 ![half add rtl](https://user-images.githubusercontent.com/121166390/228126948-fadb2b74-c199-4465-8872-bec944a7f896.png)


## TIMING DIAGRAM :
 ### Full adder
 ![full add timing](https://user-images.githubusercontent.com/121166390/228719866-4dbbfbda-b9fa-4299-b54b-f6367f7f3d47.png)

 ### Half adder
![half adder truth](https://user-images.githubusercontent.com/121166390/228719513-d6a9e89f-39da-4c97-985c-d7a861fd288a.png)

 
 

### TRUTH TABLE :
## Full adder
![full adder truth](https://user-images.githubusercontent.com/121166390/228127667-2a36743d-e1cd-4b75-b312-aa5b4820f7de.png)

## Half adder
![half adder truth](https://user-images.githubusercontent.com/121166390/228127727-9a3032e4-0b56-413c-a5b1-10cbfdcfb349.png)



## RESULT :
Therefore, half adder and full adder is verified
