# Viewport

One thing we have to be concerned with when building a responsive layout is the
_viewport_.  The viewport is the viewable area inside of the device's screen.

Some devices are automatically set to zoom in or zoom out in order to show
content correctly.  Mobile devices, in particular, may zoom out to fit an entire
webpage into the screen.  Our media queries, however, are all designed based on
the assumption that the content is not scaled.  Unless the user specifically
overrides by zooming in or out, _we_ want to have control of the default size of
elements, not the browser.

We achieve this by using the viewport meta tag inside of our html head section:

```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

This tag's content attribute is being set so that:

* The width of our viewport should be set to the width of the device
* The initial scale for the page will be set to the normal, default scale

There are other options that can be added, such as `minimum-scale=1.0` and
`maximum-scale=1.0`, _or, alternatively,_ `user-scalable=false`.  Adding these
along with setting width and initial scale will prevent users from zooming in or
out.  Doing this _can_ give you a greater control over how a site looks, but
it's generally best not to limit scaling, as this may affect screen readers that
need to zoom in users who are the visually impaired.

## Resources

* [Using the viewport meta tag to control layout on mobile](https://developer.mozilla.org/en-US/docs/Mozilla/Mobile/Viewport_meta_tag)

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/viewport' title='Viewport'>Viewport</a> on Learn.co and start learning to code for free.</p>
