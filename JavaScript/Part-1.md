# JavaScript Interview Prepration.

## Part-1

## 1. What are the different data types present in javascript?.

**_Note :_** To know the type of a JavaScript variable, we can use the typeof operator.

1. Primitive data types

   - **_String_** : It represents a series of characters and is written with quotes. A string can be represented using a single or a double quote

   **_Example:_**

   ```javascript
   var str = "Vivek Singh Bisht"; //using double quotes
   var str2 = "John Doe"; //using single quotes
   ```

   - **_Number_** : It represents a number and can be written with or without decimals.

   **_Example:_**

   ```javascript
   var x = 3; //without decimal
   var y = 3.6; //with decimal
   ```

   - **_BigInt_** : This data type is used to store numbers which are above the limitation of the Number data type. It can store large integers and is represented by adding “n” to an integer literal.

   **_Example:_**

   ```javascript
   var bigInteger = 234567890123456789012345678901234567890;
   ```

   - **_Boolean_** : It represents a logical entity and can have only two values : true or false. Booleans are generally used for conditional testing.

   **_Example:_**

   ```javascript
   var a = 2;
   var b = 3;
   var c = 2;
   (a == b)(
     // returns false
     a == c
   ); //returns true
   ```

   - **_Undefined:_** : When a variable is declared but not assigned, it has the value of undefined and it’s type is also undefined.

   **_Example:_**

   ```javascript
   var x; // value of x is undefined
   var y = undefined; // we can also set the value of a variable as undefined
   ```

   - **_Null_** : It represents a non-existent or a invalid value.

   **_Example:_**

   ```javascript
   var z = null;
   ```

   - **_Symbol_** : It is a new data type introduced in the ES6 version of javascript. It is used to store an anonymous and unique value.

   **_Example:_**

   ```javascript
   var symbol1 = Symbol("symbol");
   ```

2. Non-primitive types

   - **_Primitive data_** types can store only a single value. To store multiple and complex values, non-primitive data types are used.

   - **_Object_** : Used to store collection of data.

     **_Example:_**

   ```javascript
   // Collection of data in key-value pairs

   var obj1 = {
     x: 43,
     y: "Hello world!",
     z: function () {
       return this.x;
     },
   };

   // Collection of data as an ordered list

   var array1 = [5, "Hello", true, 4.1];
   ```

   **_Note :_** It is important to remember that any data type that is not a primitive data type, is of Object type in javascript.

## Explain Hoisting in javascript.

- Hoisting is the default behaviour of javascript where all the variable and function declarations are moved on top.

![Hoisting](https://d3n0h9tb65y8q.cloudfront.net/public_assets/assets/000/003/406/original/Hoisting.png?1654851517)

- This means that irrespective of where the variables and functions are declared, they are moved on top of the scope. The scope can be both local and global.

**_Example 1_**:

```javascript
hoistedVariable = 3;
console.log(hoistedVariable); // outputs 3 even when the variable is declared after it is initialized
var hoistedVariable;
```

**_Example 2_**:

```javascript
hoistedFunction(); // Outputs " Hello world! " even when the function is declared after calling

function hoistedFunction() {
  console.log(" Hello world! ");
}
```

**_Example 3_**:

```javascript
// Hoisting takes place in the local scope as well
function doSomething() {
  x = 33;
  console.log(x);
  var x;
}
doSomething(); // Outputs 33 since the local variable “x” is hoisted inside the local scope
```

**_Note_** - Variable initializations are not hoisted, only variable declarations are hoisted:

```javascript
var x;
console.log(x); // Outputs "undefined" since the initialization of "x" is not hoisted
x = 23;
```

**_Note_** - To avoid hoisting, you can run javascript in strict mode by using “use strict” on top of the code:

```javascript
"use strict";
x = 23; // Gives an error since 'x' is not declared
var x;
```
