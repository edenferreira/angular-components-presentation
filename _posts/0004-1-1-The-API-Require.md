---
layout: post
title: The API - Require
---

## Require

```javascript
require: {
    //For when you require ngModel for example
    ownElement: '',
    //For when you want to create tabs pane
    ownOrParent: '^',
    //Something crazy, or maybe a dashboard
    onlyParents: '^^',
    //Ever other fails if the controller is not present
    optional: '?^'
}
```
<br><br><br>

> ### Use with care because it can couple the component to another

> ### It is great to use with trancluded elements

> ### Never seen good use with option parents
