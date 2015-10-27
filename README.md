Mint Sass
=========

Convert pixel values to em, rem, and unitless values.

# Functions
```scss
px(value, [scale])  // pixel
em(value, [scale])  // em
rem(value, [scale]) // rem
un(value, [scale])  // unitless
```

# Pixel snapping
When dealing with floating point values the output will snap to the nearest pixel. Due to this it's best to do all your math before sending it to the function.

# Scale
The scale divides the value. This is useful when changing the font size of an element without scaling the rest of the box model if you're using em units. To keep your margins, paddings, and borders visually the same you can pass a scale argument to unit functions which would be the same as the font size. When using a scale pixel snapping is applied afterwards.

# Strings and null
Unit functions will silently output strings and null values if passed and the scale will be ignored if there is one. This is useful when passing variables and removing multiple properties from being output with a null variable.

# Variables
In `_mint-variables.scss` you can modify the `$mint-base` variable if you wish to change the base font size used when converting.
