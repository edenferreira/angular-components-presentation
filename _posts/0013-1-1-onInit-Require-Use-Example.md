---
layout: post
title: Example of $onInit and Require
---

```html
<navigation>
    <navigable>
        ...content
    </navigable>
    <navigable>
        ...content
    </navigable>
    <navigable>
        ...content
    </navigable>
</navigation>
```
<br>
```html
<navigation>
    <navigable ng-repeat="content in $ctrl.items track by $index">
        ...content
    </navigable>
</navigation>
```
