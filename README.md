#jquery.transitionsend

> Execute a callback when *all* CSS transitions have ended.

## Getting Started

This plugin requires jQuery `~1.7.0`

This plugin is similar to the `transitionend` event, but it will only ever be called once. This is
especially useful when you are transitioning more than one property.

This plugin has been built to work with jQuery's `on()`, `one()` and `off()` functions instead of
a unique API. This allows for abstraction.

For browsers that do not support CSS transitions, the event will be called immediately without delay.

## Usage

### Overview
It is recommended that you use `jQuery.one()` instead of `jQuery.on()` as the callback will only be
called once.

```js
$(selector).one("transitionsend", function()
{
	// do something here
});
```

### Cancelling
```javascript
$(selector).off("transitionsend");
// or
$(selector).off();
```

## Release History
* 0.1.0 initial release