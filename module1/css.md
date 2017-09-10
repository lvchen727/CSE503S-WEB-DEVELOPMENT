# CSS (Cascading Style Sheets)

## defines appearance of page

## basic structure
```CSS
header{
  color: blue;
  font-family: Verdana, sans-serif;
}
```

## CSS is composed of rules(a selector and >=1 declarations)

## Selectors:
### 1. [selecting by the tag name](https://www.w3.org/TR/CSS/#selectors)
* foo : tag name foo
* .foo: class name foo
* #foo: ID foo
* [foo="bar"] :  attribute foo whose value is bar
* foo bar: an element matching bar also a descendant of an element matching foo
* foo > bar: matching bar that is a child of an element matching foo
* foo + bar: matching bar that is the next sibling of an element matching foo
### 2. [selecting by pseudo-classes](https://www.w3.org/TR/CSS/#selectors)
```CSS
a:visited {
	color: #99FF99; /* this example uses a hexadecimal RGB definition for the color, which allows you to
		mix over 16 million colors */
}
```

## Properties:
* commom properties: color, font-family, text-decoration, background-image, background-color, border, border-radius, float, cursor, font, list-style-type, text-align, display
* some properties ask for units: px, em, rem, pt, %

## All elemnts fall into one of two categories
1. Inline(span, strong...)
2. [Block(p, div, section...)](https://www.w3.org/TR/css3-box/)
```CSS
div.box {
	width: 500px;
	margin: 0 auto; /* when two "arguments" are passed to margin or padding, the first defines top
		and bottom margin/padding and the second defines left and right margin/padding */
	padding: 25px; /* when only one "argument" is passed to margin or padding, it defines the
		margin/padding on all four sides */
	border: 1px solid black; /* the 1px defines the border-width; the solid defines the border-style;
		the black defines the border-color */
}
```


## How to include CSS (3 WAYS)
1. load external stylesheets
```CSS
<link rel="stylesheet" type="text/css" href="path/to/stylesheet.css" />
```
2. embed stylesheets in document
```html
<style type="text/css">
styles {
	go: here;
}
</style>
```

3. inline style using style attribute
```css
p.notice {
	color: blue;
}
```
```html
<p class="notice">Well done using classes instead of inline styles!</p>
<p style="color:red;">You'd better think twice about using inline styles.</p>
```
