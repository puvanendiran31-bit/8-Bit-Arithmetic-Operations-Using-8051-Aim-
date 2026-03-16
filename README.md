# 8-Bit-Arithmetic-Operations-Using-8051

## Aim:
To perform 8-bit arithmetic operations such as addition, subtraction, multiplication, and division using the 8051 microcontroller.

## Apparatus Required:

•	Laptop with Keil uVision software

## Algorithm:

## For Addition:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Add the contents of registers A and B.
4.	Store the result in memory location 40H.
5.	Store the carry (if any) in 41H.

## Program:
~~~
MOV A, 30H     
ADD A, 31H    
MOV 40H, A 
JNC NEXT 
MOV 41H, #01H
SJMP END_PROGRAM
NEXT: MOV 41H, #00H
END_PROGRAM: NOP
END
~~~

## Output:
<img width="1916" height="968" alt="Screenshot 2026-03-12 142809" src="https://github.com/user-attachments/assets/6af28191-4704-4a8d-b6f2-e3564c145492" />
<img width="1910" height="960" alt="Screenshot 2026-03-12 143541" src="https://github.com/user-attachments/assets/776b0ea2-08b6-4875-8d53-17866453cf90" />

   
## For Subtraction:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Subtract B from A.
4.	Store the result in memory location 40H.

## Program:
~~~
ORG 000H
MOV A, 30H
SUBB A, 31H
MOV 40H, A
JNC NEXT
MOV 41H,#01H;
SJMP END_PROGRAM;
NEXT:MOV 41H,#00H;
END_PROGRAM:NOP;
END
~~~


## Output:
<img width="1916" height="967" alt="Screenshot 2026-03-12 142548" src="https://github.com/user-attachments/assets/21e90cef-43aa-4d97-b098-9c63dc9ceaf7" />
<img width="1918" height="995" alt="Screenshot 2026-03-12 142628" src="https://github.com/user-attachments/assets/bbb99eee-ebaa-4038-9b93-575a4297b7c4" />

## For Multiplication:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Multiply A and B.
4.	Store the lower byte of the result in memory location 40H.
5.	Store the higher byte of the result in memory location 41H.

## Program:
~~~
ORG 0000H
MOV A, 30H 
MOV B, 31H
MUL AB
MOV 40H, A 
MOV 41H, B
END
~~~

## Output:
<img width="1919" height="967" alt="Screenshot 2026-03-12 184715" src="https://github.com/user-attachments/assets/900f12e3-f9cf-4597-88fb-1e657f34bdd7" />

<img width="1919" height="995" alt="Screenshot 2026-03-12 184658" src="https://github.com/user-attachments/assets/8c3f4804-de76-4dca-8774-5003e43cf647" />

## For Division:
1.	Load the dividend from memory location 30H into register A.
2.	Load the divisor from memory location 31H into register B.
3.	Divide A by B.
4.	Store the quotient in memory location 40H.
5.	Store the remainder in memory location 41H.


## Program:
~~~
ORG 0000H
MOV A, 30H
MOV B, 31H
DIV AB
MOV 40H, A
MOV 41H, B 
END
~~~

## Output:
<img width="1913" height="988" alt="Screenshot 2026-03-12 185653" src="https://github.com/user-attachments/assets/c0af61de-98ff-4ded-985a-e81a92f82ebf" />
<img width="1918" height="990" alt="Screenshot 2026-03-12 185709" src="https://github.com/user-attachments/assets/b8788c83-5918-4396-820d-0c41424b9b63" />


## Result:
The 8-bit arithmetic operations using the 8051 microcontroller have been successfully executed and verified using Keil software.

