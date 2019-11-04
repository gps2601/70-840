### Style HTML box properties

Every HTML has box properties, these control how the element is spaced on the page and controls the position of the box contents.

#### Applying styles to alter appearances attributes

##### Altering the size

The size of any element is controlled by its height and width properties.

By default an object will size itself to be able to display its contents.
E.g. a div will size itself to show the text content in it.

Height and width can be set in pixels (px) or centimeters (cm), or can be set as a percentage of its parent element (%)

E.g.
```
table {
    width: 50%;
    height: 50%;
}
```

This will set table to be 50 percent of its parent container.

##### Bordering

With the border property, you can control style, spacing, color and width of the border of a html element

e.g.

```
p {
    border-style: solid;
}
```
The border needs to exist before being changed, so border-style is set first.

*border-spacing* is used tol set the amount of space desired between desired adjacent elements.
E.g.
```
p {
    border-spacing: 205px;
}
```
Will provide 250px border spacing to all paragraph elements on the page.

Border properties can be set in short hand like this

```
p {
    border: 5px solid black;
}
```

Border properties can also be applying to each part of the border using:
 - border-top
 - border-left
 - border-right
 - border-bottom
 
##### Padding and margin

Padding and margin are additional methods to create space around a HTML element.

In essence there are three layers around a HTML element; padding, border and mergin (from inside to out).

Padding is distance between border and internal element content.
Can be set using...

```
padding: 25px 25px 25px 25px;
padding-top: 20px;
...
```

Margin is the space between the border of your element and the surrounding elements.

It is controlled in the same way as the padding.

#### Applying styles to alter graphics

##### Applying transparency / opacity

Setting *opacity* is done from a value from 0 to 1.0
0 indicated complete transparency, 1.0 is completely opaque

##### Applying a background image

Any html element can also contain a background image, this is done using the *background-image* property.

| background property  | Description |
| ------------- | ------------- |
| size | changes dimensions of imaghe |
| repeat | specifies whether the image should be repeated/tiled throughout the element |
| clip | specifies if the image should be clipped at the border |
| position-x/position-y | specifies the origin position of the image |


##### Applying gradients

A gradient changes the color gradually from one spectrum to another.

Two types of gradient:
 - Linear gradient
 - radial (from edges)
 
 They take direction attributes and color stop attributes.
 
##### Applying a shadow effect

Shadow effects allow you to apply a shadow to your HTML elements box.

We have box-shadow and text-shadow.

Most important attribute is h-shadow and v-shadow which dictate where the shadow is place relative to the box.

##### Applying clipping

The clip property allows you to specify what portion of an element is visible.

It takes only one parameter, the shape to clip to.

Only rectangles supported so you must use 'clip: rect(25px, 20px, 10px, 10px)'

Clip only works on elements whose position is fixed or absolute.


#### Apply styles to establish and change an elements position

The browser provides a coordinate system for how to layout elements on the page. It will simply layout in a default flow. with base coordinate at the top left of the window. (0,0)

All child elements have their own coordinate system relative to their parents div.

The position property allows you to specify three options
 - Fixed  (relative to the browser window)
 - Relative (Positioned relative to their position in normal flow)
 - Absolute (Positioned relative to its first parent element)
 
 Absolute positioning allows you to specify the location of an image such that it is removed from the normal flow.
 It can be considered as hovering above or under other elements.
 
 We also have the *float* property.
 
 Float automatically moves elements to the left or the right of surrounding content, most commonly used to place image in line with text and allow the text to flow around the image.
