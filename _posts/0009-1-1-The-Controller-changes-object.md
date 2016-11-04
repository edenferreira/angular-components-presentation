---
layout: post
title: The Controller
---

## Changes Object

```javascript
this.$onChanges = function (changes) {
    if (changes.binding.isFirstChange()) {
        this.infra = doSomeNecessaryFirstCalculations();
        this.amountChanged = changes.binding.currentValue;
    } else {
        this.amountChanged = changes.binding.currentValue - changes.binding.previousValue;
    }
};
```

#### The object contains only keys of the bindings that changed, so to test if something changed you can:
```javascript
if (changes.binding) {
    this.another = bindginsDidChange(changes.binding.currentValue);
}
```
<br>

* Remember to think about the case where the binding is undefined, the first time, and the others.
