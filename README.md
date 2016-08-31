mint-sass
===

> Sweet unit library

<br>

| Legend |
| :------------- |
| [Unit Functions](#unit-functions) |
| [`$mint-base`](#mint-base) |
| [`mint()`](#mint-fn) |
| [`mint-compress()`](#mint-compress) |
| [`mint-strip()`](#mint-strip) |

<br>

### Unit Functions
Shorthands for units based off [`mint()`](#mint-fn) that assume a base equal to [`$mint-base`](#mint-base)

+ `px(values, unit, [scale])`
+ `em(values, unit, [scale])`
+ `rem(values, unit, [scale])`
+ `un(values, unit, [scale])`

<br>

### <a name='mint-base'>`$mint-base`</a>
Base font size (`16` by default)

<br>

### <a name='mint-fn'>`mint(values, base, scale, unit)`</a>
Converts and scales values

+ `values` (`List`) List of values for mint to process
+ `base` (`Number`) Base font size
+ `scale` (`Number`) Relative font size or scale
+ `unit` (`String`) Unit for each number

```
// in
.foo {
  margin: mint(8 4 8 4, 16, 16, em);
}

// out
.foo {
  margin: 0.5em 0.25em;
}
```

<br>

### <a name='mint-compress'>`mint-compress(values)`</a>
Compress values to their shortest form

```
// in
.foo {
  margin: mint-compress(8px 4px 8px 4px);
}

// out
.foo {
  margin: 8px 4px;
}
```

<br>

### <a name='mint-strip'>`mint-strip(value)`</a>
Strip a unit from a number

```
// in
.foo {
  line-height: mint-strip(16px);
}

// out
.foo {
  line-height: 16;
}
```
