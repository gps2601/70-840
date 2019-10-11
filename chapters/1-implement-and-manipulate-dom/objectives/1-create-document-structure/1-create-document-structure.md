### Create the document structure

Objectives:
1. Use HTML5 semantic markup
2. Create a layout container in HTML
3. Optimize for search engines
4. Optimize for screen readers



#### Semantic Markup

| HTML5 Element  | Description |
| ------------- | ------------- |
| `<article>` | Define self contained areas on page  |
| `<aside>`  | Define smaller content areas outside the flow of a webpage  |
| `<figcaption>`  | Defines the caption of a figure element  |
| `<figure>`  | Defines content that contains a figure e.g. image/chart  |
| `<footer>`  | Defines the bottom section of a page  |
| `<header>`  | Defines the top section of a page  |
| `<hgroup>`  | Defines a group of headings  |
| `<mark>`  | Defines the text that should be highlighted  |
| `<nav>`  | Defines navigation to other pages in the site  |
| `<progress>`  | Defines the progress of the task  |
| `<section>`  | Defines the distinct content of a document  |


[Basic structure](./basic-html-structure.html)

[Structure](./html-page-structure.html)

The `<header>` element provides a way of declaring ht header to any area of the webpage.

The `<nav>` element provides users with navigation through the main elements of the web document.

The `<hgroup>` organizes headers and subheaders, allowing the formation of a multi-level heading.

An `<article>` is used to represent a whole and complete composition or entry e.g. magazine or blog post. Content could be redistributed independently of the rest of the page.

The `<section>` element subdivides pages into sections. An article contains zero or more section items.

The `<aside>` element defines any content that doesn't fall within the main content of the page. It doesn't place itself to the side, but just denotes it is aside to the rest of the content.

The `<figcaption>` are semantic elements for adding graphics and figure to webpages.

The `<progress>` element represents the progress of an objective or task. It supports determinate and indeterminate tasks.

 - Determinate for when you know in advance the amount of to i.e you know the starting and end values e.g. downloading a file
 - Can be done like this:
 ```
<p>Our goal is to have 1000 users:</p>
<span>0</span>
<progress value='50' max='1000'></progress>
<span>1000</span>
```
 - Indeterminate tasks when you don't know how long a task will take to complete.
 
The `<mark>` element can easily highlight important information or any text to emphasize.


The new HTML5 semantic elements don't provide eny default behaviour byt provide a stronger semantic structure to your pages.


#### Creating a layout container in HTML

The most common methods of creating a layout in HTML involve using `<div>` & `<table>`. 
The main issue with with using `<div>` elements is their inability to impart standard semantic meaning to each section.
The main issue with `<table>` is the inflexibility to change it.

#### Optimizing for search engines

`<article>` & `<section>` are the main elements used by SEO algorithms to find pages. 
It's important to ensure you have appropriate content in elements as this will make the page more discoverable.

#### Optimizing for screen readers

You should explicitly define the sections of your page by using semantic headings to make it accessible to screen readers.
