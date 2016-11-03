---
layout: post
title: The Controller
---

```javascript
function Controller() {
    //Parent is ready
    this.$onInit = function () {
    };

    //Some binding changed
    this.$onChanges = function (changes) {
    };

    //on digest
    this.$doCheck = function () {
    };

    //Child is ready
    this.$postLink = function () {
    };

    //Clean up
    this.$onDestroy = function () {
    };
}
```
