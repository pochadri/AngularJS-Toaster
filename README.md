AngularJS-Toaster
=================

**AngularJS Toaster** is a AngularJS port of the **toastr** non-blocking notification jQuery library. Requires AngularJS v1.2.0, and animations use CSS3 transformations.

### Current Version 0.4

## Demo
- Simple demo is placed at http://plnkr.co/edit/mejR4h
- Older version 0.3 placed at http://plnkr.co/edit/iaC2NY
- Old version with Angular 1.2.0-rc.2 is placed at http://plnkr.co/edit/iaC2NY
- Old version with Angular 1.1.5 is placed at http://plnkr.co/mVR4P4

## Getting started

1. Link scripts:

```html
<link href="//cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/2.3.2/css/bootstrap.min.css" rel="stylesheet" />
<link href="toaster.css" rel="stylesheet" />
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.2.0/angular.min.js" ></script>
<script src="http://code.angularjs.org/1.2.0/angular-animate.min.js" ></script>
```

2. Add toaster container directive: `<toaster-container> </toaster-container>`

3. Prepare the call of toaster method:

```js
	// Display an info toast with no title
	angular.module('main', ['toaster'])
	.controller('myController', function($scope, toaster) {
	    $scope.pop = function(){
	        toaster.pop('success', "title", "text");
	    };
	});
```

4. Call controller method on button click:

```html
<div ng-controller="myController">
    <button ng-click="pop()">Show a Toaster</button>
</div>
```

### Other Options

```html
// Change display position
<toaster-container toaster-options="{'position-class': 'toast-top-full-width'}"></toaster-container>
```

### Animations
Unlike toastr, this library relies on ngAnimate and CSS3 transformations for animations.
		
## Author
**Jiri Kavulak**

## Credits
Inspired by http://codeseven.github.io/toastr/demo.html.

## Copyright
Copyright © 2013 [Jiri Kavulak](https://twitter.com/jirikavi).

## License 
AngularJS-Toaster is under MIT license - http://www.opensource.org/licenses/mit-license.php

