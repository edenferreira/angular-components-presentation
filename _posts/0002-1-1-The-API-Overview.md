---
layout: post
title: The API
---
```javascript
angular('module').component('component', {
  bindings: {
    oneWay: '<',
    twoWay: '=',
    attributes: '@',
    callback: '&'
  },
  require: {
    ownElement: '',
    ownOrParent: '^',
    onlyParents: '^^'
  },
  controller: Controller,
  template: '?',
  templateUrl: '?',
  controllerAs: '$ctrl',
  transclude: false,
});
```
