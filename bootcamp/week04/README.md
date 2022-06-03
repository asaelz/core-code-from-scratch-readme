## Week 4: End Of Month & Pause Day
Introduction to Regex
-*Week challenges (Wednesday)*

Ex 1: Simple Validation Of A Username

*Instructions:*
Write a simple regex to validate a username. Allowed characters are:

*lowercase letters,numbers & underscore*

*Length should be between 4 and 16 characters (both included).*
```html
<script>
 function validateUsr(username) {
    return  /^[a-z0-9-_]{4,16}$/g.test(username);
 }
</script>
```

Ex 2: Get number from string

*Instructions:*

Write a function which removes from string all non-digit characters and parse the remaining to number. E.g: "hell5o wor6ld" -> 56

```html
<script>
function getNumberFromString(s) {
    return parseInt(s.replace(/[\D]/g,''));
 }
</script>
```
-*Week challenges (Wednesday)*

Ex 1: Your boss decided to save money by purchasing some cut-rate optical character recognition software for scanning in the text of old novels to your database. At first it seems to capture words okay, but you quickly notice that it throws in a lot of numbers at random places in the text.

Examples (input -> output)
'! !'                 -> '! !'
'123456789'           -> ''
'This looks5 grea8t!' -> 'This looks great!'

```html
<script>
function stringClean(s){
  // Function will return the cleaned string
  return s.replace(/[\d]/g,'');
}
</script>
```

Ex 2: You need to write regex that will validate a password to make sure it meets the following criteria:

*At least six characters long
contains a lowercase letter
contains an uppercase letter
contains a number*

Valid passwords will only be alphanumeric characters.
```html
<script>
function validate(password) {
  return /^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)[a-zA-Z\d]{6,}$/g.test(password);
}
</script>
```