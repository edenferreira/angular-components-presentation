---
layout: post
title: $doCheck
---

```javascript
//In case you're confused
this.$doCheck = function () {
};
```
<br>

* Called on every digest, so be careful.
* Changes made inside of it can trigger other digest cycles, so be very careful.
* Over use or costly computations inside it can easily hurt performace, so be extremely careful.
