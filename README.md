animate.js
==========
~~~
compact and fast vanilla.js anythig animation library
~~~
Usage:
------
animate any attributes of function:
```js
animate({
  target: window.scrollTo,
  interval: 100, // set framerate to 10 fps (1000/interval) default value 50 (20 fps)
  duration: 2000, // 2 sec
  easing: 'easeInOutExpo', // any functions, listed at http://easings.net/en are present plus easeLinear
  attributes:[
    0, // x attribute not animated, so just pass a static value
    { from: window.scrollY, to: 0 } // scroll to the page start
  ]
})
```
animate any properties of object:
```js
animate({
  target: document.getElementById('my_div').style,
  duration: 2000, // 2 sec
  easing: 'easeOutCubic', 
  properties:{
    top: { from: 200, to: 100, post: 'px'} , 
    transform: { pre: "rotate(", from: 0, to: 360, post: "deg)" },
    opacity: { from: 1, to: 0 }
  }
})
```
