202207252248
Name: **Sorted? yes? no? how?**
Link: [Codewars](https://www.codewars.com/kata/580a4734d6df748060000045)
Level: [[7 kyu]]
Tags: [[Arrays]] [[Sorting]] [[Fundamentals]]

---

# Sorted? yes? no? how?

Complete the method which accepts an array of integers, and returns one of the following:

-   `"yes, ascending"` - if the numbers in the array are sorted in an ascending order
-   `"yes, descending"` - if the numbers in the array are sorted in a descending order
-   `"no"` - otherwise

You can assume the array will always be valid, and there will always be one correct answer.

---

## Solution

``` javascript
const isSortedAndHow = arr => {
  const ascending = [...arr].sort((a,b)=>a-b)
  const descending = [...arr].sort((a,b)=>b-a)
  if (arr.every((n,i)=>n===descending[i])) return 'yes, descending'
  if (arr.every((n,i)=>n===ascending[i])) return 'yes, ascending'
  return 'no'
}
```