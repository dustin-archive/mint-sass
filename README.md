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
Values can be any data type. If a value is not a number it will be output as-is. If a value is a number or a list of numbers they will be interpreted as pixel dimensions ready to be converted. As well as converting values unit functions will also compress them to shorthand when possible.

## Scale [optional]
If you're using em units, to change the font size of an element and it's contents while keeping the rest of the box model visually the same, you can pass a scale argument equal to the font size.

## Variables
In `_mint-variables.scss` you can modify the `$mint-base` variable to change the base font size used while converting. This value should match the font size set on the body. However, I do not recommend changing this.
