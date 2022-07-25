202207252226
Name: **The Coupon Code**
Link: [Codewars](https://www.codewars.com/kata/539de388a540db7fec000642)
Level:  [[7 kyu]]
Tags: [[Date Time]] [[Strings]] [[Fundamentals]]

---

# The Coupon Code

Write a function called `checkCoupon` which verifies that a coupon code is valid and not expired.

A coupon is no more valid on the day **AFTER** the expiration date. All dates will be passed as strings in this format: `"MONTH DATE, YEAR"`.

**Examples**:

``` javascript
checkCoupon("123", "123", "July 9, 2015", "July 9, 2015")  ===  true
checkCoupon("123", "123", "July 9, 2015", "July 2, 2015")  ===  false
```

---

## Solution

``` javascript
const checkCoupon=
(enteredCode, correctCode, currentDate, expirationDate)=>
enteredCode === correctCode && Date.parse(expirationDate) >= Date.parse(currentDate)
```


```