# code-from-scratch

# Tuesday - week #1
# Interpreted And Compiled Programming Languages
## first of all ==> what are they? 
### in short a compiled programming language requires a program called *compiler* the fuction of a compiler is convert the whole code into machine languague or binary code. instead a interpreted language is not directly convert into machine language otherwise is executed line by line for an *interpreter*

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
# Thursday - Fourth day - week 1
## Ex 1 ==> Print special numbers
### Use an iterative flow control to be able to print all the even numbers in the range of numbers from 0 to 100.
```html
<script>
// Even numbers up to 100
for (var i = 1; i<=100; i++)
{
  if (i % 2 === 0) {
    if (i===2) {console.log('List of Even numbers up to 100: ');}
    console.log(i);
  }
}
</script>		       		       
```

## Ex 2 ==> Bad code
### The code shown below is not working in the right way, as a task you must find the error made by the developer who programmed this code and correct it, for this exercise you must explain what the error is and place the correct code

```html
<script>
var cond = false;
// error is here, "=" means assignment but we need comparison "=="
if ((cond = true)) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}
</script>
```
### code fixed: 
```html
<script>
var cond = false;
if (cond == true) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}
</script>
```
## Ex 3 ==> Bad code 2
### You must create the code that follows the following logic, if the given number is 100, take this number as special and show the following message: "This is a special number!", but if the number is less than 1000, multiple of 10 and different from 100, you must show the following message: "This number is almost special". if none of the given conditions are met show the following message: "Just a regular number". Another developer was trying to program the logic, but apparently couldn't, you need to fix the code to work properly.

```html
<script>
var n = 100; // Just a regular number. n = 90 Almost Special. 

if (n == 100) {
  console.log('This is a special number!');
}
else if (n < 1000 && n !=100 && n % 10 == 0 ) {
  console.log('This number is almost special');
} else {
  console.log('Just a regular number');
}
</script>
```

# Week 2 - JavaScript
## Week Challenges (Tuesday)
![alt text](images/logo.png)
### introduction to *codewars* 

### Kata 1. Multiply **:muscle:**
```html
<script>
function multiply(a, b){
 return a * b
}
</script>
```

### Kata 2. ASCII Total :ok_hand:
### You'll be given a string, and have to return the sum of all characters as an int. 
The function should be able to handle all ASCII characters.
### example: uniTotal("a") == 97 uniTotal("aaa") == 291
```html
<script>
function uniTotal(string) {
 var suma = 0; 
 for (var i= 0; i < string.length; i++) {
   suma += string.charCodeAt(i);
 }
return suma;
 }
</script>
```

### Kata 3. Char From ASCII Value :+1:
### Write a function get_char() / getChar() which takes a number and 
returns the corresponding ASCII char for that value.
### example: get_char(65) should return 'A'
```html
<script>
function getChar(c){
 return String.fromCharCode(c)
}

getChar(5);
</script>
```

### Kata 4. Binary Addition :muscle:
### Implement a function that adds two numbers together and returns their sum in binary. 
The conversion can be done before, or after the addition.
*The binary number returned should be a string.*
### example: 1, 1 --> "10" (1 + 1 = 2 in decimal or 10 in binary)
```html
<script>
function addBinary(a,b) {
  return (a + b).toString(2);
}
</script>
```


### Kata 5. Student's Final Grade :sparkles:
### Create a function finalGrade, which calculates the final grade of a 
student depending on two parameters: a grade for the exam and a number of completed projects.

###This function should take two arguments: exam - grade for exam (from 0 to 100); projects - 
number of completed projects (from 0 and above)

*This function should return a number (final grade). There are four types of final grades:*

1. 100, if a grade for the exam is more than 90 or if a number of completed projects more than 10.
2. 90, if a grade for the exam is more than 75 and if a number of completed projects is minimum 5.
3. 75, if a grade for the exam is more than 50 and if a number of completed projects is minimum 2.
4. 0, in other cases
### example: 100, 12 --> 100
```html
<script>
function finalGrade (exam, projects) {
  if (exam > 90 || projects > 10)
    {
      return 100;
    } else if(exam > 75 && projects >= 5)
      {
        return 90;
      } else if(exam > 50 && projects >= 2)
        {
          return 75;
        }
  else{
    return 0;
  }
  
}
</script>
```
# Week 2 - JavaScript
## Week Challenges (Wednesday)
1. Holiday VIII - Duty Free
*The purpose of this kata is to work out just how many bottles of duty free whiskey you would have to buy 
such that the saving over the normal high street price would effectively cover the cost of your holiday.

You will be given the high street price (normPrice), the duty free discount (discount) and the cost of the holiday.

For example, if a bottle cost £10 normally and the discount in duty free was 10%, you would save £1 per bottle. 
If your holiday cost £500, the answer you should return would be 500.

All inputs will be integers. Please return an integer. Round down.*
```html
<script>
function dutyFree(normPrice, discount, hol){
  var Descuento = ((normPrice * discount) / 100);
  var Difc = hol / Descuento;
  var Ans = Math.floor(Dif);
  
  return Ans;
}
</script>
```

2. Twice As Old 
Your function takes two arguments:
*current father's age (years) current age of his son (years)*
Сalculate how many years ago the father was twice as old as his son (or in how many years he will be twice as old).
```html
<script>
function twiceAsOld(dadYearsOld, sonYearsOld) {
  Ads = sonYearsOld * 2;
  if (Ads > dadYearsOld) {
    return Ads - dadYearsOld;
  } else {
    return dadYearsOld - Ads;
  }
}
</script>
```

4. Fake Binary
*Given a string of digits, you should replace any digit below 5 with '0' 
and any digit 5 and above with '1'. Return the resulting string.

Note: input will never be an empty string*
```html
<script>
function fakeBin(x){
var xs ="";
for (var i = 0; i < x.length; i++) { 
if (x.charAt(i) < 5) {
  xs += "0"
} else {
  xs += "1";
}
}
  return xs;
}

fakeBin("38");	
</script>
