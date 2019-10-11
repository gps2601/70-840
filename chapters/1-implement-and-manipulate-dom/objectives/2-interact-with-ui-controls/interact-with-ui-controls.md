### Write code that interacts with UI controls.

The ability to modify the HTML document at run time is very powerful. 
Javascript provides the toolkit you need to write code that interacts with web page elements.


#### Document Object Model (DOM)

The DOM is a representation of the structure of your HTML page that you can interact with programmatically.

Behind the scenes, the browser constructs a DOM, the DOM's API is exposed as objects with properties with properties and methods, which allows you to write JS to interact with the page.

The DOM is essentially a collection of nodes arranged in a tree.

#### Selecting items in the DOM 

| Method  | Description |
| ------------- | ------------- |
| `getElementById()` | Gets an individual element on the page by its unique id |
| `getElementsByClassName()` | Gets all the elements with a specified class applied |
| `getElementsByTagName()` | Gets all elements of the page that have the specified tag/element name |
| `querySelector()` | Gets the first child element that matches the provided css selector criteria |
| `querySelectorAll()` | Gets all elements that matches the provided css selector criteria |


The getElementsByClassName returns all elements that have a specified class, not just those of a specified type.

querySelector returns the first method it finds using a query selector

 - To find all `<p>` elements you can using document.querySelectorAll('p')
 - To find a `<p id='outerDiv>` elements you can using document.querySelector('#outerDiv')

#### Altering the DOM

You can use `document.removeChild()` to remove an element in the DOM.

You can use `document.createElement()` to create a new HTML element.

Elements have `element.appendChild()` to allow you to add new HTML elements to an element. It returns a reference to the newly added node.

The `appendChild()` method always adds to the end of the parent nodes list.

The `insertBefore()` method adds to the child element to the start of the parents nodes list.

If you try to insert elements into a node that doesn't support child nodes e.g. an img tag, then the interpreter will throw a run-time error.

The `removeChild()` removes a child node from the calling container and returns a reference to the removed node.

The `removeNode()` does a deep removal of an element such that all children elements are also removed.

We also have `replaceChild()` and `replaceNode()` which allows you to replace the target element with a completely new element.


#### Implementing media controls

We have two new elements that allow you to work with multimedia natively in browser `<video>` & `<audio>`.

Embedding a video in the page is as simple as adding the following markup..
`<video src='samplevide.mp4' autoplay></video>`

| `<video>` attributes | Description |
| ------------- | ------------- |
| src | src of video to play |
| autoplay | tells the browser to start playing the video as soon as it loads |
| controls | tells the browser to display built in controls |
| height/width | control amount of space the video occupies |
| loop | loop the video |
| poster | specifies an image to show in place of the allocated video until it has been played|

You can provide multiple sources and let the browser choose which format to play e.g.
You can also provide an `<object>` tag to cover the scenario where you dont have a compatible format.

```
<video >
    <source src='samplevideo.ogv' type='video/ogg'/>
    <source src='samplevideo.mp4' type='audio/mp4'/>
    <object> 
        <p> Video is not supported by this browser </p>
    </object>
</video>
```

The `<video>` tag offers many methods to interact with videos, these methods can be attached to additional html elements.


The `<audio>` tag is essentially identical to the video element. They just both provide a standardised way to represent multimedia


#### Implementing graphics with HTML `<canvas>` and SVG

`<canvas>` provides a blank canvas on which you can draw dynamically.

Canvas coordinates start from the top left being (0,0)


Both the canvas and svg grpahics engines can draw text, lines, shapes, fonts, fills and gradients.
The canvas element is drawn on via javascript getting a reference to the context.
The svg element renders graphics by using a declarative syntax.
