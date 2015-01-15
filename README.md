# angular-window-manager

It's an angular directive inspired in the work of Ramón Lamana on Ventus https://github.com/rlamana/Ventus

You can find the this project's develeopment environment  in this other github project: https://github.com/sinmsinm/ng-window-manager . That was only has release publication purposes.


###Install
Install the dependency with bower
```
bower install angular-window-manager
```

###Use in your project
Include the directive script and css in your project.
```  
  <link rel="stylesheet" type="text/css" href="path_to_library/window-manager.css" />
  <script type="text/javascript" src="path to library/angular-window-manager.js" />
  
```
Inject the `ngWindowManager` module as your app dependency
```
angular.module('wmExampleApp', ['ngWindowManager']);
```
Use the element
```
	  <wmwindow title="Good title" options="{{options}}" > My window content {{something_from_scope}} </wmwindow>
``` 
You can also have multiple windows under an element from an array
```
	  <wmwindow title="{{article.title}}" ng-repeat="article in articles"  > <p>{{article.body}} <p></wmwindow>
``` 
### Parameters
* _title_: Window title
* _close_: Function executed when window is closed
* _maximize_: Function executed when window is maximized
* _restore_: Function executed when a window is restored
* _options_: Additional options to customize the window, see below. 

### Options 
You can pass some options to a window to customize the behaviour:
 * _position_ {x, y} : Initial position of the window when it's created  
 * _size_ {width, height}: Initial size of the window when it's created
 * _maximizeTo_: Element id where the windows will be maximized (when user push the button) 
 * _windowContainer_: Element id where windows can move over. If not provided parent element would be the windowContainer.

Options example:

```
$scope.options = {
		position: {x: 120, y:320},
		size: {width: 300, height:300},
		maximizeTo: 'contentArea',
		windowContainer: 'myMoveZone'
	};
```

