202208222205
Name: **Meeting**
Link: [Codewars](https://www.codewars.com/kata/59df2f8f08c6cec835000012)
Level:  [[6 kyu]]
Tags: [[Fundamentals]]

---

# Meeting

John has invited some friends. His list is:

```
s = "Fred:Corwill;Wilfred:Corwill;Barney:Tornbull;Betty:Tornbull;Bjon:Tornbull;Raphael:Corwill;Alfred:Corwill";
```

Could you make a program that

-   makes this string uppercase
-   gives it sorted in alphabetical order by last name.

When the last names are the same, sort them by first name. Last name and first name of a guest come in the result between parentheses separated by a comma.

So the result of function `meeting(s)` will be:

```
"(CORWILL, ALFRED)(CORWILL, FRED)(CORWILL, RAPHAEL)(CORWILL, WILFRED)(TORNBULL, BARNEY)(TORNBULL, BETTY)(TORNBULL, BJON)"
```

It can happen that in two distinct families with the same family name two people have the same first name too.

---

## Solution1

``` javascript
const meeting = s => {
  const formatPairs= s.toUpperCase().split('').map(e=>e.replace(':',', ')).join(''),
        formatSurname = formatPairs.split(';').map(e=>e.split(', ').reverse().join(', '))
  let arr = []
  formatSurname.map(e=>arr.push(`(${e})`))
  return arr.sort().join('')
}
```


## Solution2

``` javascript
const meeting = s => {
  const formatPairs= s.toUpperCase().split('').map(e=>e.replace(':',', ')).join('')
  console.log(formatPairs)
  const formatSurname = formatPairs.split(';').map(e=>e.split(', ').reverse().join(', '))
  let arr = []
  formatSurname.map(e=>arr.push(`(${e})`))
  return arr.sort().join('')
}
```


## Solution3

``` javascript
const meeting = s => {
  const first = s.toUpperCase().split('').map(e=>e.replace(':',', ')).join('')
  const second = first.split(';').map(e=>e.split(', ').reverse().join(', '))
  let arr = []
  second.map(e=>arr.push(`(${e})`))
  return arr.sort().join('')
}
```