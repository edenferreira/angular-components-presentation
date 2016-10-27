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
  controller: Controller,
  template: '?',
  templateUrl: '?',
  controllerAs: '$ctrl',
  transclude: false,
  require: {
    ownElement: '',
    ownOrParent: '^',
    onlyParents: '^^'
  },
});
```
