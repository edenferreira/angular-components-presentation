---
layout: post
title: The API
---
## Bindings

```javascript
bindings: {
  //Traditional angular with watch on parent and child
  twoWay: '=',
  //New binding with watch only on parent
  oneWay: '<',
  //Traditional angular that passes the value as is
  attributes: '@',
  //Traditional angular that can be subscribed to listen to events
  callback: '&'
}
```
