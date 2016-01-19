# ngOrwell
A simple angular observer for AngularJs 1

## Install

You can install this package either with `npm` or with `bower`.

### npm

```shell
npm install ngOrwell
```

Then add `ngOrwell` as a dependency for your app:

```javascript
angular.module('myApp', [require('ngOrwell')]);
```

### bower

```shell
bower install ngOrwell
```

Add a `<script>` to your `index.html`:

```html
<script src="/bower_components/ng-orwell/Orwell.js"></script>
```

Then add `lw.orwell` as a dependency for your app:

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

### Deleting an observable
```javascript
Orwell.deleteObservable(name);
```

### Adding an observer to an observable

### Destroying an observer

### Updating the observable
