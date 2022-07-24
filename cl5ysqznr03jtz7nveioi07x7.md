## Markdown README.md

# Headers
    # H1
    ## H2
    ### H3
    #### H4
    ##### H5
    ###### H6

output will be 

  # H1
 ## H2
 ### H3
 #### H4
 ##### H5
 ###### H6

---

# Bold 

      **Bold text here**         OR           __Bold text here__
 **Nilesh Nama**

# Italic

    *Italic *     OR    _Italic_
> *Nilesh Nama*

# Strike Through
    ~~1000~~  555


# List
    1. First ordered list item
    2. Another item
      * Unordered sub-list. 
    1. Actual numbers don't matter, just that it's a number
      1. Ordered sub-list
    4. And another item.  
       
       Some text that should be aligned with the above item.
    
    * Unordered list can use asterisks
    - Or minuses
    + Or pluses

1. First ordered list item
2. Another item
  * Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
  1. Ordered sub-list
4. And another item.  
   
   Some text that should be aligned with the above item.

* Unordered list can use asterisks
- Or minuses
+ Or pluses

---

# Links
there are two ways to create links as follows

    [I'm an inline-style link](https://blogs.nileshnama.com)
    
    [I'm a reference-style link][Arbitrary case-insensitive reference text]
    
    [You can use numbers for reference-style link definitions][1]
    
    Or leave it empty and use the [link text itself]
    
    URLs and URLs in angle brackets will automatically get turned into links. 
    http://www.example.com or <http://www.example.com> and sometimes 
    example.com (but not on Github, for example).
    
    Some text to show that the reference links can follow later.
    
    [arbitrary case-insensitive reference text]: https://www.nileshnama.com
    [1]: www.nileshnama.com
    [link text itself]: www.nileshnama.com

[I'm an inline-style link](https://blogs.nileshnama.com)

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself]

URLs and URLs in angle brackets will automatically get turned into links. 
http://www.example.com or <http://www.example.com> and sometimes 
example.com (but not on Github, for example).

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.nileshnama.com
[1]: http://www.nileshnama.com
[link text itself]: www.nileshnama.com

---

# Block Quote

    > Blockquotes are very handy
    > This line is part of the same quote.
    
    Quote break.
    
    > This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote.

> Blockquotes are very handy
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote.
 
---

# Code Snippet & Syntax highlighting
there can be two types of code snippets        1. Whole Code               2. Keyword

## 1. Whole Code
    ```
    write code Here

    ```


```
write code Here

``` 
## 2. Keyword
backtick is use for write just keyword

    `Hello World!`

`Hello World!`

# Image (hover to see the title text)

    Inline-style: 
    ![hashnode logo](https://github.com/NileshNama/NileshNama/blob/main/hashnodeLogo.png "Logo Title Text 1")
    
    Reference-style: 
    ![hashnode logo][logo]
    
    [logo]: https://github.com/NileshNama/NileshNama/blob/main/hashnodeLogo.png" Logo Title Text 2"



Inline-style: 
![hashnode logo](https://github.com/NileshNama/NileshNama/blob/main/hashnodeLogo.png) "Logo Title Text 1")

Reference-style: 
![hashnode logo][logo]

[logo]: https://github.com/NileshNama/NileshNama/blob/main/hashnodeLogo.png "Logo Title Text 2"

Or 
### Locally hosted Images
    ![text write here](./file path)

![Hello file](./helllo.jpg)

---

# For break the lines
    Three or more...
    
    ---
    
    Hyphens
    
    ***
    
    Asterisks
    
    ___
    
    Underscores

---
***
___

# Tables
Tables aren't part of the core Markdown spec, but they are part of GFM and Markdown Here supports them. They are an easy way of adding tables.

    Colons can be used to align columns.
    
    | Tables        | Are           | Cool  |
    | ------------- |:-------------:| -----:|
    | col 3 is      | right-aligned | $1600 |
    | col 2 is      | centered      |   $12 |
    | zebra stripes | are neat      |    $1 |
    
    The outer pipes (|) are optional, and you don't need to make the raw Markdown line up prettily. You can also use inline Markdown.
    
    Markdown | Less | Pretty
    --- | --- | ---
    *Still* | `renders` | **nicely**
    1 | 2 | 3
  Colons can be used to align columns.

| Tables            | Are                 | Cool   |
| -------------  |:-------------:|   -----:|
| col 3 is           | right-aligned | $1600 |
| col 2 is           | centered       |   $12    |
| zebra stripes | are neat        |    $1     |

The outer pipes (|) are optional, and you don't need to make the raw Markdown line up prettily. You can also use inline Markdown.

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3


# YT Videos
They can't be added directly but you can add an image with a link to the video like this:


```
<a href="http://www.youtube.com/watch?feature=player_embedded&v=lf7TVbYwJ7s
" target="_blank"><img src="https://github.com/NileshNama/NileshNama/blob/main/alanwalker.jpg" 
alt="Alan walker" width="240" height="180" border="10" /></a>

``` 


<a href="http://www.youtube.com/watch?feature=player_embedded&v=lf7TVbYwJ7s
" target="_blank"><img src="https://github.com/NileshNama/NileshNama/blob/main/alanwalker.jpg" 
alt="Alan walker" width="240" height="180" border="10" /></a>

