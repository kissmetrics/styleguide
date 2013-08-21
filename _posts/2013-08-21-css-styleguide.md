---
layout: styleguide
title: "CSS Styleguide"
---

## Table of Contents
* [Coding-style](#coding-style)
* [SCSS](#scss)

## <a id='coding-style'></a>Coding-style
* Use soft-tabs with a two space indent.
* Keep lines fewer than 80 characters.
* Never leave trailing whitespace.
* Avoid IDs in CSS.
* Use US English for all naming. Name classes and variables in the locale of the language you are working with.

* Put spaces after `:` in property declarations.

```
# Bad
color:red;

# Good
color: red;
```


* Alphabetize your properties.

```
h1 {
  color: red;
  font-size: 2em;
  font-weight: 500;
  line-height: 1.5;
  margin: 1em 0;
}
```

* Avoid over-qualified selectors.

```
# Bad
div.promo {}

# Good
.promo {}
```


```
# Bad
ul.nav li a {}

# Good
.nav a {}
```

## <a id='scss'></a>SCSS
* Any `$variable` or `@mixin` that is used in more than one file should be put in `globals/`. Others should be put at the top of the file where they're used.
* As a rule of thumb, don't nest further than 3 levels deep. If you find yourself going further, think about reorganizing your rules (either the specificity needed, or the layout of the nesting).

```
# Bad
x = code
code should do something

# Good
x = code
code should show something
```

## <a id='comments'></a>Comments

```
# Bad
x = code
code should do something

# Good
x = code
code should show something
```

## <a id='shorthand'></a>Shorthand

```
# Bad
x = code
code should do something

# Good
x = code
code should show something
```
