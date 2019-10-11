### Apply styling to HTML elements programmatically

By default, all HTML elements flow statically from left to right in the same order they are declared.

CSS provides a mechanism to specify some advanced options in element position, you can position elements using *absolute positioning* & *relative positioning*.

With *absolute positioning*, an element is placed in the exact location specified relative to its container's borders.

With *relative positioning*, an element is positioned to its immediate left sibling's coordinates.

You can apply four properties individually or in combination to control the position of an element; top, left, right and bottom.

So absolute is relative to the parent container, whereas relative is relative to the left sibling node



#### Applying a transform

Applying a transform is a way to change an object on the webpage. 

To add a transform to an element, you can declare it in the css for the element by add the transform property e.g.

`.rota { transform: rotate(90deg);}`

We can use:

 - rotate
 - translate
 - skew 
 - scale ( resize element by a specified ratio)
 
 
#### Showing and hiding elements

Display properties can tell whether a HTML element is to be displayed...

*Inline* tells the browser to show item, whereas *none* tells the browser to hide the item.


The second property for deciding whether an item is show is the visibility property.

| visibility property | effect |
| ------------- | ------------- |
| visible | show the element |
| hidden | hides the element |
| collapse | collapses the element where applicable e.g. table row |
| inherit | inherit the value from parent |

The visibility property acts slightly differently to the display property. Setting the visibility hides and element but the surrounding acts like it is still there.
