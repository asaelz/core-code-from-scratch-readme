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