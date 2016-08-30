Mint
===

> Sweet unit library

## Functions
```
px($values, $scale: null)  // pixel
em($values, $scale: null)  // em
rem($values, $scale: null) // rem
un($values, $scale: null)  // unitless
```

## Values
+ Values can be any data type
+ When passing numbers, units can only be `px` or unitless

If a value is not a number it will be output as-is. If a value or list of values contain a `px` or unitless number they will be interpreted as pixel dimensions and converted, otherwise an error message will be thrown. As well as converting values unit functions will also compress them to shorthand when possible.

## Scale
+ Optional

If you're using em units, to change the font size of an element and it's contents while keeping the rest of the box model visually the same, you can pass a scale argument equal to the font size.

## Variables
You can modify the `$mint-base` variable to change the base font size used while converting. This value should match the font size set on the body. However, I do not recommend changing this.
