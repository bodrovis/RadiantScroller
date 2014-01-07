# jQuery RadiantScroller plugin

This is a jQuery plugin that allows to create responsive scrollers (carousels) with grid and simple horizontal layouts.

## Demos

* [Basic scroller with 3x2 grid and with no mousewheel support and no pagination](http://www.radiant-wind.com/code_examples/10)
* [Scroller with 3x2 grid and with mousewheel support and pagination](http://www.radiant-wind.com/code_examples/11)

## Requirements

1. jQuery 1.7.0+
2. [MouseWheel plugin](https://github.com/brandonaaron/jquery-mousewheel) (only if you want to provide mousewheel support)

## Installation and usage

* Hook up required files

* Hook up `jquery.radiant_scroller-min.js` and `jquery.radiant_scroller.css`

* Set up basic layout for the scroller:

```html
<div id="your_scroller_id">
    <div class="scroller-el"><img src="image1.jpg" alt="Image1" /></div>
    <div class="scroller-el"><img src="image2.jpg" alt="Image2" /></div>
    <div class="scroller-el"><img src="image3.jpg" alt="Image3" /></div>
</div>
```

The `scroller-el` class is required.

* Set up basic styling. In fact, only specifying margins and dimensions for the images in the scroller is required. This can be done like:

```css
.radiant_scroller .scroller-el {
    width: 200px;
    height: 200px;
    margin-right: 10px;
    margin-bottom: 10px; /* This is optional but recommended - otherwise your images will have no horizontal spacing */
}
```

* Initialize the scroller. The values for `elementWidth` and `elementMargin` should be the same as your specified in
the previous step otherwise the scroller's grid will be built incorrectly.
You will probably want to specify scroller's grid dimensions with the `cols` and `rows` attributes (the default is
2x2 grid). All available options are listed in the "Options" section.

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

* Style your scroller as needed.

## Options

<table>
  <thead>
    <tr>
      <th>Property</th>
      <th>Default</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row"><code>animateDuration</code></th>
      <td><code>700</code></td>
      <td><code>Integer</code> Animation duration for the scrolling. The value is specified in milliseconds.</td>
    </tr>
    <tr>
      <th scope="row"><code>addPagination</code></th>
      <td><code>false</code></td>
      <td><code>Boolean</code> Whether the scroller should have pagination
      (often displayed as small navigational dots) enabled.</td>
    </tr>
    <tr>
      <th scope="row"><code>cols</code></th>
      <td><code>2</code></td>
      <td><code>Integer</code> How many cols should the scroller have - basically this means how many elements
      will be visible at once horizontally (but if the scroller's width changes this value will also change).</td>
    </tr>
    <tr>
      <th scope="row"><code>easingType</code></th>
      <td><code>"swing"</code></td>
      <td><code>String</code> Easing type for the scrolling. You can specify any other type of easing but bear in mind
      that jQuery has only <code>swing</code> and <code>linear</code> easings included.
      You will have to include
      <a target="_blank" href="http://jqueryui.com/effect/#easing">jQueryUI's effects and easings plugin</a> to get more.</td>
    </tr>
    <tr>
      <th scope="row"><code>elementMargin</code></th>
      <td><code>10</code></td>
      <td><code>Integer</code> Horizontal (left/right) margin for the scroller's elements. This value should correspond
      to the value that is provided in the styles.</td>
    </tr>
    <tr>
      <th scope="row"><code>elementWidth</code></th>
      <td><code>200</code></td>
      <td><code>Integer</code> Width for the scroller's elements. This value should correspond
      to the value that is provided in the styles.</td>
    </tr>
    <tr>
      <th scope="row"><code>nextButtonText</code></th>
      <td><code>""</code></td>
      <td><code>String</code> Text to be shown on the "next" button.</td>
    </tr>
    <tr>
      <th scope="row"><code>prevButtonText</code></th>
      <td><code>""</code></td>
      <td><code>String</code> Text to be shown on the "previous" button.</td>
    </tr>
    <tr>
      <th scope="row"><code>rows</code></th>
      <td><code>2</code></td>
      <td><code>Integer</code> How many rows should the scroller have.</td>
    </tr>
    <tr>
      <th scope="row"><code>useMouseWheel</code></th>
      <td><code>false</code></td>
      <td><code>Boolean</code> Whether support for the mousewheel scrolling should be enabled. Please note
      that when this value is set to <code>true</code>, you should hook up
      <a target="_blank" href="https://github.com/brandonaaron/jquery-mousewheel">MouseWheel plugin</a>.</td>
    </tr>
  </tbody>
</table>

## License

This plugin is licensed under the [MIT License](https://github.com/bodrovis/RadiantScroller/blob/master/LICENSE.txt).

Copyright (c) 2013 [Ilya Bodrov](http://radiant-wind.com)
