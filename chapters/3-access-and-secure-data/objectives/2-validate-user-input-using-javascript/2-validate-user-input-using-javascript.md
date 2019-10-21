### Objective 3.2 - Validate user input using Javascript

Javscript provides additional functionality not available in HTML5 elements.

It can also be used to protect against malicious code injection.

#### Evaluating regular expressions

You can use a pattern attribute in HTML5 elements to match a regex for an input field, but in some situations this may not be suitable.

| Regex symbol  | Description |
| ------------- | ------------- |
| ^ | denotes the beginning of a string  |
| $ | denotes the end of a string  |
| . | indicates to match on any character |
| [A-Z] | Match any alphabetic uppercase letters  |
| \d | Match any numeric character |
| + | Preceding character/character set must match at least one |
| * | The preceding set might match at least once |
| [^] |  The carat when combined with a character set denotes a negation |
| ? | The preceding character is optional |
| \w | Indicates to match a word consisting off any alphanumeric including underscore |
| \ | Escape character, match on any literal |
| \s | Match on any space character |


^[A-Z.a-z] ..... Carat indicates start of a string, the next character must be alphanumeric 

^[A-Z.a-z]\d ..... The next character must be a numeric (can also use [0-9])

^[A-Z.a-z]\d\s ..... The next character must be a space

^[A-Z.a-z]\d\s* ..... Now the space is optional ( but now loads of spaces could be passed)

^[A-Z.a-z]\d\s{1} ..... Now 1 space is required (back to square one)

^[A-Z.a-z]\d[\s{1}]? ..... Using th question mark, the preceding space is now optional


#### Evaluating regular expressions in Javascript

Regular expressions in Javascript are  objects, they can bve created and provide methods to evaluate strings.

To create in JS, you have to surround them with /*Insert regex here*/.

You can use .test to return true or false if the regex matches.

You can use .exec to return as a string array  or null if no match is made

#### Validating data with built in functions

- isNaN(value) provides a way to check if the value isn't a number
- isFinite(value) provides a way to check if the value is a finite number


#### Preventing code injection

 - Don't use the eval() function, this runs the javascript code passed to it, dont use this to evaluate code you dont have 100% control of.


#### iFrames

Sandbox should always be added to iFrames to restrict what data can be passed.

| iFrame sandbox attribute  | Description |
| ------------- | ------------- |
| "" | Applies all restrictions, this is the most secure.  |
| allow-same-origin | iFrame content is trated as being from the same origin as containing HTML document|
| allow-top-navigation | iFrame content can load content from the containing HTML document |
| allow-forms | iFrame can submit forms |
| allow-scripts | iFrame can run scripts |


