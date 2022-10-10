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


# Part 2
### Task 1:
Ask the user for two numbers and print out the biggest
```
INP
STA 99
INP
STA 98
SUB 99
BRP isPositive
LDA 99
BRA end
isPositive LDA 98
end OUT
HLT
```

### Task 2:
Ask the user for two numbers, If they are the same then print 0, otherwise add them and print out the answer
```
INP
STA 99
INP
STA 98
SUB 99
BRZ isZero
LDA 99
ADD 98
isZero OUT
HLT
```

### Task 3:
Ask the user for one larger number and one factor of that number (e.g. 15 and 3, 20 and 5). The program should keep subtracting the smaller number until it reaches 0 - where it should print out 0.
```
INP
STA 99
INP
STA 98
LDA 99
loop SUB 98
BRZ isZero
BRP loop
isZero OUT
HLT
```