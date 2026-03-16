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
```
ORG 0000H
MOV A, 30H     
ADD A, 31H    
MOV 40H, A 
JNC NEXT 
MOV 41H, #01H
SJMP END_PROGRAM
NEXT: MOV 41H, #00H
END_PROGRAM: NOP
END
```

## Output:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4169f552-540c-4e81-b3ab-8a8c554212b5" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a7152a05-2659-440b-bafd-f74262e002dc" />


## For Subtraction:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Subtract B from A.
4.	Store the result in memory location 40H.

## Program:
```
ORG 0000H
MOV A, 30H
SUBB A, 31H
MOV 40H, A
JNC NEXT
MOV 41H, #01H
SJMP END_PROGRAM
NEXT: MOV 41H, #00H
END_PROGRAM: NOP
END
```

## Output:
<img width="1910" height="912" alt="image" src="https://github.com/user-attachments/assets/922ddc96-7634-4af0-8164-e8e71f308a19" />
<img width="1915" height="909" alt="image" src="https://github.com/user-attachments/assets/e8bdf4b8-5a2b-4be4-99a1-333412a995cb" />

## For Multiplication:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Multiply A and B.
4.	Store the lower byte of the result in memory location 40H.
5.	Store the higher byte of the result in memory location 41H.

## Program:
```
ORG 0000H
MOV A, 30H 
MOV B, 31H
MUL AB
MOV 40H, A 
MOV 41H, B
END
```
## Output:
<img width="1918" height="1137" alt="image" src="https://github.com/user-attachments/assets/f01fb0ed-39cf-467c-a56e-4d6bd55e0467" />
<img width="1919" height="1137" alt="image" src="https://github.com/user-attachments/assets/117ca2d2-2117-4a29-907c-9e011e72cc56" />

## For Division:
1.	Load the dividend from memory location 30H into register A.
2.	Load the divisor from memory location 31H into register B.
3.	Divide A by B.
4.	Store the quotient in memory location 40H.
5.	Store the remainder in memory location 41H.

## Program:
```
ORG 0000H
MOV A, 30H
MOV B, 31H
DIV AB
MOV 40H, A
MOV 41H, B 
END
```

## Output:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/02f0277e-1124-4b45-b277-204bfca0d660" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0df0f5c7-4ed2-46fc-86f7-c9cb5f47c36a" />

## Result:
The 8-bit arithmetic operations using the 8051 microcontroller have been successfully executed and verified using Keil software.

