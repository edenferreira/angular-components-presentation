---
layout: post
title: The API - Callbacks
---

## Callbacks syntax

#### On the component

```javascript
function Controller() {
  this.whenIDoSomething = function (someValue) {
    this.onCallback({
      $event: {
        someValue: someValue
      }
    });
  }
}
```

#### On the component listening

```html
  <component on-callback="$ctrl.handleCallback($event)"></component>
```

```javascript
function Controller() {
  this.handleCallback = function (event) {
    doSomething(event.someValue);
  };
}
```
