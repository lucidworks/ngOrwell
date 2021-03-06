# ngOrwell
A simple angular observer for AngularJs 1

## Install

You can install this package either with `npm` or with `bower`.

### npm

```shell
npm install ng-orwell
```

Then add `ng-orwell` as a dependency for your app:

```javascript
angular.module('myApp', [require('ng-orwell')]);
```

### bower

```shell
bower install ng-orwell
```

Add a `<script>` to your `index.html`:

```html
<script src="/bower_components/ng-orwell/Orwell.js"></script>
```

Then add `ngOrwell` as a dependency for your app:

```javascript
angular.module('myApp', ['ngOrwell']);
```

## Documentation

Orwell is a simple to use observable for AngularJs 1.

### Including orwell in angular
```javascript
myApp.controller('myController', function(Orwell){

}
```

### Creating a observable

```javascript
Orwell.createObservable(name, content);
```

### Getting an observable
```javascript
Orwell.getObservable(name);
```

### Updating content on an observable

This will call all your observer callbacks who are observing this observable.

```javascript
var myContent = {
  something: 'something'
};
var observable = Orwell.getObservable(name);
observable.setContent(myContent);
```

### Deleting an observable
```javascript
Orwell.deleteObservable(name);
```

### Adding an observer to an observable
```javascript
var observable = Orwell.getObservable(name);
var observer = observable.addObserver(function(content){
  // your callback code here.
})
```

### Destroying an observer
```javascript
var observable = Orwell.getObservable(name);
var observer = observable.addObserver(function(content){
  // your callback code here.
})
$scope.$on('destroy', function(){
  observable.removeObserver(observer);
});
```
## License

[Apache 2.0](LICENSE)
