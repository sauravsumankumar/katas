202208222143
Name: **How many pages in a book?**
Link: [Codewars](https://www.codewars.com/kata/622de76d28bf330057cd6af8)
Level:  [[6 kyu]]
Tags: [[Puzzles]] [[Algorithms]]

---

# How many pages in a book?

Every book has `n` pages with page numbers `1` to `n`. The `summary` is made by adding up the **number of digits** of all page numbers.

Task: Given the `summary`, find the number of pages `n` the book has.

**Example**:

If the input is `summary=25`, then the output must be `n=17`: The numbers 1 to 17 have 25 digits in total: `1234567891011121314151617`.

---

## Solution

``` javascript
const amountOfPages = n =>{
  let counter = 1, str = ''
  
  while (str.length < n){
    str += counter
    counter++
  }
  return counter-1
}
```