### Style HTML text properties

##### Applying color to text
Text color can be changed to using the color property. It accepts three methods:
 - Hexadecimal value
 - Color name
 - RGB function
 
##### Applying bold to text
CSS provides properties of the text via the font object.

The font weight object allows for:
- lighter
- normal
- bold
- bolder
- It also allows for a numeric value between 100 and 900

The font style for the font object allows it to be styled in italics.

##### Applying styles to text font

You can control font typeface in a few ways.

You can rely on fonts installed on the system rendering the page e.g.

```
p{
    font-family:Arial, 'Times New Roman', Webdings;
}
```

This uses the first it finds from left to right.

You can use WOFF (Web Open Font Format) by using the special keyword @font-face. This can be done like this:

```
@font-face {
    font-family: "My nicer font"
    src: url('fonts/my_woff_font.eot')
    src: url('fonts/my_woff_font.woff)
}

p {
    font-family: 'My Nicer Font';
}
```

Here, we give it a name and specify where it is loaded from, either the web server or external internet source.

We can used font-size to specify the size of the font. It accepts:
- xx-small
- x-small
- small
- smaller
- medium
- large
- larger
- x-large
- xx-large

##### Applying styles to text alignment, spacing, and indentation

Text alignment can be set using the text-align attribute. It's properties are...

| text-align property  | Description |
| ------------- | ------------- |
| right | aligns text to the right side of the parent container |
| left | aligns text to the left side of the parent container |
| center |  aligns text to the horizontal center of the parent container |
| justify | stretches text horizontally to fill the width of the parent container |


##### Text indentation

Text indentation is configured using the text-indent attribute. It accepts an integer value with how much to indent.

```
p {
    text-align: center;
}
```

##### Text spacing

There are two ways to control spacing of text:
 - letter-spacing
 - word-spacing
 
These can be used like this:
```
p {
    letter-spacing: 8px
}
```

##### Applying styles to text hyphenation 

Applying styles to text hyphenation allows you to control how sentences or words wrap at the end of the line.

| hyphen attribute | Description |
| ------------- | ------------- |
| none | Words will not break with a hyphen, sentence will only break on whitespace |
| Auto | Words will break on a predetermined algorithmn |
| Manual | Words will break on specified hints in the words e.g. using &shy notation within the text |

When auto is applied, the browser uses it's own rules to determine.
