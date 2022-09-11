202209111802
Name: **Count the smiley faces!**
Link: [Codewars](https://www.codewars.com/kata/583203e6eb35d7980400002a/)
Level:  [[6 kyu]]
Tags: [[Regular Expressions]] [[Fundamentals]]

---

# Count the smiley faces!

Given an array (arr) as an argument complete the function `countSmileys` that should return the total number of smiling faces.

Rules for a smiling face:

-   Each smiley face must contain a valid pair of eyes. Eyes can be marked as `:` or `;`
-   A smiley face can have a nose but it does not have to. Valid characters for a nose are `-` or `~`
-   Every smiling face must have a smiling mouth that should be marked with either `)` or `D`

No additional characters are allowed except for those mentioned.

**Valid smiley face examples:** `:) :D ;-D :~)`  
**Invalid smiley faces:** `;( :> :} :]`

## Example

``` js
countSmileys([':)', ';(', ';}', ':-D']);       // should return 2;
countSmileys([';D', ':-(', ':-)', ';~)']);     // should return 3;
countSmileys([';]', ':[', ';*', ':$', ';-D']); // should return 1;
```

---

## Solution

``` javascript
const countSmileys=arr=>arr.filter((e)=>e.match(/(:|;)(-|~)?(\)|D)/)).length
```