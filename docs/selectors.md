# Selectors

## Element Selectors

### Universal Selector

Matches every element.

```css
* {
  color: blue;
}
```

### Type Selector

Matches an element of a given type.

```css
p {
  color: blue;
}
```

### Descendant Selector

An element below another element.

```css
li p {
  color: blue;
}
```

### Child Selector

A child of another element.

```css
li > p {
  color: blue;
}
```

### Adjacent Sibling Selector

A sibling right after another element.

```css
p + p {
  color: blue;
}
```

### General Sibling Selector

A sibling after another element.

```css
p ~ p {
  color: blue;
}
```

### Class Selector

An element with a given *class*.

```css
p.foo {
  color: blue;
}
```

```css
p.foo.bar {
  color: blue;
}
```

```css
.baz {
  color: blue;
}
```

### ID Selector

An element with a given *id*.

```css
p#foo {
  color: blue;
}
```

```css
#bar {
  color: blue;
}
```

## Attribute Selectors

### Simple Attribute Selector

An element with a given attribute.

```css
p[class] {
  background-color: green;
}
```

### Exact Attribute Value Selector

An element with a given attribute with a given value.

```css
p[class="foo"] {
  background-color: green;
}
```

### Partial Attribute Value Selector

Attribute value in a space separated list.

```css
p[class~="foo"] {
  background-color: green;
}
```

### Beginning Substring Attribute Value Selector

Attribute value starting with.

```css
a[href^="http:"] {
  background-color: green;
}
```

### Ending Substring Attribute Value Selector

Attribute value ending with.

```css
a[href$=".pdf"] {
  background-color: green;
}
```

### Arbitrary Substring Attribute Value Selector

Attribute value containing.

```css
a[href*="/foo/"] {
  background-color: green;
}
```

### Language Attribute Selector

First *item* in a hyphen separated list.

```css
html[lang|="en"] {
  background-color: green;
}
```

## Structural Pseudo-Class Selectors

### :empty

An empty element.

```css
p:empty {
  background-color: red;
}
```

```css
*:empty {
  background-color: red;
}
```

### :first-child

An element that is the first child of it's parent element.

```css
p:first-child {
  background-color: red;
}
```

```css
*:first-child {
  background-color: red;
}
```

### :last-child

An element that is the last child of it's parent element.

```css
p:last-child {
  background-color: red;
}
```

```css
*:last-child {
  background-color: red;
}
```

### :first-of-type

An element that is the first child of a given type of it's parent element.

```css
p:first-of-type {
  background-color: red;
}
```

```css
*:first-of-type {
  background-color: red;
}
```

### :last-of-type

An element that is the first child of a given type of it's parent element.

```css
p:last-of-type {
  background-color: red;
}
```

```css
*:last-of-type {
  background-color: red;
}
```

### :nth-child

An element that is the n'_th_ child of it's parent element.

Children are one-based and *n* is zero-based.

```css
p:nth-child(3n) {
  background-color: red;
}
```

```css
p:nth-child(3n+1) {
  background-color: red;
}
```

```css
p:nth-child(3n-1) {
  background-color: red;
}
```

```css
*:nth-child(3n) {
  background-color: red;
}
```

### :nth-last-child

An element that is the n'_th_ last child of it's parent element.

Children are one-based and *n* is zero-based.

```css
p:nth-last-child(3n) {
  background-color: red;
}
```

```css
p:nth-last-child(3n+1) {
  background-color: red;
}
```

```css
p:nth-last-child(3n-1) {
  background-color: red;
}
```

```css
*:nth-last-child(3n) {
  background-color: red;
}
```

### :nth-of-type

An element that is the n'_th_ child of a given type of it's parent element.

Elements of type are one-based and *n* is zero-based.

```css
p:nth-of-type(3n) {
  background-color: red;
}
```

```css
p:nth-of-type(3n+1) {
  background-color: red;
}
```

```css
p:nth-of-type(3n-1) {
  background-color: red;
}
```

```css
*:nth-of-type(3n) {
  background-color: red;
}
```

### :nth-last-of-type

An element that is the n'_th_ last child of a given type of it's parent element.

Elements of type are one-based and *n* is zero-based.

```css
p:nth-last-of-type(3n) {
  background-color: red;
}
```

```css
p:nth-last-of-type(3n+1) {
  background-color: red;
}
```

```css
p:nth-last-of-type(3n-1) {
  background-color: red;
}
```

```css
*:nth-last-of-type(3n) {
  background-color: red;
}
```

### :only-child

An element that is the only child of it's parent element.

```css
p:only-child {
  background-color: red;
}
```

```css
*:only-child {
  background-color: red;
}
```

### :only-of-type

An element that is the only child of a given type of it's parent element.

```css
p:only-of-type {
  background-color: red;
}
```

```css
*:only-of-type {
  background-color: red;
}
```

### :lang

Any element with associated language-encoding information.

```css
html:lang(en) {
  background-color: red;
}
```

```css
*:lang(de) {
  background-color: red;
}
```

### :root

The *root* element.

```css
:root {
  color: red;
}
```

## :not

Matches every element that is not described by a simple selector.

```css
*:not(p) {
  color: red;
}
```

```css
p:not(:first-child) {
  color: red;
}
```

```css
a:not([href]) {
  color: red;
}
```

```css
*:first-child:not(p) {
  color: red;
}
```

```css
*:not(div):not(p) {
  color: red;
}
```

## Interaction Pseudo-Class Selectors

### :active

An active element - ex. while an anchor is being clicked.

```css
a:active {
  color: green;
}
```

```css
*:active {
  color: green;
}
```

### :checked

A checked element - ex. a checkbox that is checked.

```css
input:checked {
  box-shadow: red 0 0 5px;
}
```

```css
*:checked {
  box-shadow: red 0 0 5px;
}
```

### :disabled

A disabled element - ex. a disabled input element.

```html
<input type="text" disabled>
```

```css
input:disabled {
  border: 2px solid lightgray;
}
```

```css
*:disabled {
  border: 2px solid lightgray;
}
```

### :enabled

A enabled element - ex. a enabled input element.

```html
<input type="text">
```

```css
input:enabled {
  border: 2px solid lightgreen;
}
```

```css
*:enabled {
  border: 2px solid lightgreen;
}
```

### :focus

An element with focus - ex. a focused anchor.

```css
a:focus {
  outline: 2px dotted orange;
}
```

```css
input:focus {
  background-color: orange;
}
```

```css
*:focus {
  color: orange;
}
```

#### Note

IE only supports `:focus` for *anchors*

### :hover

An element that is hovered.

```css
a:hover {
  background-color: lightyellow;
}
```

### :visited

A hyperlink to a resource that has already been visited -
ex. an anchor to a page that has been visited.

```css
a:visited {
  color: gray;
}
```

```css
*:visited {
  color: gray;
}
```

### :link

A hyperlink to a resource that has *not* yet been visited -
ex. an anchor to a page that has not been visited.

```css
a:link {
  color: green;
}
```

```css
*:link {
  color: green;
}
```

### :target

An element that has an *id* that matches the *hash* part of the URL.

```css
div:target {
  background-color: lightgreen;
}
```

```css
*:target {
  background-color: lightgreen;
}
```

## Pseudo-Element Selectors

### ::first-line

The first line of a elements text.

```css
p::first-line {
  font-variant: small-caps;
}
```

### ::first-letter

The first letter of a elements text.

```css
p::first-letter {
  font-size: 2em;
}
```

### ::before

A pseudo-element containing generated content placed before the content in the element.

```css
span::before {
  content: '$';
}
```

### ::after

A pseudo-element containing generated content placed after the content in the element.

```css
span::after {
  content: '™';
}
```
