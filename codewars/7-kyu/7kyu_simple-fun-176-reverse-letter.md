202207252122
Name: **Simple Fun #176: Reverse Letter**
Link: [Codewars](https://www.codewars.com/kata/58b8c94b7df3f116eb00005b)
Level:  [[7 kyu]]
Tags: [[Fundamentals]]

---

# Simple Fun #176: Reverse Letter

Given a string `str`, reverse it and omit all non-alphabetic characters.

## Example

For `str = "krishan"`, the output should be `"nahsirk"`.

For `str = "ultr53o?n"`, the output should be `"nortlu"`.

---

## Solution

``` javascript
reverseLetter=s=>s.split('').map(e=>e.match(/[a-z]/)).reverse().join('')
```