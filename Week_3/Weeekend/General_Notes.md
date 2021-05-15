## Notes

- Event Bubbling

When an event happens – the most nested element where it happens gets labeled as the “target element” (event.target).

  - Then the event moves down from the document root to event.target, calling handlers assigned with addEventListener(..., true) on the way (true is a shorthand for {capture: true}).
  - Then handlers are called on the target element itself.
  - Then the event bubbles up from event.target to the root, calling handlers assigned using on<event>, HTML attributes and addEventListener without the 3rd argument or with the 3rd argument false/{capture:false}.

Each handler can access event object properties:

  - event.target – the deepest element that originated the event.
  - event.currentTarget (=this) – the current element that handles the event (the one that has the handler on it)
  - event.eventPhase – the current phase (capturing=1, target=2, bubbling=3).

Any event handler can stop the event by calling event.stopPropagation(), but that’s not recommended, because we can’t really be sure we won’t need it above, maybe for completely different things.

[Website about even bubbling and capturing]('https://javascript.info/bubbling-and-capturing')