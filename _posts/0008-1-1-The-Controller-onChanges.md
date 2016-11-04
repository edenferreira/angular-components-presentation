---
layout: post
title: The Controller - $onChanges
---

## $onChanges

```javascript
this.$onChanges = function (changes) {
    if (changes.binding) {
        this.other = doSomething(changes.binding.currentValue);
    }
};
```
<br><br><br>

* This is the more important, and will be the most used of all hooks.

* Is called every time a one way (<) or unparsed(@) binding change.

* Will *NOT* be called for two way (=) binding

* The change is checked with simple equality, AKA ===.
