## Getting Started With JavaScript - Part 1


#  Introduction 

JavaScript is one of the most potent and famous languages to learn in 2022. It is one of the most demanding languages in many industries and having it as a language you can fluently code in is a huge advantage on its own. Personally, I am thankful and grateful to all the developers who produce tech content and make it available for free so that anyone can code irrespective of their barriers, for that reason I wanted to give back to the community with this series of blogs with which if you follow you can learn JavaScript too. In this blog, we will look at the basics of JavaScript or in other words the bare minimum you need to jump straight to the cool stuff. SO LET'S GET ON with it...


![lets-go-dwight-schrute.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1659468076921/Ilg7oo07S.gif align="left")



# First things first

JavaScript is a programming language so if this is your first time learning a programming language, here are some basics stuff you need to know before starting out and if you know how to code then you can skip these parts:

## Variables:

Variables are containers for storing data and are mainly used to store data values. In JavaScript, variables are declared using:

- var
- let
- const
- nothing at all ;0

Now, using var is not recommended as it is used in older versions of JavaScript(before ES6) but currently Developers and companies are mainly going forward with the ES6 version of JavaScript. But still, you should learn every fundamental to be really updated.

Using var: 


```
var x = 5
var y = 6
var z = x + y // 5 + 6 = 11
``` 
Above x,y and z are variables, declared with the var keyword

Using let:

```
let x = 5
let y = 6
let z = x + y // 5 + 6 = 11
``` 
Above x,y and z are variables, declared with the let keyword

Using const:

```
const cost1 = 5
const cost2 = 6
let sum = cost1 + cost2 // 5 + 6 = 11
``` 
The two variables cost1 and cost2 are declared with const keyword. These are constant values and cannot be changed later in the code. The variable sum is declared with the let keyword. This is a value that can be changed

Using NOTHING(not the phone 😅):

This is NOT RECOMMENDED

```
x = 3;
y = 4;
z = x + y // 3 + 4 = 7
```
Here x,y and z are undeclared variables 

### Variable Scope

The scope of a variable is the region of your code in which it is defined. JS variables have only two scopes.

- Global Variables: A global variable has a global scope which means it can be defined anywhere in your JavaScript code. 

- Local Variables: A local variable will be visible only within a function where it is defined. Function parameters are always local to that function

### Variable Names

While naming a variable, you should consider these rules:
- You should not use any of the JavaScript reversed keywords as a variable name.

- JavaScript variable names should not start with a numeral (0-9). They must begin with a letter or an underscore character. For example, 123rock is an invalid variable name but _123rock is a valid one.

- JavaScript variable names are case-sensitive. For example, Name and name are two different variables.


![200.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1659468003435/Jx4-FqW0u.gif align="left")

## Operators

JavaScript includes operators the same as other languages. An operator performs some operation on single or multiple operands(data value) and produces a result. For example, in 1 + 2, the + sign is an operator and 1 is the left side operand and 1 is the left side operand and 2 is the right side operand.

**JavaScript includes the following categories of operators: **

- Arithmetic Operators:

JavaScript Arithmetic Operators are used to perform arithmetic on numbers:
![JavaScript-Arithmatic-Operators.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659469375325/tPwz6X3dY.png align="left")

```
let x = 5;
let y = 2;
let z1 = x + y;
let z2 = x * y;
let z3 = x / y;
let z4 = x % y;
```
- Conditional Operators:

JavaScript provides conditional operators that compare two operands and return a boolean value true or false.


![js-boolean-operator-table.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659557102231/DfzFrpDp_.png align="left")

```
let a = 5, b = 10, c = "5"
var x = a;

a == c // return true
a === c // returns false
a == x // returns true
a != b // returns true
a > b // returns true
a < b // returns true
a >= b // returns false
a <= b // returns false
```
- Logical Operators

The logical operators are used to combine two or more conditions. JavaScript provides the following logical operators.


![JavaScript-Logical-Operator.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659557442246/iwp-dFQWt.png align="left")

```
const a = true, b = false;
const c = 4;

// logical AND
console.log(a && a); // true
console.log(a && b);  // false

console.log((c > 2) && (c < 2)); // false

// logical OR
console.log(a || b); // true
console.log(b || b); // false
console.log((c>2) || (c<2)); // true

// logical NOT
console.log(!a); // false
console.log(!b); // true
```
- Assignment Operators:

JavaScript provides the assignment to assign values to variables with fewer keystrokes

![KLKaBkN.jpeg](https://cdn.hashnode.com/res/hashnode/image/upload/v1659558610624/IHbJEx6b0.jpeg align="left")

```
let x = 10;
x += 5;
x -= 5;
x *= 5;
x /= 5;
x %= 5;
```
- Ternary Operators:

JavaScript provides a special operator called ternary operator:? that assigns the value to a variable based on some condition. It is a short form of the if-else condition

```
condition ? doThisIfTrue : doThisIfFalse

1 > 2 ? console.log(true) : console.log(false)
// returns false
```

## Data Types

There are different types of data that can be used in the JavaScript program. 

There are two types of Datatype: 

### Primitive Datatype:
1. String 
2. Number
3. BigInt
4. Boolean
5. Undefined 
6. Null
7. Symbol

### Non-primitive Datatype:
1. Object

## Functions in JavaScript:

A JavaScript function is a block of code designed to perform a particular task. A JavaScript function is executed when "something" invokes it(calls it) or triggers it.

### Syntax:
A JavaScript function is defined with the function keyword, followed by paratheses ().

Function names can obtain letters, digits, underscores, and dollar signs(same rules as variables).

The parentheses may include parameter names separated by commas.

```
function name(parameter 1,parameter 2) {
// code to be executed 
}
```
### Why use functions?

So that you can write code once and use it many times, improves Code reusability.

Invocation:

The code inside the function will execute when something invokes the function:
- When an event occurs 
- When it is invoked(called) from JavaScript code
- Automatically invoked or self invoked 

### Function Return:

When JavaScript reaches a return statement the function will stop executing. If the function was invoked from a statement, JavaScript will 'return' to execute the code after the invoking statement.

Functions often compute a return value. The return value is 'returned' back to the 'caller'.

Now comes some fundamental things like loops and conditional statements which I will publish some vlogs separately. Stay Tuned ;)

Now let's do something OOPsie


![giphy.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1661370664714/0L4je7abE.gif align="left")

# Object Oriented Programming(OOPs) 
 


## Objects:

We have already learnt that JavaScript variables are containers for data values in our data type section. 

Now, what are objects?? Let's talk in code

```
// To make an object literal:
const dog = {
    name: "Rusty",
    breed: "unknown",
    isAlive: false,
    age: 7
}
// All keys will be turned into strings!

// To retrieve a value:
dog.age; //7
dog["age"]; //7

//updating values
dog.breed = "mutt";
dog["age"] = 8;
```
Here the dog is an object that stores values such as numbers and strings. 

### Accessing Object Properties

We can access object properties in two ways.

1. objectName.propertyName

2. objectName.["propertyName"]

### Object Methods:

Objects can also have methods. Methods are actions that can be performed on objects.

A method is a function stored as a property. 

```
const student = {
firstName = 'subham'
lastName = 'ghosh'
class = 10
myFun: function() { console.log("Hello there") }
}
student.myFun();

```
## Classes:

The class keyword is used to create a class. We should always add a method called constructor() in the class.

Example:

```
class Car {
  constructor(name, year) {
    this.name = name;
    this.year = year;
  }
}
```

### Constructor Method:

The constructor method is a special method which is used to initialise object properties. It should have the correct name "constructor". If we don't define a constructor method, JavaScript will add an empty constructor method. 

```
class ClassName {
  constructor() { ... }
  method_1() { ... }
  method_2() { ... }
  method_3() { ... }
}
```

![that-was-fun-fun.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1661370194846/fOFi8MsaT.gif align="left")

So here we are done with the Basics of JavaScript, now comes the fun part which will be continued in part 2 of this blog, so SUBSCRIBE to my newsletter to get personalised emails when it gets out!! See you next time and if you find my content helpful, consider following me on [Twitter](https://twitter.com/subhamstwt) and Hashnode itself. BYEEEEE!


