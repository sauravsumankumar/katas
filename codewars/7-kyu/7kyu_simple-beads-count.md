202207261058
Name: **Simple beads count**
Link: [Codewars](https://www.codewars.com/kata/58712dfa5c538b6fc7000569)
Level:  [[7 kyu]]
Tags: [[Fundamentals]]

---

# Simple beads count

Two red beads are placed between every two blue beads. There are N blue beads. After looking at the arrangement below work out the number of red beads.

``` javascript
@ @@ @ @@ @ @@ @ @@ @ @@ @
```

Implement `count_red_beads(n)` so that it returns the number of red beads.  
If there are less than 2 blue beads return 0.

---

## Solution

``` javascript
countRedBeads=n=>n<=2?0:(n-1)*2
```