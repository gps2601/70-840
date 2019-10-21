### Create a Web Worker process

Web workers provide a way of developing multithreaded JS applications. Everything in JS is singlethreaded and executed synchronously.

If you require an intensive script to run without effecting performance, web workers might be suitable.

Attached code can show how js is interuppted by intensive processes.

#### Creating a worker process with the Web Worker API

Web Worker API is based on the Javascript messaging framework.

Creates a seperate file that contains a script that will be executed on a separate thread.

Created like so...
```
var webworker = new Worker('workercode.js');
```

Worker object operations
- postMessage (starts the worker process)
- terminate (stops the worker process from continuing)
- onmessage (specifies the function for the worker to call back to when it is completed)
- onerror (specifies a function to call when an error occurs)

webworker.postMessage('')

webWorker.terminate();

webWorker.onmessage = = function(event) { callback function code here} 


#### Web Worker limitations

 - The postMessage allows you to pass data into the worker, but it must be of serializable type e.g. json, XML, it can't be a function
 
 - Number of workers. Can only create a limited amount as they are resource intensive.
 
 - DOM access. They operate on their own global context which means that they don't have access to the DOM.
 
 - There is no limit on how many you can create, but generally a bad idea.