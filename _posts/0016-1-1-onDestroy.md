---
layout: post
title: $onDestroy
---

```javascript
this.$onDestroy = function () {
    //scope will be destroyed
};
```
<br>

* Called when the component's scope will be destroyed
* Use to clean up the events you bound on the postLink
* Seldom necessary, as you should not be doing dom manipulations directly in the majority of cases
