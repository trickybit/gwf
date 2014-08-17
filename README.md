gwf
===

Google Web Font LESS mixin

###gwf

#### input
```css
.gwf('Lato', sans-serif; 100,200,400,700,900);
```
#### output
```css
@import "//fonts.googleapis.com/css?family=Lato:100,200,400,700,900";
```
####params
- family{string}
- weights{list}

### family
#### input
```css
.gwf.family;
```
#### output
```css
font-family: 'Lato', sans-serif;
```

### weight
#### input
```css
.gwf.weight(900);
```
#### output
```css
font-weight: 900;
```
####params
- weight{number}

### rel
#### input
```css
.gwf.weight.rel(lighter);
```
#### output
```css
font-weight: 100;
```
#### params
- index {integer}

### name
#### input
```css
.gwf.weight.name(poster);
```
#### output
```css
font-weight: 900;
```
#### params
- name {keyword} 
