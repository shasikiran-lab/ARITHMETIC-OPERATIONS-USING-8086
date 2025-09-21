# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```
#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2000                   |   79                     | 
|  2001                   |   88                     |
|  2002                   |   23                     |
|  2003                   |   02                     |


| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2004                   |   9C                     | 
|  2005                   |   8A                     |
|  2006                   |   00                     |


#### Manual Calculations

![WhatsApp Image 2025-09-21 at 21 30 28_3dfd9c3f](https://github.com/user-attachments/assets/6a095792-f702-48db-8b35-863cc50455aa)


---

## OUTPUT IMAGE FROM MASM SOFTWARE


![WhatsApp Image 2025-09-21 at 22 07 00_2f422786](https://github.com/user-attachments/assets/0015c93e-4416-40b2-af95-8fbe2d9ec823)

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2000                   |   79                     | 
|  2001                   |   88                     |
|  2002                   |   23                     |
|  2003                   |   02                     |


| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2004                   |   56                     | 
|  2005                   |   86                     |
|  2006                   |   00                     |
#### Manual Calculations

![sub](https://github.com/user-attachments/assets/b6aa72b3-b140-4abb-8f23-8354e32eeafe)

---


## OUTPUT SCREEN FROM MASM SOFTWARE

![WhatsApp Image 2025-09-21 at 22 13 18_97b0ce03](https://github.com/user-attachments/assets/b69308d9-f67e-4ca5-a89c-a069144134cc)

## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2000                   |   02                     | 
|  2001                   |   00                     |
|  2002                   |   03                     |
|  2003                   |   00                     |


| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2004                   |   06                     | 
|  2005                   |   00                     |
|  2006                   |   00                     |
#### Manual Calculations

![mul](https://github.com/user-attachments/assets/7a11c560-b9eb-4673-888f-012603af4b17)


---

## OUTPUT SCREEN FROM MASM SOFTWARE

![WhatsApp Image 2025-09-21 at 22 15 47_7e930f4d](https://github.com/user-attachments/assets/be29e2e4-37e4-43e4-a57f-b110ef4fbf30)

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2000                   |   69                     | 
|  2001                   |   24                     |
|  2002                   |   34                     |
|  2003                   |   12                     |


| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2004                   |   02                     | 
|  2005                   |   00                     |
|  2006                   |   01                     |
#### Manual Calculations

![div](https://github.com/user-attachments/assets/48eac901-d117-4d12-8bbc-c26d1d786572)


---
## OUTPUT FROM MASM SOFTWARE


![WhatsApp Image 2025-09-21 at 22 18 27_a986f312](https://github.com/user-attachments/assets/6ae55dc7-cae4-4746-8ed6-0072a1cb625d)


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

