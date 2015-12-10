# SASS

## Nesting

```scss
.foo {
  .bar {
    color: red;
  }
}
```

## Parent Selector

```scss
.foo {
  &.bar {
    color: red;
  }
}
```

```scss
.foo {
  color: green;
  .bar & {
    color: red;
  }
}
```

## Nested Properties

```scss
.foo {
  font: {
    size: 15px;
    weight: bold;
  }
}
```

```scss
.foo {
  font: {
    size: 15px;
    weight: bold;
  }
}
```

## Comments

```scss
/*
  Styling class foo
*/
.foo {
  color: red;
  //color: blue;
}
```

### Compressed output

```scss
/*!
  Styling class foo
*/
.foo {
  color: red;
  //color: blue;
}
```

### Interpolation

```scss
$version: "1.2.3";

/* Version #{$version} */
```

## Variables

```scss
$color: blue;

.foo {
  color: $color;
}
```

### Scope

```scss
$color: blue;

.foo {
  $color: red;
  .bar {
    color: $color;
  }
}

.baz {
  color: $color;
}
```

#### !global

```scss
$color: blue;

.foo {
  $color: red !global;
  .bar {
    color: $color;
  }
}

.baz {
  color: $color;
}
```
