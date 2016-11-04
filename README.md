# Webplate Tools
The Webplate Tools library is a lightweight set of Javascript methods that facilitate quicker and easier development.

* [Getting Started](#getting-started)
* [Getting Started With NPM](#getting-started-with-npm)
* [Initialization](#initialization)
	* [Defaults](#defaults)
* [Methods](#methods)
	* [Basic Checks](#basic-checks)

## Getting Started
You can either download a copy of the source files or install Webplate Tools via Bower.

```
bower install webplate-tools
```

Next include the required Javascript file.

```html
<body>
	/* Your content goes here */
   <script src="js/webplate-tools.min.js"></script>
</body>
```

## Getting Started With NPM
If you instead wish to use Weplate Tools as a Node module simply install using the following command.

```
npm install webplate-tools
```

Once done require Webplate Tools as you would any other module.

```javascript
var Web = require('webplate-tools');
```

**NOTE:** There are slight differences between the Node and standard library files. These differences should not affect its usage but please report any issue should you find any.

## Initialization
The library is automatically initialized due the Revealing Module Pattern used and is bound to the variable **Web**. This variable acts as the libraries namespace and scopes all methods to this declaration. An example of some method calls can be seen below:

```javascript
// Convert a string to uppercase
var boldName = Web.string.uppercase.all('Chris Humboldt');

// Generate a random integer
var randomNumber = Web.random.integer();
```

Make sure not to overwrite or reassign this variable name to anything else within your project.

#### Defaults
You can overwrite the library options globally by altering the defaults. To do so reference the defaults object property. For now there is only the **log** option with the plan to add more as needed.

```javascript
/*
This allows you to use the Web.log() method throughout your project
and when deploying to production, assign this a value of "false" to
prevent any forgot console.log message from displaying.
*/
Web.defaults.log = false;
```

## Methods
Below is a list of the all the methods, the default values and the options.
