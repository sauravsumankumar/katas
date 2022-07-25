202207252222
Name: **Alternate capitalization**
Link: [Codewars](https://www.codewars.com/kata/59cfc000aeb2844d16000075)
Level:  [[7 kyu]]
Tags: [[Strings]] [[Fundamentals]]

---

# Alternate capitalization

Given a string, capitalize the letters that occupy even indexes and odd indexes separately, and return as shown below. Index `0` will be considered even.

**Example**:
`capitalize("abcdef") = ['AbCdEf', 'aBcDeF']`. See test cases for more examples.

The input will be a lowercase string with no spaces.

---

## Solution 1

``` javascript
capitalize=s=>{
  const even = s.split('').map((e,i,a)=>i%2?e.toLowerCase():e.toUpperCase()).join('')
  const odd = s.split('').map((e,i,a)=>i%2!==0?e.toUpperCase():e.toLowerCase()).join('')
  return [even, odd] 
}
```

## Solution 2

``` javascript
capitalize=s=>{
  const word1 = s.split('').map((e,i,a)=>i%2?e.toLowerCase():e.toUpperCase()).join('')
  const word2 = s.split('').map((e,i,a)=>i%2?e.toUpperCase():e.toLowerCase()).join('')
  return [word1, word2] 
}
```


