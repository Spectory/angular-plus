# angular-plus

## Angular awesome-if

```html
<include-directive 
  awesome-if="should_show" 
  template="platforms/connections"> <!-- rails template -->
</include-directive>
```

awesome-if is a directive that behaves like ng-show, but removes the dom while
not shown(i.e detaches it). It's the same as ng-if, but without the overhead of recompiling largs dom each time.
It's not recreated and as such, to be aware that your controller has been reshown use the following:

```javascript
  $scope.$parent.restart = function () {
    $scope.init();
  };

  $scope.$parent.stop = function () {
    ...
  };  
```


