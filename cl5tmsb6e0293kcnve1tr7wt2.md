## Position in CSS3

In general position define as 
```
 position: positiontype;

``` 
There are 4 kind of positiontype that are very essential and useful, understanding positions helps to design interface in a better way & that looks beautiful also.

- static
- relative
- absolute
- fixed

for desired position, one of them is use

# 1. Static
it is a by default position for any html element

![Screenshot (28).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658318656100/d0F0kXHky.png align="left")

it is a fixed position, we can't change it by use of top/bottom/right/left.

# 2. Relative
in this position html element can change relative to its original position.
this can move html element   top/bottom/right/left from relative to *Its DOM configuration*. where ever DOM inject the html element in webpage. 

```
.big {
        position: static;
        /* height: 200vh; */
        margin-top: 200px;
      }

```


![Screenshot (29).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658321541572/yyFgEQFkF.png align="left")

```
.big {
        position: relative;
        top: 200px;
        left: 200px;
      }
```

![Screenshot (30).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658321551185/HHVv5sw7F.png align="left")

# 3.Absolute
we can understand it by following statements:
1. just move me from top/bottom/right/left relative to my just parent (just above)
2. if parent say nothing relative or static  anything  then  *go to relative to parent of parent also (just above one).


```
.big {
        position: static;
        top: 200px;
        left: 200px;
        /* height: 200vh; */
      }
``` 


![Screenshot (31).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658322339038/ub7yuvy-1.png align="left")

```
.big {
        position: absolute;
        top: 200px;
        left: 200px;
        /* height: 200vh; */
      }
``` 

![Screenshot (32).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658322348605/rAK8SKQA_.png align="left")

so in brief the absolute position for any html element is relative to its very close Parent.

# 4. Fixed
move relative to the at the browsers very top[ (don't care who is parent or where its injected by DOM)
regardless what is the screen size , its fixed at one place.


```
.big {
        position: fixed;
        top: 200px;
        left: 200px; */
        
      }
``` 

![Screenshot (34).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658322596633/VZ5klFLHh.png align="left")


this is the all about the position in CSS3, thank you.

