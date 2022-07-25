202207252214
Name: **Round up to the next multiple of 5**
Link: [Codewars](https://www.codewars.com/kata/55d1d6d5955ec6365400006d)
Level:  [[7 kyu]]
Tags: [[Fundamentals]]

---

# Round up to the next multiple of 5

Given an integer as input, can you round it to the next (meaning, "higher") multiple of 5?

**Examples**:

``` javascript
input:    output:
0    ->   0
2    ->   5
3    ->   5
12   ->   15
21   ->   25
30   ->   30
-2   ->   0
-5   ->   -5
etc.
```


---

## Solution 1

``` javascript
roundToNext5=n=>{
    while(n%5 !== 0){
      n++
    }
  return n
}
```

## Solution 2

``` javascript
roundToNext5=n=>Math.ceil(n/5)*5
```

## Solution 3

``` javascript
roundToNext5=n=>{
  while(n%5 !== 0) n++
  return n
}
```

## Solution 4

``` javascript
roundToNext5=n=>n%5!==0?roundToNext5(n+1):n
```