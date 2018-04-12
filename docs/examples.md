# Examples
This detects wherether the "Cancel" or "OK" button has been pressed:
```js
$confirm('click a button', function (ok){
  if (ok) {
    $alert('You pressed OK.')
  } else {
    $alert('You pressed Cancel.')
  }
});
// note: this works not just on $confirm, but on $alert, $alert.info/error, even $prompt and $window.form (which we’ll get on to later)
```

You can open an application from $fs.utils.getMenuOpenWith() by using the action function in the object of each application:
```js
$fs.utils.getMenuOpenWith('/a/trash/trash.jpg')[0].action();
// Image Viewer is the first object in the array because it’s an image so execute that using the action function
```

How would I get the text inputted into a prompt?
```js
$prompt('Please insert your credit card number.', '', function(ok, text) {
  if (ok) {
    $alert(text)
  }
});
```

How to use $window properly:

```js
// put the $window in a variable
var myWindow = $window('url-or-whatever'); //right, returns an object with things to interact with the window or just information ect

/* you can use it like you would with $window, except $window.current is whatever you named the variable and to make the window the active window, just use the active() function
