### Find elements using CSS selectors and jQuery

#### Defining element, style, and attribute selectors

CSS use selectors that you define in a file or style block to define which elements should be styled.

We can use element selectors:
```
div {
}
```

We can use class selectors:
```
.mycustomclass {

}
```
We can also use attribute selectors, i.e. select all input fields with the require attribute:

```
input[required]{ 

}
```

List of attribute selectors:

| Attribute selector| description|
|---|---|
| = | Specifies that an attribute equals a specific value|
| ~= | specifies a space separated words as the values for an attribute |
|^= | Specifies attribute value starting with the selector value|
| $= | Specifies attribute value ending with the selector value|
|*=| Specifies that the attribute value must contain the selector value|

#### Finding elements by using pseudo element and pseudo classes

Pseudo classes allow you to apply styles to an element based on its state, its interaction with the user, or position in document.

##### :link, :visited, :hover
These are the most commonly used pseudo classes.
Links can be styled a certain way if they have been used, or are being hovered on.

##### :checked

This allows you to apply stylings to an element that is in a checked state.  e.g.
```
input[type="checkbox"]:checked {
}
```

##### :required

This allows you to apply stylings to any element that have the required attribute.

##### :enabled and :disabled

This allows you to style controls based on their enabled or disable state.

##### :first-child

This selector applies a styling to the first element that occurs in a list.

##### :first-letter

This selector will alter the style of the first letter in the specified element.


##### :before and :after

This will add the specified content before or after the selected elements.

E.g. This will add ** before all paragraphs.    

```
p::before{
    content: '**';
}
```