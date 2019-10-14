### Implement a callback

Callbacks are a design pattern to help you work with multiple threads or execute code asynchronously. 

It will callback the executing code when it is finished with some kind of result.

#### Implementing bidirectional communication with the websocket api

The Websocket api provides bidirectional communication and have simplified the way data can be sent.

Traditional technqiues use http which is heavier, websocket allows connection directly to a server over a socket.

construct using:

var wsConnection = new WebSocket ('ws://.url-to-connect', [optional list of protocols ])

Possible WebSocket readyState:
 - Open
 - Connecting
 - Closing
 - Closed
 
#### Making webpages dynamic with jQuery and AJAX

jQuery is a javascript library that specializes in working with the DOM to make webpages dynamic

You can request data behind the scenes and then use various DOM manipulation techniques to update specific parts of the page instead of doing a page refresh.

Example ajax request:

```
$.ajax({
    url: www.url.com,
    cache: false,
    dataType: "xml",
    success: function(data) {
        function(){
            // do something with the data.
        }
    }
})
```

We can set the cache value to set whether a cache result can be used.

#### Wiring up an event in jQuery

You can wire up an event to an element using jQuery like this:
```
$('#searchButton').click(function() {
    /// code goes here
})
```

You just need to make sure the CSS selector is unique to the elements you want to assign the function to.

#### Implementing a callback with an anonymous function

#### *this* in jQuery

Refers to the objects or set of objects that it finds as a result of a css selector:

```
$("document").ready(
    function() {
        $('#floorDiv').click(function() {
            $('#this).css("background-color", "red");
        })
    }
)
```

This uses *this* to refer to the element that was selected by the calling function.