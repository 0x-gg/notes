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

