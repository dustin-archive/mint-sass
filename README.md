Mint Sass
=========

A Sass library for units.

## Functions
```scss
px(values, [scale])  // pixel
em(values, [scale])  // em
rem(values, [scale]) // rem
un(values, [scale])  // unitless
```

## Values
Unit functions can accept any value. If a value is not a number it be output without being scaled or converted. This is useful when using variables and retaining the ability to prevent the properties from being output with a null value.

## Multiple values
If you want to convert multiple values at a time, rather than calling the function every time for each value, you can pass a list of values to convert. As well as converting the values, unit functions will also compress like-values when possible. For example, `1 1 1 1` will become `1` and `1 2 1 2` will become `1 2`.

## Pixel snapping
When dealing with floating point values the output will floor to the lowest physical pixel which is calculated from the base font size. Snapping to the lowest pixel can reduce file size by reducing the length of the floating point or remove it entirely. Because of this it's best to do all your math before using the functions.

## Scale
Scale divides the values. If you're using em units, this is useful when changing the font size of an element without wanting to scale the rest of the box model. To keep your margins, paddings, and borders visually the same you can pass a scale argument the same as the font size.

## Variables
In `_mint-variables.scss` you can modify the `$mint-base` variable if you wish to change the base font size used when converting, but I personally do not recommend doing this.
