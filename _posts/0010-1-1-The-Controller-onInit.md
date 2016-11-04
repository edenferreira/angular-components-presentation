---
layout: post
title: The Controller
---

## $onInit

```javascript
    var ownId;

    this.$onInit = function () {
         ownId = this.parentRequiredIsReady.notifyWasAdded();
    };
```

* $onInit is guaranteed to be called after the parent controller was create and had its own $onInit called.
* It's the second hook called on the component initiation, *AFTER* $onChanges
* It goes hand in hand with "require".
