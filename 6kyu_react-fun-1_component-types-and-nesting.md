202209111832
Name: **React Fun #1: Component types and nesting**
Link: [Codewars](https://www.codewars.com/kata/595b9b85ff19c2bd35000013/)
Level:  [[6 kyu]]
Tags: [[React]] [[Fundamentals]]

---

# React Fun #1: Component types and nesting

## Task

1.  Create three components. Following the provided rules
2.  One component should be named `Hello` and it should return `'Hello'` wrapped inside of `h1`.
3.  The second component should be named `World` and it should return `'World!'` wrapped inside of `h2`.
4.  Create a parent component using `class` syntax called `Greet` and nest previous two components inside of it, wrapping them with a `div`.

If you are stuck, refer to examples provided here. Good luck! :)

There might be some problem with spaces (like you've inserted some extra spaces that make tests fail). It's easy to solve them by reading the error message. So it's never a problem. :)

---

## Solution 1

``` javascript
const React = require('react');

class Hello extends React.Component {
  render() {
    return <h1>Hello</h1>;
  }
}
class World extends React.Component {
  render() {
    return <h2>World!</h2>;
  }
}
class Greet extends React.Component {
  render() {
    return <div><Hello /><World /></div>
  }
}
```
## Solution 2

``` js
const React = require('react');
const Hello = () => (<h1>Hello</h1>)
const World = () => (<h2>World!</h2>)
class Greet extends React.Component {
    render() {
        return <div><Hello /><World /></div>
    }
}
```