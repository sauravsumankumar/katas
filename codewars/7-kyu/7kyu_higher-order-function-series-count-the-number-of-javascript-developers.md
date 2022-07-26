202207261103
Name: **Coding Meetup #1 - Higher-Order Functions Series - Count the number of JavaScript developers coming from Europe**
Link: [Codewars]()
Level:  [[7 kyu]]
Tags: [[Data-Structures]] [[Fundamentals]] [[Algorithms]] [[Strings]] [[Regular Expressions]] [[Arrays]] [[Funtional-prgramming]]

---

# Coding Meetup #1 - Higher-Order Functions Series - Count the number of JavaScript developers coming from Europe

You will be given an array of objects (hashes in ruby) representing data about developers who have signed up to attend the coding meetup that you are organising for the first time.

Your task is to **return the number of JavaScript developers coming from Europe**.

**Example**:

```javascript
var list1 = [
  { firstName: 'Noah', lastName: 'M.', country: 'Switzerland', continent: 'Europe', age: 19, language: 'JavaScript' },
  { firstName: 'Maia', lastName: 'S.', country: 'Tahiti', continent: 'Oceania', age: 28, language: 'JavaScript' },
  { firstName: 'Shufen', lastName: 'L.', country: 'Taiwan', continent: 'Asia', age: 35, language: 'HTML' },
  { firstName: 'Sumayah', lastName: 'M.', country: 'Tajikistan', continent: 'Asia', age: 30, language: 'CSS' }
];
```

Your function should return number `1`.

---

## Solution 1

``` javascript
countDevelopers=list=>{
  let counter = 0
  list.map(e=> (e.continent === 'Europe' && e.language === 'JavaScript') && counter++)
  return counter
}
```

## Solution 2

``` javascript
countDevelopers=list=>list.filter(e=>(e.continent === 'Europe' && e.language === 'JavaScript')).length
```