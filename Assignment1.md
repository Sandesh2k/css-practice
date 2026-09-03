# CSS fundamentals
```html 
    <div id="container">
    <p class="text">Hello</p>
    </div>
    <style>
    .text { color: red; }
    #container p{ color: blue; }
    </style>
```

This issue occurs due to specificity:
inline > id > class > element

Here, #container(id) has higher priority than .text(class), p (element) is also associated with #container that is all p inside #container have to accept the assigned property.

It can be solved using:
1. If p is removed, then #container is applied only on parent and .text will work on p.

```html 
    <div id="container">
    <p class="text">Hello</p>
    </div>
    <style>
    .text { color: red; }
    #container { color: blue; }
    </style>
```

2. If another block is added:
#container .text{color: red;}
 then .text will work as class has higher priority than element.

 ```html 
    <div id="container">
    <p class="text">Hello</p>
    </div>
    <style>
    .text { color: red; }
    #container p{ color: blue; }
    #container .text{color: red}
    </style>
```
