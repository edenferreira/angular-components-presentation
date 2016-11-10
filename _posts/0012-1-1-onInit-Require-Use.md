---
layout: post
title: Example of $onInit and Require
---

```javascript
function NavigableCtrl() {
  this.$onInit = function() {
    this.navigation.addNewItem(this.name);
  };

  this.$onChanges = function(changes) {
    if (changes.name) {
      this.name = changes.name.currentValue || changes.name.previousValue;
    }
  };

  this.$onDestroy = function() {
    this.navigation.removeItem(this.name);
  };

  this.isActive = function() {
    return this.navigation.isActive(this.name);
  };
}

angular.module('navigation').component('navigable', {
    ...,
    require: {
        navigation: '^^'
    },
    template: '<ng-transclude ng-show="$ctrl.isActive()"></ng-transclude>',
    transclude: true
});
```
