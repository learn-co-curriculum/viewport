# The Viewport Property

## Problem Statement

Have you ever visited a website on your phone where it will zoom out
and everything on the page is very tiny--then you have to zoom in to
read the text and see the content? Have you found yourself writing a
lot of media queries to make your content scale, stretch, or fit on
various sized screens, just to have the device itself ignore them and
out on your website? How can we have control over these default features
that mobile browsers enforce?

## Objectives

1. Explain the `width` property of viewport meta tag
2. Explain the `initial-scale` property of viewport meta tag

## Explain the `width` Property of Viewport Meta Tag

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

## Explain the `initial-scale` Property of Viewport Meta Tag

You will want to specify that the width of our viewport should only be *exactly*
as wide as the device. Set its initial scale to 1.0--indicating that the device's
initial scale is set to a normal scale, and not to zoom in or out on this content.

```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

If we look at our previous example again, this tag's content attribute is being
set so that:

* The width of our viewport should be set to the width of the device
* The initial scale for the page will be set to the normal, default scale

There are other options that can be added, such as `minimum-scale=1.0` and
`maximum-scale=1.0`, _or, alternatively,_ `user-scalable=false`.  Adding these
along with setting width and initial scale will prevent users from zooming in or
out.  Doing this _can_ give you a greater control over how a site looks, but
it's generally best not to limit scaling, as this may affect screen readers that
need to zoom in users who are the visually impaired.

## Conclusion

When building a responsive layout, we have to be concerned with the _viewport_
property. This is the viewable area inside of the device's screen. Some devices
are set up to zoom in or zoom out, so that it will scale the content to fit the
screen. With the use of the `viewport` meta tag we can scale websites so the
content plays well with the media queries, and prevents the user from zooming
in or out on this content and breaking the layout.

## Resources

* [Using the viewport meta tag to control layout on mobile](https://developer.mozilla.org/en-US/docs/Mozilla/Mobile/Viewport_meta_tag)

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/viewport' title='Viewport'>Viewport</a> on Learn.co and start learning to code for free.</p>
