# Interpreted And Compiled Programming Languages
## first of all ==> what are they? 
### in short a compiled programming language required a program called *compiler* the fuction of a compiler is convert the whole code into machine languague or binary code. instead a interpreted language is not directly convert into machine language otherwise is executed line by line for an *interpreter*

#Advantages 
### Compiled
1. Compiled languages are faster because the *compiler* read the whole code and covert it into machine languague inside the same machine.
2. The code is secure because you only send a binary file (executable version of your code that only can be read for the machine)
### Interpreted
1. cross-platform, only interpreter needed 
2. less secure because if you need to send your program you send a copy of your code
3. Easy to test

# Ex 2 : Is Java compiled or interpreted, or both?
### Java is a hybrid, compiled to mid-language called bytecode and later it is interpreted 

# Ex 3: Pseudocode currency converter
  1. START
  2. Dollars <-- GET
  3. BitCoinConst <-- 0.000022
  4. ConvertedValue <-- Dollars * BitCoinConst
  5. PRINT ConvertedValue
  6. END
# Wednesday - third day - week #1
## Exercise 1 ==> Your date of birth in the matrix? 
### Explain to your *team* how to convert their birth year into binary code 
At first place, to convert a decimal number (base 10) into a binary number (base 2) you need to know the power of 2. 
***
## 2 to the power of n (multiplies by itself n times). 
once learned that, let see power of 2 up to 11 
| 2^1    | 2^2  | 2^3 | 2^4 | 2^5 | 2^6 | 2^7  | 2^8 | 2^9 | 2^10 | 2^11 |              
| ------ |:----:| ---:|:---:| ---:| --- |:----:| ---:|:---:| ----:| ----:|
| 2      | 4    | 8   |  16 | 32  | 64  | 128  | 256 | 512 | 1024 | 2048 |

now we learn how to convert a birth year into binary number with the practice: Let's see 1996
### substract method 
In this example we will use the substract method, we already have a number *1996*
1. First step is find the closest number of 1996, *2048* exceed our target number so we will start with *1024*
2. Substract *1024* to *1996* that's equal to *972* and we continue substracting but now with the result *972*
3. now the closest number of *972* is *512* so we only need to substract *972 - 512* and that's equal to *460*
4. for *460* the closest number is *256* and that's *204*
5. we do the same for *204*, the closest number is *128* and the result of substracting is *76*
6. now *76* - *64* and the result will be > 12
7. we almost done, *12* - *8* = *4*
8. *4* - *4* is equal to *0*

### once we do it we take every number used for substracting our target number and add a 1 if we used it and 0 if we didn't
| 2^1    | 2^2  | 2^3 | 2^4 | 2^5 | 2^6 | 2^7  | 2^8 | 2^9 | 2^10 |           
| ------ |:----:| ---:|:---:| ---:| --- |:----:| ---:|:---:| ----:|
| 2      | 4    | 8   |  16 | 32  | 64  | 128  | 256 | 512 | 1024 |
| 0      | 1    | 1   |  0  | 0   | 1   | 1    | 1   | 1   | 1    |

we read the number from highest to lowest, so *1996* in binary is equal to *11111001100* if you want to check your operation, add all the numbers used 
*1024 + 512 + 256 + 128 + 64 + 8 + 4 = 1996* 

# MIPS
## ex 2 part 1 ==> Create a program that adds any two given numbers provided by the user
```
 .data
        FirstInput: .asciiz "\nPls Insert the first number: "
	SecondInput: .asciiz "\nPls Insert the second number: "
	Result: .asciiz "\nThe Result is: "
	   
  .text
        main:
              li $v0, 4
              la $a0, FirstInput
              syscall

              li $v0, 5
              syscall
              
              move $t0, $v0
              
              li $v0, 4
              la $a0, SecondInput
              syscall

              li $v0, 5
              syscall
              
              move $t1, $v0
              
              add $t2, $t0, $t1
              
              li $v0, 4
              la $a0, Result
              syscall
              
              li $v0, 1
              move $a0, $t2
              syscall

```
## ex 2 part 1 ==> Create a program that displays your name

```
 .data
        Myname: .asciiz "\nHi, My name is Abner :D "
	   
  .text
        main:
              li $v0, 4
              la $a0, Myname
              syscall


```

