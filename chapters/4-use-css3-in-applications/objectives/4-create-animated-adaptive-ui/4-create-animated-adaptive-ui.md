### Create an animated and adaptive UI

#### Animating objects by applying CSS transitions

A transition starts when the specified property is changed

|css3 transition property | description|
|---|---|
|transition-property| thr transition being applied|
|transition-duration| how much time is should take|
|transition delay | how long after a property is changed should it initiate |

Transitions also have a property called transition-timing-function which allows you to control the speed of the effect in different ways.

#### Applying 3-D and 2-D transformations

You can apply three dimensional transitions to html elements

|transformation| description|
|---|---|
|translate| moves object from current location to new location|
|scale| changes the size of object|
| rotate| spins the object along the x/y/z axis|
| matrix| allows you combine the transformations in one command|

Can be done either...
```
div {
    transform: rotateX(30deg) rotateY(30deg) rotateZ(deg)
}
```
or

```
transform: rotate3d(1,1,1, 30deg)
```

#### Adjusting UI based on media queries

Media queries allow you to adjust elements based on the size available to the webpage

They look like this....
```
@media screen and (max-width: 800px){

}
```

These styles will be applied when the screen is less than 800px.

You can specify media queries when you link in your style sheet e.g.

```
<link rel='stylesheet' media='screen and (min-width: 1200px)" href= "Desktop.css"/>
```

#### Hiding or disabling controls

You can set the visibility of a css property like this..

```
.myhiddenelements {
    visinility: hidden;
}
```

This will act like the element is still there, but you can't see it.

If you went to completely remove the element from the layout visually, use *display: none*.