202207252251
Name: **Alphabet war**
Link: [Codewars](https://www.codewars.com/kata/59377c53e66267c8f6000027)
Level:  [[7 kyu]]
Tags: [[Fundamentals]] [[Strings]]

---

# Alphabet war

Write a function that accepts `fight` string consists of only small letters and return who wins the fight. When the left side wins return `Left side wins!`, when the right side wins return `Right side wins!`, in other case return `Let's fight again!`.

The left side letters and their power:

```
 w - 4
 p - 3
 b - 2
 s - 1
```

The right side letters and their power:

```
 m - 4
 q - 3
 d - 2
 z - 1
```

**Example**:

```javascript
alphabetWar("z");        //=> Right side wins!
alphabetWar("zdqmwpbs"); //=> Let's fight again!
alphabetWar("zzzzs");    //=> Right side wins!
alphabetWar("wwwwwwz");  //=> Left side wins!
```

---

## Solution 1

``` javascript
const alphabetWar=s=>{
  let splitted = s.split(''), 
      leftSum = 0, 
      rightSum = 0
  
  splitted.filter(e=>{
      if (e === 'w') leftSum += 4
      if (e === 'p') leftSum += 3
      if (e === 'b') leftSum += 2
      if (e === 's') leftSum += 1
    
      if (e === 'm') rightSum += 4
      if (e === 'q') rightSum += 3
      if (e === 'd') rightSum += 2
      if (e === 'z') rightSum += 1
  })
  

  return leftSum > rightSum 
    ? "Left side wins!" 
    : leftSum < rightSum 
    ? "Right side wins!" 
    : "Let's fight again!"
}
```

## Solution 2

``` javascript
const alphabetWar=s=>{
  let splitted = s.split(''), 
      leftSum = 0, 
      rightSum = 0
  
  let left = splitted.filter(e=>{
      if (e === 'w') leftSum += 4
      if (e === 'p') leftSum += 3
      if (e === 'b') leftSum += 2
      if (e === 's') leftSum += 1
  })
  
  let right = splitted.filter(e=>{
      if (e === 'm') rightSum += 4
      if (e === 'q') rightSum += 3
      if (e === 'd') rightSum += 2
      if (e === 'z') rightSum += 1
  })
  
  return leftSum > rightSum 
    ? "Left side wins!" 
    : leftSum < rightSum 
    ? "Right side wins!" 
    : "Let's fight again!"
}
```