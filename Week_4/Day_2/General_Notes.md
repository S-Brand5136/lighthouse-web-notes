## Notes

### DOM Events

- Event listeners can be used to make this page interactive. To set up your app to respond to events:

  - Add an event listener to a DOM node
  - Specify which event it should listen for
  - Add a function that runs when that event happens

- addEventListener is a method available to any element/DOM node.

- When an event happens, an object is created that contains all the information about  that event. The callback function that you specify can automatically receive that object as a parameter

- In JavaScript, we can listen to events using this:

``` javascript
  element.addEventListener(<event-name>, <callback>, <use-capture>);
```
  - event-name (string) This is the name or type of event that you would like to listen to. It could be any of the standard DOM events (click, mousedown, touchstart, transitionEnd, etc.) or even your own custom event name (we’ll touch on custom events later).
  - callback (function) This function gets called when the event happens. The event object, containing data about the event, is passed as the first argument.
  - use-capture (boolean) This declares whether the callback should be fired in the “capture” phase. (Don’t worry: We’ll explain what that means a little later.)

  `Removing Listeners`
 
 - Removing event listeners once they are no longer needed is a *best practice*

 - To do this, use the element.removeEventListener() method:

``` javascript
  element.removeEventListener(<event-name>, <callback>, <use-capture>);
```
- But removeEventListener has one catch: You must have a reference to the callback function that was originally bound. Simply calling element.removeEventListener(‘click’); will not work.

```javascript

var element = document.getElementById('element');

function callback() {
  alert('Hello once');
  element.removeEventListener('click', callback);
}

// Add listener
element.addEventListener('click', callback);

```

`The event object`

 - is created when the event first happens. It travels with the event through the DOM.

`Event Phases`

  - When a DOM event fires in the app it doesn't just fire once, it has three different phases. 
    - capture phaose
    - target phase
    - bubbling phase
  
`Capture phase`

  - Its the first phase in a DOM event. 
  - It starts at the root of the document, and works its way down each layer of the DOM
  - The job of the capture phase is to build the propagation path that the event will travel back through during the bubbling phase
  - You can listen to the capture phase by setting the third argument of addEventListener to true

`Target phase`

  - This event fires on the taget node before bubbling back up the DOM

`Bubbling phase`

  - This event fires after the target phase is done
  - It bubbles up through the DOM until it reaches the documents root.
  
`Stopping Propagation`
  
  - To interrupt the path of any event at any point by calling the stopPropagation method on the event object. The event will no longer call any liseners.

  - with stopPropagation
  ``` javascript
child.addEventListener('click', function(event) {
 event.stopPropagation();
});

parent.addEventListener('click', function(event) {
 // If the child element is clicked
 // this callback will not fire
});
  ``` 
- with stopImmediatePropagation
``` javascript
child.addEventListener('click', function(event) {
 event.stopImmediatePropagation();
});

child.addEventListener('click', function(event) {
 // If the child element is clicked
 // this callback will not fire
});
```