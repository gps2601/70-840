### Implemnt HTML5 APIs

Javascript APIs now ofer more functionality that allow more data to be stored locally throuh the Web Storage API.
They allow offline work via the AppCache API.
The geolocation API provide methods to work with global positioning.

#### Storage API

Two forms of web storage exist: local and session storage.

Local storage is persistent and is available after the users closes the browser.

Session storage is only available during the current session of the browser. If the browser is closed, this storage is lost.

To access use the *localStorage object* or the *sessionStorage object*.

They provide exactly the same API. 

The benefit of web storage vs cookies is that the data remains local and is not passed back and forth between the server and client.

To store more complex objects you can convert them using JSON (serialize into JSON), give it a key in the web storage.
e.g.

```
var customr = new Object();
customer.firstname = "geof";
customer.lastName = "smith";
localStorage.setItem("cart1", JSON.stringify(customer))
```

#### AppCache API

AppCache makes content and webpages available when a web application is in offline mode.

Two components make up AppCache API, the manifest and the JS api to support it.

##### Using AppCache manifest

Specify that a page should be available for offline by adding attribute to HTML element

```
<html manifest="webApp.appcache">
...
</html>
```

This points to the manifest file.

The application cache manifest file must list each file required to be stored for offline use.

It is split into 2 sections:

 - Cache (all items that must be cached)
 - Network (required network resources, when the app is in offline mode it wont reach out for anything unless listed here)
 - Fallback (Provides fallback instructions if something isn't available, e.g. render login.html)
 
 ##### Using AppCache API
 
 App cache is available as a global object.
 
 ```
 Access using:
 var appCache = window.applicationCache;
 ```
 
 One of the more useful things you can do is verify the app cache status, it can be...
 
 | Status | Description |
 | ------------- | ------------- |
 | Uncached | the application isn't associated with an app manifest |
 | idle | most up to date copy of the cache is being used  |
 | checking | The application manifest is being checked for updates |
 | downloading | Resources in manifest are being downloaded |
 | updateReady | the resources listed in the manifest have been successfully downloaded |
 | obsolete | The menifest can no longer be downloaded so will be deleted. |
 
 When you know the status of the cache, you can call the two methods:
  
  - swapCache (cache can be replaced with a newer version)
  - updated (update the cache if an update is available.)
  
e.g. Call update, when the status of 'status' is 'updateReady' then you can swap the cache.


#### Geolocation API

You can get a reference to the geolocation api from the *window.navigator* property.
e.g.

```
var geolocator = window.navigator.geolocation;
```

It provides 3 key methods to interact with:
 
 - getCurrentPosition()
 - watchPosition()
 - clearWatch()
 
*getCurrentPosition* can take three arguments:

```
getCurrentPositoin(positionCallBack, positionErrorCallback, positionOptions)
```

Options

| Property | Description |
| ------------- | ------------- |
| enableHighAccuracy | more resource intensive but gets as close as possible |
| timeout | how long it takes to complete  |
| maximumAge | sets the allowable ages of a cached value if used |
  

*watchPosition* continuosly polls for new location and triggers the callback function each time location changes.