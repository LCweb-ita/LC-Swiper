# TouchSwipe events made easy, by LCweb

No dependencies **vanilla javascript class** to easily handle swipe events on page elements.

 - gives you the swipe delta in each direction
 - supports multiple instances per element
 - features a destroy public method (targeting the specific instance)
 
What do you want more from 2KB of code? :P<br/>
**NB:** obviously it works only for touch devices.


For live demos check: https://lcweb.it/lc-swiper-javascript-plugin


## Installation & Usage

1. include lc-swiper.min.js

2. initialize plugin targeting one/multiple page elements and the callback function triggered after each swipe.<br/><br/>NB: first parameter may be a textual selector or a DOM object (yes, also jQuery objects)


You must use a valid callback function as second parameter. It will be triggered each time a swipe event is performed.<br/>
It has got two parameters:


```
<script type="text/javascript>
new lc_swiper('#swipe_target', function(directions, $el) {

    // .. do something awesome!

    /*
     * directions object composition:
     * {
        up      : (int) number of pixels swiped
        right   : (int) number of pixels swiped
        down    : (int) number of pixels swiped
        left    : (int) number of pixels swiped
     * }
     */

});
</script>
```

## Multiple actions and the destroy method

As said, you can setup multiple instances of the class and also destroy the single instance for a granular control on what is enabled

```
<script type="text/javascript>
const instance1 = new lc_swiper('#swipe_target', function(dir, $el) {
    ... 
});

const instance2 = new lc_swiper('#swipe_target', function(dir, $el) {
    ... 
});


// stop performing the first instance callback on swipe
instance1.destroy();
</script>
```



* * *


Copyright &copy; Luca Montanari - [LCweb](https://lcweb.it)
