202207261053
Name: **Bumps in the Road**
Link: [Codewars](https://www.codewars.com/kata/57ed30dde7728215300005fa)
Level:  [[7 kyu]]
Tags: [[Fundamentals]] [[Strings]]

---

# Bumps in the Road

Your car is old, it breaks easily. The shock absorbers are gone and you think it can handle about 15 more bumps before it dies totally.

Unfortunately for you, your drive is very bumpy! Given a string showing either flat road (`_`) or bumps (`n`). If you are able to reach home safely by encountering `15 bumps or less`, return `Woohoo!`, otherwise return `Car Dead`

---

## Solution

``` javascript
bump=s=>{
  let counter = 0
  s.split('').filter(e=>e==='n'&&counter++)
  return counter <= 15 ? 'Woohoo!' : 'Car Dead'
}
```