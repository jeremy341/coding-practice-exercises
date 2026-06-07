# Basic HTML Review

## Role of HTML

HTML represents the content and structure of the web page.

## HTML Elements

Elements are the building blocks for an HTML document. They represent headings, paragraphs, links, images and more. Most HTML elements consist of an opening tag (`<elementName>`) and a closing tag (`</elementName>`).

Here is the basic syntax:

```html
<elementName>Content goes here</elementName>
```

## Void Elements

Void elements cannot have any content and only have a start tag. Examples include `img` and `meta` elements.

```html
<img>
<meta>
```

It is common to see some codebases that include a forward slash `/` inside the void element. Both of these are acceptable:

```html
<img>
<img/>
```

## Attributes

An attribute is a value placed inside the opening tag of an HTML element. Attributes provide additional information about the element or specify how the element should behave. Here is the basic syntax for an attribute:

```html
<element attribute="value"></element>
```

A boolean attribute is an attribute that can either be present or absent in an HTML tag. If present, the value is true otherwise it is false. Examples of boolean attributes include `disabled`, `readonly`, and `required`.

## Comments

Comments are used in programming to leave notes for yourself and other developers in your code. Here is the syntax for a comment in HTML:

```html
<!-- This is an HTML comment -->
```

## Common HTML Elements

### Heading Elements

There are six heading elements in HTML. The `h1` through `h6` heading elements are used to signify the importance of content below them. The lower the number, the higher the importance, so `h2` elements have less importance than `h1` elements.

```html
<h1>most important heading element</h1>
<h2>second most important heading element</h2>
<h3>third most important heading element</h3>
<h4>fourth most important heading element</h4>
<h5>fifth most important heading element</h5>
<h6>least important heading element</h6>
```
