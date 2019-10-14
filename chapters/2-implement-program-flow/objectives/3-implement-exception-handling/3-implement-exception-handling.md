### Implement exception handling

Structured error hanbdling is achieved in javascript with the *try... catch... finally...* constructs.

Try catch finally handles exceptions that occur during program processing. It enables you to see what kind of error occurred and what to do with it.

The 'catch' block receives an exception object, the try block is then protected against any exceptions it may throw.

Properties available on an exception object:
 - message (description)
 - number (a numeric error code)
 - name ( the name of the exception object)
 
 You can use the exception object to decide what to do with the error.
 
 The finally block will run after the try or catch block is completed.

Each has their own scope.

Exceptions bubble their way up to the calling code until they are handled or the browser receives the exception.

Check for null values and raise an exception if null.