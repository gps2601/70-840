### Objective 3.1 - Validate user input by using HTML5 elements

#### Choosing input controls

HTML5 provides a wide assortment of controls to make capturing user input simple.

HTML5 tag `<input>` denotes user input, exceptions are button and textarea.

#### HTML5 Input element types

| HTML5 Input type  | Description |
| ------------- | ------------- |
| color | provides a color picker  |
| date | provides a date picker |
| datetime | provides a date and time picker |
| month | provides a numeric month and year |
| week | numeric week and year |
| time | select a time of day |
| number | forces input to be numeric |
| Range | values within a range using a slider bar |
| tel | formats as a phone number |
| url | require to be a formatted url |
| Radio | select a single value in group |
| Checkbox | select multiple values in group |
| Password | glyphs entered characters |
| Button | performs an action such as running a script |
| Reset | Resets all html elements within a form |
| Submit | Posts the form data to a destination |


##### Using text and textarea

Text and textarea are more flexible, allows users to enter any text they want into a textbox.
Textarea allows multiline entry.

##### Input buttons

Three types:
- submit (submits the form - default text of submit)
- resets the form (default values - default text of reset)
- button (describe your own behaviour)

##### Button buttons

Also offers the submit and reset but doesn't provide text on buttons, everything else must be specified in html.
You can embed images by having a nested `<img>` tag.


#### Implementing content attributes

##### Making controls read-only

You can make an item uneditable using the readonly attribute.

##### Providing a spellchecker

You can pass the attribute spellcheck='true' to turn on spellchecking in an input element.

##### Specifying a pattern

You can specify a pattern attribute pattern='' to match a regex in the input field.

E.g.

```
<input type='text' title="only .com and .ca are permitted." pattern="^[a-zA-Z0-9\-\.(com|ca)$]"/>
```

##### Placeholder attribute

Prompts user as to what is expected in the field

##### Required attribute

Makes sure the is completed before being submitted.