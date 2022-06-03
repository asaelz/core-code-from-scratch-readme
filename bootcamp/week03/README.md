## week 3: JavaScript
![alt text](/images/week3.png)

## 3. JavaScript 3
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

### Week challenges (Wednesday)
Ex 1: Valid Parentheses
Write a function that takes a string of parentheses, and determines if the order of the parentheses is valid. The function should return true if the string is valid, and false if it's invalid.

Examples
"()"              =>  true
")(()))"          =>  false
"("               =>  false
"(())((()())())"  =>  true

```html
<script>
  function validParentheses(parens) {
    let valid = 0;
    for (let i = 0; i < parens.length; i++) {
      if (parens[i] === ')') valid--;
      if (parens[i] === '(') valid++;
      if (valid < 0) return false;
    }
    return valid == 0;
}
</script>
```

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

