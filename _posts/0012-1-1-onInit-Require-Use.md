---
layout: post
title: Example of $onInit and Require
---

```javascript
function NavigableCtrl() {
    var ownId;

    this.$onInit = function () {
        ownId = this.navigation.addNewItem();
    };

    this.isActive = function () {
        return this.navigation.isActive(ownId);
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
