### Objective 3.3 - Consume Data

The two data formats commonly used in data transmission are JSON and XML.

JSON is unstructured whereas XML is structured.

XML has named tags and opening and closing tags, whereas JSON uses key value pairs in string format.

#### Using the XMLHttpRequest Object

Calls to a web service can be made using the XMLHttpRequest object.

Both synchronous and asynchronous calls are supported.



#####The following are events of the XMLHttpRequest object

| Events  | Description |
| ------------- | ------------- |
| Onreadystatechange | event handler for when the state of request has change, used for asynchronous calls |
| Ontimeout | Event handler for when the request can't be completed |

#####The following are methods of the XMLHttpRequest object

| Method  | Description |
| ------------- | ------------- |
| Abort | Cancel request  |
| getAllResponseHeaders | list all the response headers |
| getResponseHeader | gets a specific header |
| Send | Makes the HTTP request and receives the response |
| setRequestHeader | sets a customer http header to request |
| Open | Sets properties for the request |

#####The following are properties of the XMLHttpRequest object

| Property  | Description |
| ------------- | ------------- |
| readyState | gets the current state of the object |
| Response | gets the response returned from the server |
| responseBody | gets the response body as an array of bytes |
| responseText | gets the response as a string |
| responseType | gets the data type with the response, e.g. blob, text, array-buffer |
| responseXML | gets th e response body as an XML DOM object |
| Status | gets the http status code of the request |
| statusText | gets the HTTP text to correspond the Status code |
| Timeout | sets the timeout threshold for the request |
| withCredentials | specifies whether a request should include user credentials |

#####The following are parameters passed to the XMLHttpRequest.open() method

| Parameter  | Description |
| ------------- | ------------- |
| Method | The HTTP method used e.g. GET or POST |
| URL | Where to make the request to |
| async | a boolean to indicate if the request is asynchronous, if true event handler needs to be set for onreadystatechanged |
| User name | A user name if the destination requires one |
| passwrod | a password if the destination requires one |


By default, the timeout on a request is zero, that is, it will never timeout.

A timeout should be set, and a function written ontimout




