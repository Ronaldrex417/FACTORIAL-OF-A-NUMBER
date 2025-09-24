..# FACTORIAL-OF-A-NUMBER
# FACTORIAL OF A NUMBER USING 8051 (Keil)

## AIM
To write and execute an Assembly language program to perform the factorial of a number using 8051 Keil.

---

## APPARATUS REQUIRED
- Personal computer with Keil software

---

## ALGORITHM
1. **Start**
2. **Input**: Read the number `n`.
3. **Initialize**:
   - Set factorial to `1`.
   - Set `i` to `1`.
4. **Loop**: While `i` is less than or equal to `n`:
   - Multiply factorial by `i`.
   - Increment `i` by `1`.
5. **Output**: Store or print the value of factorial.
6. **End**

---

## FLOWCHART
<img width="506" height="525" alt="image" src="https://github.com/user-attachments/assets/f3b47187-6f0f-490c-8704-f2973cb2b276" />


---

## PROGRAM
```asm
ORG 0000H
MOV DPTR,#4500H
MOVX A,@DPTR
MOV R0,A
INC DPTR
ACALL FACTORIAL
MOVX @DPTR,A
SJMP THIN
FACTORIAL:DEC R0
CJNE R0,#01H,PRODUCT
SJMP THICK
PRODUCT:MOV B,R0
MUL AB
ACALL FACTORIAL
THICK: RET
THIN:RET
END

```
OUTPUT
<img width="719" height="590" alt="Screenshot 2025-09-24 222205" src="https://github.com/user-attachments/assets/ae40bc0e-5d0d-4517-ab84-83d86bbe987d" />
<img width="826" height="382" alt="Screenshot 2025-09-24 222220" src="https://github.com/user-attachments/assets/3cde0615-22ac-4c67-924c-23d00d62b2bb" />



---
MANUAL CALCULATIONS
![WhatsApp Image 2025-09-24 at 22 38 41_59e9db6c](https://github.com/user-attachments/assets/4148bb3c-cb96-42c1-a1e8-b2e8fe477990)

---

RESULT

Thus, the factorial of a number was calculated and executed successfully using 8051 Keil.

---


