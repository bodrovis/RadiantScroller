# jQuery RadiantScroller plugin

This is a jQuery plugin that allows to create responsive scrollers (carousels) with grid and simple horizontal layout.

## Requirements

1. jQuery 1.7.0+
2. [MouseWheel plugin](https://github.com/brandonaaron/jquery-mousewheel) (only if you want to provide mousewheel support)

## Installation and usage

1. Hook up required files
2. Hook up `jquery.radiant_scroller-min.js` and `jquery.radiant_scroller.css`
3. Set up basic layout for the scroller:
```html
<div id="your_scroller_id">
    <div class="scroller-el"><img src="image1.jpg" alt="Image1" /></div>
    <div class="scroller-el"><img src="image2.jpg" alt="Image2" /></div>
    <div class="scroller-el"><img src="image3.jpg" alt="Image3" /></div>
</div>
```
The `scroller-el` class is required.
4. Set up basic styling. In fact, only specifying margins and dimensions for the images in the scroller is required. This can be done like:
```css
.radiant_scroller .scroller-el {
    width: 200px;
    height: 200px;
    margin-right: 10px;
    margin-bottom: 10px; /* This is optional but recommended - otherwise your images will have no horizontal spacing */
}
```
5. Initialize the scroller. The values for `elementWidth` and `elementMargin` should be the same as your specified in the previous step otherwise the scroller's grid will be built incorrectly.
You will probably want to specify scroller's grid dimensions with the `cols` and `rows` attributes (the default is 2x2 grid).
```js
$(document).ready(function() {
    $('#myScroller').radiantScroller({
        elementWidth: 200,
        elementMargin: 10,
        cols: 3,
        rows: 3
    });
});
```
6. Style your scroller as needed.

## License

This plugin is licensed under the [MIT License](https://github.com/bodrovis/RadiantScroller/blob/master/LICENSE.txt).

Copyright (c) 2013 [Ilya Bodrov](http://radiant-wind.com)
