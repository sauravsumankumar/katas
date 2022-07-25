202207252255
Name: **Boiled Eggs**
Link: [Codewars](https://www.codewars.com/kata/52b5247074ea613a09000164)
Level:  [[7 kyu]]
Tags: [[Mathematics]] [[Algorithms]]

---

# Boiled Eggs

Implement a function, which takes a non-negative integer, representing the number of eggs to boil. It must return the time in minutes (integer), which it takes to have all the eggs boiled.

1.   You can put at most 8 eggs into the pot at once
2.   It takes 5 minutes to boil an egg
3.   We assume, that the water is boiling all the time (no time to heat up)
4.  For simplicity we also don't consider the time it takes to put eggs into the pot or get them out of it


**Example**:

``` javascript
0 --> 0
5 --> 5
10 --> 10
```

---

## Solution

``` javascript
cookingTime=(e)=>Math.ceil(e/8)*5
```