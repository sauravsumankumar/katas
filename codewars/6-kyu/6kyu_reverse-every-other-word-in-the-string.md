202208161722
Name: **Reverse every other word in the string**
Link: [Codewars](https://www.codewars.com/kata/58d76854024c72c3e20000de)
Level:  [[6 kyu]]
Tags: [[Arrays]] [[Fundamentals]]

---

# Reverse every other word in the string

Reverse every other word in a given string, then return the string. Throw away any leading or trailing white space, while ensuring there is exactly one space between each word. Punctuation marks should be treated as if they are a part of the word in this kata.

---

## Solution

``` javascript
const reverse=a=>{
  let phrase = a.split(' ')
  phrase = phrase.map((e,i,a)=>i%2!==0?e.split('').reverse().join(''):e)
  return phrase.filter(e=>e!=='',0).join(' ')
}
```