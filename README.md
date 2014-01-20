#jquery.transitionsend

> Execute a callback when *all* CSS transitions have ended.

## Getting Started

This plugin requires jQuery `~1.7.0` or Zepto `~1.1.2`

The `transitionsend` event is similar to the standard `transitionend` event, except that it is **only called once**—instead of once *per property*. This is especially useful for **advanced animation** where you are transitioning more than one property on any given element.

This plugin has been built to work with jQuery's [`on()`](http://api.jquery.com/on/), [`one()`](http://api.jquery.com/one/) and [`off()`](http://api.jquery.com/off/) functions instead of
a unique API. This **allows for abstraction**.

- - -
The event will be dispatched immediately without delay in these situations:
* Elements with no CSS transitions applied
* Browsers that do not support CSS transitions

- - -
*Note*: Current technology prohibits the ability to detect when a transition has been cancelled (by means of CSS or other). You will have to keep track of such things yourself.

## Usage
### Overview
It is recommended that you use `jQuery.one()` instead of `jQuery.on()` because the callback will only be
triggered once.
```js
$(selector).addClass("cool-transition");

$(selector).one("transitionsend", function()
{
	// do something here
});

// Cancel event
$(selector).off("transitionsend");
```

### Reflow
A `reflow` function is also included. It "relayouts" elements, preparing them for an immediate repaint (or "rerender"). It comes in handy when adding a transition `className` to your newly created element and actually having the transition play.
```javascript
$("body").html('<div id="something"/>');
$("#something").reflow();
$("#something").addClass("cool-transition");
// it animates!
```

## Release History
* 0.2.0 added AMD support
* 0.1.2 added Zepto support
* 0.1.1 renamed `repaint` to `reflow`
* 0.1.0 initial release
