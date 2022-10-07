---
{"dg-publish":true,"permalink":"/computer-science/cpu/lmc/","dgHomeLink":true,"dgPassFrontmatter":false}
---


# Little Man Computer

### Task 1: Reverse Input
- Ask the user for three numbers and then repeat them in reverse order
```
00 STA 00  
01 INP  
02 STA 01  
03 INP  
04 STA 02  
05 LDA 02  
06 OUT  
07 LDA 01  
08 OUT  
09 LDA 00  
10 OUT  
11 HLT
```

### Task 2: 
- Ask the user for three numbers, add them and print out the answer
```
00 INP  
01 STA 00  
02 INP  
03 STA 01  
04 INP  
05 ADD 00  
06 ADD 01  
07 OUT  
08 HLT
```

### Task 3:
- Ask the user for one number, double it and print out the answer.
```
00 INP  
01 STA 00  
02 ADD 00  
03 OUT  
04 HLT
```

### Task 4:
- Ask the user for two numbers. Print out the answer to first number minus the second number followed by the answer to the second number minus the first number.
```
00 INP  
01 STA 00  
02 INP  
03 STA 01  
04 SUB 00  
05 OUT  
06 LDA 00  
07 SUB 01  
08 OUT  
09 HLT
```

```

```