### Structure a CSS file by using CSS selectors

#### Referencing Elements correctly

We can use element names, class selectors.

We can combined an element with a class selector.

```
p.largeTitle{
...
}
```

We can use ID like this:

```
#myId{
...
}
```

We can combine stylings like this:

```
p, h1, h2 {
...
}
```

#### Implementing inheritance

Some styles applied to a parent element are automatically inherited by the children.

If you then define new style to the child element, these will override inherited ones.

#### Overriding inheritance using !important

How a browser interprets style is it will use the last style it found when interpreting the stylesheets.

You can use the !important tag against a style to make sure a style takes priority.

e.g. 

```
p {
    font-family: serif;
    color: blue;
}

p {
    color: purple !important;
}

p {
    color: yellow;
}
```

Here this would make the color purple be applied.