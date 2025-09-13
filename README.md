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
|      1200:12            |   1204:44                |
|      1201:34            |   1205:68                |
|      1202:12            |   1206:00                |
|      1203:34            |   1207:C4                |
#### Manual Calculations

<img width="553" height="563" alt="image" src="https://github.com/user-attachments/assets/c80148af-1846-4792-acaa-3fdd337129b9" />


## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="653" height="393" alt="image" src="https://github.com/user-attachments/assets/2bd9ff34-32c1-41f3-9a04-684f257d0ad0" />

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
|      1200:12            |   1204:00                |
|      1201:34            |   1205:00                |
|      1202:12            |   1206:83                |
|      1203:34            |   1207:C4                |

#### Manual Calculations

<img width="550" height="564" alt="image" src="https://github.com/user-attachments/assets/d0ff2e86-0a93-4712-a4e9-8c9e7b27e900" />



## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="593" height="397" alt="image" src="https://github.com/user-attachments/assets/7753c88b-0fc6-48df-9394-c316b10e3f81" />

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
|      1200:12            |   1204:44                |
|      1201:34            |   1205:51                |
|      1202:12            |   1206:97                |
|      1203:34            |   1207:0A                |

#### Manual Calculations

<img width="573" height="554" alt="image" src="https://github.com/user-attachments/assets/9ea4d5da-670e-4c77-99bf-1ceca29ed0d6" />


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="583" height="378" alt="image" src="https://github.com/user-attachments/assets/8d777154-eaf3-4df5-813a-5d66df5323cb" />

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
|      1200:12            |   1204:01                |
|      1201:34            |   1205:00                |
|      1202:12            |   1206:00                |
|      1203:34            |   1207:00                |

#### Manual Calculations

<img width="600" height="521" alt="image" src="https://github.com/user-attachments/assets/1c3470dc-2f06-44fc-9b0f-674e411edc7d" />

## OUTPUT FROM MASM SOFTWARE

<img width="576" height="387" alt="image" src="https://github.com/user-attachments/assets/200ebdde-6bc9-44a0-9243-024e537e9c31" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
