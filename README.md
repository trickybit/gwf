gwf
===

Google Web Font LESS mixin

```less
& {
  .gwf('Lato', sans-serif; 100,200,400,700,900);
  
  body {
    .gwf.family;
  }
  
  h1 {
    .gwf.weight.rel(lighter);
  }
}
```
- [GIST](https://gist.github.com/tappily/0710b07bf250d3188d2b)
- [CodePen](http://codepen.io/tappily/full/bcLKv)

##gwf
Initializes a selector and imports the webfont, encoding entities, like whitespace characters, according to the Google Web Font service API.

### input
```css
.gwf('Lato', sans-serif; 100,200,400,700,900);
```
### output
```css
@import "//fonts.googleapis.com/css?family=Lato:100,200,400,700,900";
```
###params
- family{string}
- weights{list}

## family
### input
```css
.gwf.family;
```
### output
```css
font-family: 'Lato', sans-serif;
```

## weight
### input
```css
.gwf.weight(900);
```
### output
```css
font-weight: 900;
```
### params
- weight{number}

## rel
Use relative names from the CSS spec to pick the closet match from the initial weights provided to .gwf();

### input
```css
& {
  .gwf('Lato', sans-serif; 200,400,700);
  
  h1 {
    .gwf.weight.rel(lighter);
  }
}
```
### output
```css
h1 {
  font-weight: 200;
}
```
### params
- index {integer}
  - lighter
  - light
  - normal
  - bold
  - bolder

## name
Use common typographic names.

### input
```css
.gwf.weight.name(poster);
```
### output
```css
font-weight: 900;
```
### params
- name {keyword} 
  - extralight, ultralight
  - light, thin
  - book, demi
  - normal, regular
  - medium
  - semibold, demibold
  - bold
  - black, extrabold, heavy
  - extrablack, fat, poster, ultrablack
