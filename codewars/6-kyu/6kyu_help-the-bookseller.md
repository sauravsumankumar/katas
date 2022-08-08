202208082115
Name: **Help the bookseller !**
Link: [Codewars]()
Level:  [[6 kyu]]
Tags: [[Fundamentals]] [[Algorithms]]

---

# Help the bookseller !

A bookseller has lots of books classified in 26 categories labelled A, B, ... Z. Each book has a code `c` of 3, 4, 5 or more characters. The **1st** character of a code is a capital letter which defines the book category.

In the bookseller's stockist each code `c` is followed by a space and by a positive integer n (int n >= 0) which indicates the quantity of books of this code in stock.

**Example**:

``` js
L = {"ABART 20", "CDXEF 50", "BKWRK 25", "BTSQZ 89", "DRTYM 60"}.
or
L = ["ABART 20", "CDXEF 50", "BKWRK 25", "BTSQZ 89", "DRTYM 60"] or ....
```

Your task is to find all the books of L with codes belonging to each category of M and to sum their quantity according to each category.

``` js
M = {"A", "B", "C", "W"} 
or
M = ["A", "B", "C", "W"] or ...

(A : 20) - (B : 114) - (C : 50) - (W : 0)
```

---

## Solution

``` javascript
const stockList = (books, categories) => {
  let result = ''
  
  if (books.length === 0 || categories.length === 0) return result
  
  for (let i = 0; i < categories.length; i++) {
    let sum = 0
    
    for (let j = 0; j < books.length; j++) if (books[j][0] === categories[i]) sum += parseInt(books[j].split(' ')[1])
    
    if (result !== '') result += ' - '
    result += '(' + categories[i] + ' : ' + sum + ')'
  }
  return result
}
```