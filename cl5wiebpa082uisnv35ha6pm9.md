## Selector & Pseudo Selector in CSS3

# CSS3  Selector

in a generic manner, selector can define as 
``` 
Selector {
        background-color: #4d4d4d;
        color: #ffffff;
      }
``` 

Here we should point that in the "Selector "  can be the tags / asterisk*  etc 
&  declare all styles and background color, color etc inside the {  } curly brackets .


## 1. Universal Selector
to select everything, we use asterisk (*)


```
      * {
        background-color: #4d4d4d;
        color: #ffffff;
      }
``` 

## 2. Individual Selector
```
      p {
        background-color: yellow;
      }
```
here we can see this code snippet for paragraph tag. it can be extend to any type or individual tag like img or div.

## 3. Class Selector

```
.warning {
        background-color: #fdfdfd;
        color: black;
      }
``` 
this will select whole warning class


## 4. ID Selector

```
#hero {
        background-color: red;
        color: blue;
      }
``` 

## 5. List Selector (also known as and selector (chained) )

```
      li.bg-black.text-white {
        background-color: green;
        color: #fdfdfd;
      }

``` 
## 6. Combined Selector (Selector List)

```
      span, li
          {
            background-color: burlywood;
            color: black;
          }

``` 

# Combinator Selectors

## 7. Inside an element

```
div ul li {
        background-color: orange;
        color: violet;
      }
``` 

## 8. direct child


```
 div > li {
        background-color: pink;
      }
``` 

## 9. sibling + 


```
.sibling + p {
        background-color: red;
      }
``` 

## 10. sibling  ~

.sibling ~ p {
        background-color: red;
      }

# Attribute Selectors

## 12.  a[href="#"]
below will style all anchor tags which link to ineuron.com,  they'll receive the black color. All other anchor tags will remain unaffected.

```
a[href="https://ineuron.com/"] {
  color: black; 
}
``` 

## 13.  a[href*="#"]
the star designates that the proceeding value must appear somewhere in the attribute's value

```
a[href*="hashnode"] {
   color: blue; 
}
``` 

## 14.  a[href^="https"]
^ designates the beginning of a string. If we want to target all anchor tags that have an href which begins with https.

```
a[href^="http"] {
   text-decoration: 1px solid blue;
   padding-left: 10px;
}

``` 

## 15.  a[href$=".mp4"]
$ refers to the end of a string. In this case, we're searching for all anchors which link to an image—or a URL that ends with .mp4.

```
a[href$=".jpg"] {
   color: red;
}

``` 



**Now we talk about Pseudo Selectors and their variants**

## a: hover

```
li:hover {
        background-color: yellow;
        border: 2px solid black;
        padding: 5px;
      }
``` 

## a: focus


```
input:focus {
        background-color: red;
        color: wheat;
      }

``` 
 
## first child, last child, nth child


```
li: first-child {
        background-color: orange;
      }
``` 


```
li: last-child {
        background-color: orange;
      }
``` 


```
li: nth-child {
        background-color: orange;
      }
``` 



## custom  data attributes
```
[nileshnama] {
        background-color: purple;
      }
```

# Part of label

## 16. before :: part of label


```
.imp-label::before {
        content: "hello";
        display: block;
        width: 20px;
        height: 20px;
        border-radius: 10px;
        background-color: orange;
      }
``` 


## 17. after :: part of label 


```
.imp-label::after {
        content: "hello again";
        display: block;
        width: 20px;
        height: 20px;
        border-radius: 10px;
        background-color: orange;
      }
``` 


➖➖➖✨The End✨➖➖That's all from my side, Thank you💖 !

%%[buymeacoffee]









