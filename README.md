<h1 align="center">Bootcamp: Code from Scratch 🚀</h1>

- Week 1 : [Introduction to programming & Javascript](bootcamp/week01/)



## 2. JavaScript
## Week Challenges (Tuesday)
![alt text](images/logo.png)
### introduction to *codewars* 

### Kata 1. Multiply 
```html
<script>
function multiply(a, b){
 return a * b
}
</script>
```

### Kata 2. ASCII Total 
### You'll be given a string, and have to return the sum of all characters as an int. 
The function should be able to handle all ASCII characters.
### example: uniTotal("a") == 97 uniTotal("aaa") == 291
```html
<script>
function uniTotal(string) {
 var suma = 0; 
 for (let i= 0; i < string.length; i++) {
   suma += string.charCodeAt(i);
 }
return suma;
 }
</script>
```

### Kata 3. Char From ASCII Value 
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

### Kata 4. Binary Addition 
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


### Kata 5. Student's Final Grade 
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
## 2. JavaScript
## Week 2 Challenges (Wednesday)
### Kata 1.Holiday VIII - Duty Free
*The purpose of this kata is to work out just how many bottles of duty free whiskey you would have to buy 
such that the saving over the normal high street price would effectively cover the cost of your holiday.

You will be given the high street price (normPrice), the duty free discount (discount) and the cost of the holiday.

For example, if a bottle cost £10 normally and the discount in duty free was 10%, you would save £1 per bottle. 
If your holiday cost £500, the answer you should return would be 500.

All inputs will be integers. Please return an integer. Round down.*
```html
<script>
function dutyFree(normPrice, discount, hol){
  let Descuento = ((normPrice * discount) / 100);
  let Difc = hol / Descuento;
  let Ans = Math.floor(Dif);
  
  return Ans;
}
</script>
```

### Kata 2. Twice As Old 
Your function takes two arguments:
*current father's age (years) current age of his son (years)*
Сalculate how many years ago the father was twice as old as his son (or in how many years he will be twice as old).
```html
<script>
function twiceAsOld(dadYearsOld, sonYearsOld) {
  let Ads = sonYearsOld * 2;
  if (Ads > dadYearsOld) {
    return Ads - dadYearsOld;
  } else {
    return dadYearsOld - Ads;
  }
}
</script>
```
### Kata 3. Valid Spacing
Your task is to write a function called valid_spacing() which checks if a string has valid spacing. 
The function should return either true or false.

*the definition of valid spacing is one space between words*
```html
<script>
function validSpacing(s) {
    if(/^[\s]/.test(s) == true || /[\s]$/.test(s) == true) { 
     return false;
  }
  
  for(let i = 0; i < s.length; i++) {
    if(s.charAt(i) === ' '){ 
      if(i != 0 && s.charAt(i-1) === ' ') {
        return false;
      }
      if(i != (s.length - 1) && s.charAt(i+1) === ' ') {
        return false;
      }
    }
  }
  
  return true; 
}
</script>
```

### Kata 4. Fake Binary
*Given a string of digits, you should replace any digit below 5 with '0' 
and any digit 5 and above with '1'. Return the resulting string.

Note: input will never be an empty string*
```html
<script>
function fakeBin(x){
let xs ="";
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
```

## Week 2 Challenges (Thursday)
### Remove All Exclamation Marks From The End Of Sentence
*Exclamation marks series #2: 
Remove all exclamation marks from the end of sentence*
```html
<script>
function remove (str) {  
  const Regex = /!*$/g;
  return str.replace(Regex,'');
}
</script>
```
## Vowel Remover 
*Create a function called shortcut to remove 
the lowercase vowels (a, e, i, o, u ) in a given string.*
ex: "hello"     -->  "hll"
```html
<script>
function shortcut (string) {
  return string.replace(/[aeiou*]/g, '');
}
</script>
```

## Rock Paper Scissors 
*Let's play! You have to return which player won! In case of a draw return Draw!.*
ex: rps('scissors','paper') // Player 1 won!
```html
<script>
const rps = (p1, p2) => {

    switch (p1 + p2) {
        case "paperrock":
            return "Player 1 won!";
        case "rockscissors":
            return "Player 1 won!"
        case "scissorspaper":
            return "Player 1 won!"
        case "paperscissors":
            return "Player 2 won!";
        case "scissorsrock":
            return "Player 2 won!"
        case "rockpaper":
            return "Player 2 won!"
        default:
            return "Draw!";
    }
};
</script>
```
## Persistent Bugger 
*Write a function, persistence, that takes in a positive parameter 
num and returns its multiplicative persistence, which is the number
of times you must multiply the digits in num until you reach a single digit.*
ex: 39 --> 3 (because 3*9 = 27, 2*7 = 14, 1*4 = 4 and 4 has only one digit)
```html
<script>
function persistence(num) {
  let counter = 0;
  num = num.toString();
  while (num.length > 1) {
    counter++;
    num = num
      .split('')
      .map(Number)
      .reduce((a, b) => a * b)
      .toString();
  }
  return counter;
}
</script>
```
## 3. JavaScript 3
## week 3: JavaScript
### Week challenges (Monday)
1.Who likes it?
You probably know the "like" system from Facebook and other pages. People can "like" blog posts, 
pictures or other items. We want to create the text that should be displayed next to such an item.

Implement the function which takes an array containing the names of people that like an item. 
It must return the display text as shown in the examples:
Ex: ["Peter"] -->  "Peter likes this"

```html
<script>
function likes(names) {
 switch(names.length) {
      case 0:
      return 'no one likes this';
      case 1:
      return names[0] + ' likes this';
      case 2:
      return names[0] +' and ' + names[1] + ' like this';
      case 3:
      return names[0] +', ' + names[1] +  ' and '+ names[2] + ' like this';
      default:
      return names[0] + ', ' + names[1] + ' and '+ (names.length - 2) + ' others like this'; 
  }
}

likes(['Peter', 'Moninca', 'Luis', 'Mariel']);
</script>
```

2.Bit Counting
Write a function that takes an integer as input, and returns the number of bits that are equal 
to one in the binary representation of that number. You can guarantee that input is non-negative.

Example: The binary representation of 1234 is 10011010010, so the function should return 5 in this case.

```html
<script>
var countBits = function(n) {
  // Program Me
    let binary = n.toString(2);
    return parseInt(binary.split("1").length -1);
};	
</script>
```
3.Your Order, Please
Your task is to sort a given string. Each word in the string will contain a single number. 
This number is the position the word should have in the result.
## 404

## Week challenges (Tuesday)
1.Simple Pig Latin
Move the first letter of each word to the end of it, then add "ay" to the end of the word. 
Leave punctuation marks untouched.
*pigIt('Pig latin is cool'); // igPay atinlay siay oolcay*
# 404

2.Count the number of Duplicates
Write a function that will return the count of distinct case-insensitive 
alphabetic characters and numeric digits that occur more than once in the input string. 
The input string can be assumed to contain only alphabets (both uppercase and lowercase) 
and numeric digits.
# 404

3.Decode the Morse code 
Your task is to implement a function that would take the morse code as input 
and return a decoded human-readable string.

For example:
*decodeMorse('.... . -.--   .--- ..- -.. .')
//should return "HEY JUDE"*
# 404

### Week challenges (Thursday)
3. 1st Core Challenge :rocket:
Challenge description 
**Let’s write our Mission Statement!** In **one paragraph**, 
please answer to the next 5 questions:

1. Who are you?
2. What background do you have?
3. Who do you want to be?
4. What do you want to do?
5. What are the core values and principles that govern your character and contributions?
 ```
	I'm Abner and I'm passionate about web programming. 
	I was taking online courses about web development 
	because i want to learn all about it. I want to be 
	a full stack web developer to create amazing web apps 
	with a cool front-end ✨ and a powerful back-end 🤘. 
	I can be a little insecure but I always want to try, 
	i believe that the hard working has results.
```

