### Raise and handle an event

We can hook up an event to tell the browser when an event has occurred, this function is known as an event listener.

##### Event objects

An event object is a common object within event handlers that provides meta data about the event.

Can be done in:
- declared in html
- assign function to even property through javascript
- use addEventListener and removeEventListener methods


addEventListener

- takes event name and event function and optional cascade 
- same for removeEventListener


##### Using anonymous functions

Functions that don't have a name so can't be called elsewhere in the code

##### Canceling an event

We can cancel events to completely override the implementation of the native functionality of the DOM element.


##### Declaring and handling bubbled events

Event bubbling is the concept that applies when HTML document has nested elements.

##### Handling DOM events

##### Change Events
    
 - a change event occurs when the value associated with an element changes
    
###### Focus Events
 
 - a focus event fires when an element receives or loses the focus
 
    - focus (raised when it receives focus)
    - blur (raised when it loses focus)
    - focusin and focusout (raised just before an element recieves or loses focus)
    
###### Keyboard events

 - keydown
 - keyup
 - keypress
 
In some cases only the keydown will fire, not keypress or keyup, e.g. arrow keys.

###### Mouse Events

Events:
- click
- dblclick
- mousedown
- mouseup
- mouseenter or mouseover
- mouseleave
- mousemove

Properties:
- clientX
- clientY
- offsetX
- offsetY
- screenX
- screenY

###### Drag and drop functionality

Drag and drop functionality allows a user to pick up an element with the mouse and place it in another location.

###### Creating custom events

You can create custom events and call them dynamically.