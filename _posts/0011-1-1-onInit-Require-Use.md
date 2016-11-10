---
layout: post
title: Example of $onInit and Require
---

```javascript
 function NavigationCtrl() {
   var items = [];
   var activeName;

   this.addNewItem = function(name) {
     items.push(name);
     if (isFirstItem(items)) {
       this.activate(name);
     }
   };

   this.activate = function(name) {
     activeName = name;
     this.onActiveChange({
       $event: {
         name: activeName
       }
     });
   };

   this.isActive = function(name) {
     return activeName === name;
   };

   this.navigables = function() {
     return items;
   };

   function isFirstItem(items) {
     return items.length === 1;
   }
 }

angular.module('navigation').component('navigation', {
    ...,
    template: '{code-to-change-the-active...}<ng-transclude></ng-transclude>',
    transclude: true
});
```
