### Create a flexible content layout

#### Implement a layout using a flexible box model

The flexbox is a css3 construct that provides a way to lay out elements that flow.

All the items within a flexbox are called flexbox items.

You can specify it to run horizontally or vertically.

| style | option | description | 
| ------------- | ------------- |------- |
| flex-direction | column | vertical axis top to bottom |
|  | row (default) | horizontal axis left to right|
|  | column-reverse | vertical axis bottom to top|
|  | row-reverse | horizontal axis right to left|
| flex-pack | End | renders child elements from end in relation to layout axis set direction|
|  | Start | renders child elements from the start in relation to layout axis set direction|
|  | center | renders the child elements centered on the layout axis|
|  | distribute | evenly spaces the child elements|


You can use the 'flex' property to specify how much an element takes up of the container relative to others.

You can use the 'flex-order' property to order items within a flexbox container.

You can also use the 'flex-wrap' property to set whether an item should wrap or not if items in a container have exceed the length of the container.


#### Implementing a layout using position, floating, and exclusions

Float is a mechanism where the surrounding content will flow smoothly around the element with it's float property set either left or right.

Exclusions provide a way to overcome this limitation with float.

They are achieved by using the CSS3 property wrap-flow

|wrap-flow property| description|
|---|---|
| auto| the default, the exclusion will be over the top of the inline element|
| both | this exclusion will force the inline element to wrap smoothly on both sides|
| start | this exlcusion will force the elements to wrap only on the starting edge|
|end| this exclusion will force the inline element to wrap only the ending edge|
|maximum | the exclusion will force the inline element to wrap only on the side with the largest available space|
|clear| this exclusion will force the inline content to wrap only on the top and bottom and leave the start and end edges empty|

#### Implementing a layout using grid alignment

The grid layout capability of CSS3 provides a way to layout the content of the webpage like a HTML but using only CSS3 to achieve the results.

grid-columns allows you to specify how many columns are in your grid

grid-rows allows you to specify how many rows are in your grid

You need to give each child element awareness of where it is placed in the grid with *grid-column: 1 and grid-row: 2* otherwise they will all float on top of eachother.

You can use *grid-row-span* and *grid-column-span* to specify how much of a row or column an element should span relative to other items in the row or column.

#### Implementing a layout using regions, grouping and nesting

Regions is a new CSS3 construct that allows you to have content flow through various regions in a webpage.

Exam unlikely to cover this as it is experimental.