JavaScript immutability -
Strings are not mutable but arrays are

```{JavaScript}
var myStr = "Jello World";
myStr[0] = "H"; // Fix Me

TypeError: 0 is read-only

// You need to assign it to a new string
```

Nth Letter of string

```{JavaScript}
myStr[N-1]
```

Last Letter
```{JavaScript}
myStr[myStr.length - 1]
```

Nth-to-last letter
```{JavaScript}
myStr[myStr.length - N]
```

`myArray.push()` - push to end of array
`myArray.pop()` - remove last element, set it into some variable

`myArray.shift()` - like pop, but instead of removing last, removes from start.
`myArray.unshift()` - opposite of shift, add element to beginning of array

Variables created without `var` are automatically defined in the global scope. You should always declare variable with `var`.

Double equal, `==`, behavior:

```{JavaScript}
1 == 1 // true
1 == 2 // false
1 == '1' // true
"3" == 3 // true

// Only value, no data type checking
```

Triple equal, `===`, behavior:

```{JavaScript}
3 === 3 // true
3 === '3' // false

// Both value and data type checking
```

Inequality operator, `!=`, behavior

```{JavaScript}
1 != 2 // true
1 != "1" // false
1 != '1' // false
1 != true // false
0 != false // false

// Datatype is converted to equivalent
```

Strict inequality operator, `!==`, behavior

```{JavaScript}
3 !== 3 // false
3 !== '3' // true
4 !== 3 // true

// Datatype not converted
```

Greater that, `>`, operator behavior:

```{JavaScript}
 5 > 3 // true
7 > '3' // true
2 > 3 // false
'1' > 9 // false

// Datatype converted
```

Greater that or equal to, `>=`, behavior:

```{JavaScript}
6 >= 6 // true
7 >= '3' // true
2 >= 3 // false
'7' >= 9 // false

// Datatype converted
```

Similarly, datatype converted for `<`, `<=`

Logical order in chained if-else statements is important

`switch` - don't forget to add `break;` in each `case`. `default` does not require `break;`:

```{JavaScript}
switch (num) {
  case value1:
    statement1;
    break;
  case value2:
    statement2;
    break;
  ...
  default:
    defaultStatement;
}
```

Chained if/else's can be converted to switch/case:

```{JavaScript}
switch (x) {
 case 1:
 case 2:
 case 3:
   do something;
   break;
 case 4:
 ...
}
```

Objects and properties -

```{JavaScript}
# property has a space
var x = myObj["my property"];

# delete a property
delete myObj.objProperty;

# does it have a property?
myObj.hasOwnProperty(checkProp);
```

`Math.random()` generated between 0 (inclusive) and 1 (exclusive)

Regex:
```{JavaScript}
\s+ // one or more whitespace
\S // anything that isn't whitespace. No need of + here
```

Constructor functions:
```{JavaScript}
var Car = function() {
  this.wheels = 4; // this refers to the new object being created
  this.engines = 1;
  this.seats = 5;
};

var myCar = new Car();
// important to use new, so JavaScript all reference to this are made to new object
```

Map does nothing to the original array. You need to store it somewhere.

Reduce -
```{JavaScript}
myArr.reduce(function(previousVal, currentVal) {
...
// previousVal starts with the first element of array (default, unless optional 2nd argument is passed, in which case it becomes that value)
// first argument is callback whose arguments are the accumulator
// previousVal - first value of array
// currentVal - next value of array
// and so on
});
```

Filter - Any array element for which the callback returns true will be kept and elements that return false will be filtered out.
