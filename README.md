#jquery.transitionsend

> Execute a callback when *all* CSS transitions have ended.

## Getting Started

This plugin requires jQuery `~1.7.0`

The `transitionsend` event is similar to the standard `transitionend` event, but it will only ever be called once. This is
especially useful when you are transitioning more than one property on any given element.

This plugin has been built to work with jQuery's [`on()`](http://api.jquery.com/on/), [`one()`](http://api.jquery.com/one/) and [`off()`](http://api.jquery.com/off/) functions instead of
a unique API. This allows for abstraction.

For browsers that do not support CSS transitions, the event will be triggered immediately without delay.

## Usage
It is recommended that you use `jQuery.one()` instead of `jQuery.on()` because the callback will only be
called once.

Usage is the same as with any other event in jQuery.

```js
$(selector).one("transitionsend", function()
{
	// do something here
});

// Cancel event
$(selector).off("transitionsend");
```

## Release History
* 0.1.0 initial release
