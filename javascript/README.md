JavaScript
========================
## Console
To concat variables in console.log you can separate them with comma.Like below:
~~~javascript
var foo = "bar";
console.log("Hello to",foo);
~~~
output : ```Hello to bar```

It will automatically add space betweens variables and strings!

### Placeholders
Usin % in strings concatenation is called placeholders.
~~~javascript
var foo = "bar";
console.log("Hello to %",foo);
~~~
output : ```Hello to bar```

## DOM
DOM stands for Document Object Model.It is an object oriented representation of HTML or XML.

## Window
### window.alert
Shorthand of window.alert is ```alert```.Because window is a global object.
Alert works a modal prompt.It meand it doesn't work until the prompt is answered.

### prompt
It will get an input from user in window alert.Example:
~~~javascript
var value = prompt("Give us a value.")
~~~
If user doesn't accept to return a value:
in safari -> empty string
in other browsers -> null value

### window.confirm
It will show a ok cancle screen to ask from user to have some behaviour or not.

### Difference of undefined and null
Term `undefined` means that the variable is decalred but no value is assinged whereas `null` is a value for a variable.

By the way `undefined` is a type and `null` is an object.
