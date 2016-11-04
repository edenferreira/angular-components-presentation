---
layout: post
title: Example of $onInit and Require
---

```javascript
function NavigationCtrl() {
    var items = [],
        activeIndex;

    this.addNewItem = function () {
        var index = items.length;
        items.push(index);
        if (items.length === 1) {
            activeIndex = index;
        }
        return index;
    };

    this.activate = function (index) {
        activateIndex = index;
    }

    this.isActive = function (index) {
        return activeIndex === index;
    };
}

angular.module('navigation').component('navigation', {
    ...,
    template: '{code-to-change-the-active...}<ng-transclude></ng-transclude>',
    transclude: true
});
```
