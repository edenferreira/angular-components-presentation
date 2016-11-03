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

#### Use with care because it can (problably will) couple the components.

#### It is great to use with trancluded elements.

#### NgModel is a good example of directive designed to be required.
