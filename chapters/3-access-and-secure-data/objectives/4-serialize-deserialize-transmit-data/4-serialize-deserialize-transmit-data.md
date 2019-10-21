### Objective 3.4 - Serialize, deserialize, and transmit data.

The concept of converting data from one form to another is called serialization and deserialization.

With serialization, the data is put into a format for transmission.
With deserialization, the transmitted data is converted into something that can be worked with, e.g. a custom object.

Also, applications can work with binary data, the data needs to be serialized into a binary stream to achieve this.

#### Sending data by using XMLHttpRequest

To send data, the XMLHttpRequest.send method must have data sent to it.
E.g.

```
var xmlData = 'some data'
var xReq = new XMLHttpRequest();
xReq.open("POST", "www.someurl.co.uk", false);
xReq.send(xmlData);
```

#### Serializing and deserializing JSON data

The browser provides native support when working with JSON and XML. The JSON obvject is available for converting a JSON string to and object.

E.g.

```
var person = {
    Firstname: "Rick",
    HairColor: "Brown"
}
var jsonPerson = JSON.stringify(person)
```

The person has been serialized into a JSON string that can be sent and understood by an endpointr.

To interpret this as a response you can do the following.

```
req.open("GET", "MyData.json", false);
req.send(null);
var jsonPerson = JSON.parse(req.responseText);
```

#### Serializing and deserializing binary data

Capturing image data follows as similar technique as above, except the responsetype property must not be set to *Blob*.

E.g.

```
var xReq = new XMLHttpRequest();
xReq.open("GET","orange.jpg", false);
xReq.responseType = 'blob';
xReq.send(null);
var blob = xReq.response;
document.getElemeentById("Result").src = URL.createObjectURL(blob);
```
By setting the response property, this allows the blob content to be deserialized from the response.
The blob is passed to URL.createObjectUrl method which gives the img element a URL linking to the Blob, allowing it to be displayed in the browser.

#### Using the Form.Submit method

The form element contains an action attribute that tels the form where to submit the data, this submits the whole html page back to the server for processing.

Another way to do this is to hook up the forms submit even and handle the submission through Javascript.

This will post its data to the server page in action for processing.
```
<form id="signupForm" action="processSignUp.aspx">
</form>
```

We can instead wire up the event in Javascript.

```
$("document").ready(function() {
    $("form").submit(function() {
    })
});
```

And this way we can decide what to send in the form and how.

#### Using the jQuery.serialize method

jQuery provides a way to encode data from a HTML form by traversing the form thats passed into it and looking for input boxes to construct a query string.


This code is written like this:

```
$("form").submit(function() {
    var qString = $(this).serialize();
    alert(qString);
    $.ajax({
        url: 'a.url.com',
        type: "POST",
        data: qString,
        succes: function(r) {}
      
    });;
    return false;
}
```

Only valid input fields are serialized into the encoded string.

For radio buttons you would need to specify a value to differentiate in the query string.

