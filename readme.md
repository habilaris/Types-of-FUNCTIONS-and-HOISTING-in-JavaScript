# FUNCTIONS, Types of Function Expressions, HOISTING and "USE STRICT" KEYWORD


---
### "USE STRICT" KEYWORD
```
"use strict" 
```
It is used so JS does not implicitly create a GLOBAL VARIABLE if a developer forgets to use let/var/const for creating a variable!

OTHERWISE: Suppose, In a code,
```
function add(num) {
    sum1 = num1 + num2; 
}
```
- IMPORTANT: Here "sum1" will create a GLOBAL VARIABLE, that will work even outside the function scope, Which later-on can create conflicts!
- And YES! It is possible to create a variable in JS without let/var/const, but only in "NON-STRICT" mode.

---

## HOISTING

DEF: Hoisting is the theoretical concept of bringing all the HOISTED VARIABLES, FUNCTIONS and CLASSES at the top of the script/code to compile it first.
Keypoiny: All the OLD METHODS of Variable(var), Function(Normal Function Declaration) and Class Declarations in JavaScript are Hoisted.

---

### 1. NORMAL Function (Hoisted)

```
sum_1(5, 5);    // Benefit of a hosted function that you can use the function even before the function declaration

function sum_1(num1, num2) {     // Only "Function Declaration" for the hoisted one!
    let sum1 = num1 + num2;
    console.log("1. NORMAL Function:", sum1);
};
```

## 1.  Function EXPRESSIONS (Non-Hoisted): In which a function is put in a variable except IIFE.
1.  ### ANONYMOUS Function Expression.
2.  ### NAMED Function Expression.
3.  ### ARROW Function Expression.
4.  ### Immediatelly Invoked Function Expression.
---

### A. ANONYMOUS Function Expression

```
let sum2 = function (num1, num2) {
    let sum1 = num1 + num2;
    console.log("a. ANONYMOUS Function Expression:", sum1);
};
```



### B. NAMED Function Expression (When a normal function becomes function expression!)

```
let sum3 = function add(num1, num2) {
    let sum1 = num1 + num2;
    console.log("b. NAMED Function Expression:", sum1);
};

sum3(5, 8);
```



### C. ARROW Function Expression (Non-Hoisted)

```
let sum4 = (num1, num2) => {
    let sum1 = num1 + num2;
    console.log("c. ARROW Function Expression:", sum1);
}
sum4(6,8);
```
There is no stand-alone concept of just "Arrow Function", it's always "Arrow Function Expression"!



### D. Immediately Invoked Function Expression (IIFE)

```
( function (num1, num2) {
    let sum1 = num1 + num2;
    console.log("d. Immediately Invoked Function Expression (IIFE):", sum1);
} (7,8) );
```


