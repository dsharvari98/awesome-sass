# awesome-sass
Notes regarding Sass framework
To Learn about Sass first of all you should have knowledge of 
1. HTML
2. CSS

# SASS
* Sass stands for Syntactically Awesome Stylesheet
* Sass is an extension to CSS
* Sass is a CSS pre-processor
* Sass is completely compatible with all versions of CSS
* Sass reduces repetition of CSS and therefore saves time
* Sass is free to download and use
* Two syntaxes available:
1. SCSS (Sassy CSS): This is an extension of the CSS syntax, meaning that every valid CSS file is also a valid SCSS file with the same meaning
2. Sass syntax (also known as indented syntax): Older syntax that uses indentation instead of brackets to indicate nesting and uses newlines instead of semicolons to separate different properties

## Some Features
examples are takes from [Sass website](https://sass-lang.com)

## Variables
### Example SCSS:
```
$font-stack: Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}
```
### Resulting CSS:
```
body {
  font: 100% Helvetica, sans-serif;
  color: #333;
}
```
## Nesting
 Allows you to nest your CSS selectors in a way that's similar to how your HTML elements are nested
 ```
nav ul {
  margin: 0;
  padding: 0;
  list-style: none;
}

nav li {
  display: inline-block;
}

nav a {
  display: block;
  padding: 6px 12px;
  text-decoration: none;
}
```
Example SCSS:
```
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li { display: inline-block; }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
```
Resulting CSS:
```
nav ul {
  margin: 0;
  padding: 0;
  list-style: none;
}

nav li {
  display: inline-block;
}

nav a {
  display: block;
  padding: 6px 12px;
  text-decoration: none;
}
```
## Mixins
Mixin = a group of CSS declarations that you can reuse together, potentially parameterized

Helps to keep your SCSS DRY

Typical use case: vendor prefixes
Example SCSS:
```
@mixin transform($property) {
  -webkit-transform: $property;
  -ms-transform: $property;
  transform: $property;
}

.box { @include transform(rotate(30deg)); }
````
Resulting CSS:
```
.box {
  -webkit-transform: rotate(30deg);
  -ms-transform: rotate(30deg);
  transform: rotate(30deg);
}
```
## Inheritance
Inheritance lets you share properties between selectors

Helps to keep both your SCSS and CSS DRY

Example SCSS:
```
%message-shared {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

.message {
  @extend %message-shared;
}

.success {
  @extend %message-shared;
  border-color: green;
}

.error {
  @extend %message-shared;
  border-color: red;
}

.warning {
  @extend %message-shared;
  border-color: yellow;
}
```
Resulting CSS:
```
.message, .success, .error, .warning {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

.success {
  border-color: green;
}

.error {
  border-color: red;
}

.warning {
  border-color: yellow;
}
```
## Resources
⋅⋅* [CSS - The Complete Guide 2020 (incl. Flexbox, Grid & Sass) ](https://www.udemy.com/course/css-the-complete-guide-incl-flexbox-grid-sass/)
..* [Sass](https://sass-lang.com)
..* [What's the difference between Sass and scss](https://stackoverflow.com/questions/5654447/whats-the-difference-between-scss-and-sass)






















