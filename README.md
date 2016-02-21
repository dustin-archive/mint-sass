Mint Sass
=========

A tiny Sass library for units.

## Functions
```
px(values, [scale])  // pixel
em(values, [scale])  // em
rem(values, [scale]) // rem
un(values, [scale])  // unitless
```

## Values
Values can be any data type. If a value is not a number it will be output as-is. If a value is a number or a list of numbers they will be interpreted as pixel dimensions ready to be converted. As well as converting values unit functions will also compress them to shorthand when possible.*

* The `mint-compress` function works perfect, but I'm looking for a more elegant solution.

## Scale [optional]
If you're using em units, to change the font size of an element and it's contents while keeping the rest of the box model visually the same, you can pass a scale argument equal to the font size.

## Variables
In `_mint-variables.scss` you can modify the `$mint-base` variable to change the base font size used while converting. This value should match the font size set on the body. However, I do not recommend changing this.
