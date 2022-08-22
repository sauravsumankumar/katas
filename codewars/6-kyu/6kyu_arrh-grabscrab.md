202208222158
Name: **Arrh, grabscrab!**
Link: [Codewars](https://www.codewars.com/kata/52b305bec65ea40fe90007a7)
Level:  [[6 kyu]]
Tags: [[Strings]] [[Algorithms]]

---

# Arrh, grabscrab!

Pirates have notorious difficulty with enunciating. They tend to blur all the letters together and scream at people.

At long last, we need a way to unscramble what these pirates are saying.

Write a function that will accept a jumble of letters as well as a dictionary, and output a list of words that the pirate might have meant.

**Example**:

```
grabscrab( "ortsp", ["sport", "parrot", "ports", "matey"] )
```

Should return `["sport", "ports"]`.

Return matches in the same order as in the dictionary. Return an empty array if there are no matches.


---

## Solution1

``` javascript
function grabscrab(anagram, dictionary) {
  const word = anagram.split('').sort().join('')
  
  let results = []
  
  dictionary.filter(e=> e.split('').sort().join('') === word && results.push(e),0)
  
  return results
}
```

## Solution2

``` javascript
const grabscrab=(anagram, dictionary)=>{
  const word = anagram.split('').sort().join('')
  return dictionary.filter(e=>e.split('').sort().join('')===word,0)
}
```

## Solution3

``` javascript
const grabscrab=(anagram, dictionary)=> dictionary.filter(e=> e.split('').sort().join('') === anagram.split('').sort().join(''),0)
```