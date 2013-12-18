#jquery.transitionsend

> Execute a callback when *all* CSS transitions have ended.

## Getting Started

This plugin requires jQuery `~1.7.0`

The `transitionsend` event is similar to the standard `transitionend` event, except that it will only ever be called once—instead of once *per property*. This is especially useful for advanced animation where you are transitioning more than one property on any given element.

This plugin has been built to work with jQuery's [`on()`](http://api.jquery.com/on/), [`one()`](http://api.jquery.com/one/) and [`off()`](http://api.jquery.com/off/) functions instead of
a unique API. This allows for abstraction.

For browsers that do not support CSS transitions, the event will be triggered immediately without delay.

Current technology limits this plugin's ability to detect if a transition has been cancelled (by means of CSS changes or other). You will have to keep track of such things yourself.

## Usage
It is recommended that you use `jQuery.one()` instead of `jQuery.on()` because the callback will only be
called once.

Usage is the same as with any other event in jQuery:
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
