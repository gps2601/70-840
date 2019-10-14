### Establish scope of objects and variables

##### Establishing the lifetime of variables and scope

- Scope of objects

##### Avoiding using the global namespace

The global namespace is where lal the native javascript libraries live. It is available to all code within an application session.

It should be avoided due to the potential for naming conflicts.

You can create your own namespace to avoid this problem.

##### Leveraging the *this* keyword.

The keyword *this* is a special term that allows Javascript developers to reference the containing object directly.

```
<script>
    this.navigator.geolocation
    window.onload = function () {
        // this here would reference the window object
        document.getElementById("aDiv").onclick = function(){
            // here 'this' refers to the DIV element
        }
    }
</script>
```