202208082124
Name: **My Language Skills**
Link: [Codewars](https://www.codewars.com/kata/5b16490986b6d336c900007d)
Level:  [[7 kyu]]
Tags: [[Sorting]] [[Arrays]] [[Algorithms]]

---

# My Language Skills

You are given a dictionary/hash/object containing some languages and your test results in the given languages. Return the list of languages where your test score is at least `60`, in descending order of the results.

Note: the scores will always be unique (so no duplicate values)

**Examples**:

```javascript
{"Java": 10, "Ruby": 80, "Python": 65}    -->  ["Ruby", "Python"]
{"Hindi": 60, "Dutch" : 93, "Greek": 71}  -->  ["Dutch", "Greek", "Hindi"]
{"C++": 50, "ASM": 10, "Haskell": 20}     -->  []
```


---

## Solution

``` javascript
const myLanguages = dicc => Object.keys(dicc).filter(e => dicc[e] >= 60).sort((a, b) => dicc[b] - dicc[a])
```