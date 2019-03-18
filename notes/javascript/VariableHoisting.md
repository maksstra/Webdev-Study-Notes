---
group: javascript
layout: post

title: Variable Hoisting
descr: How variable declarations and values are interpreted

resources:
  - title: JS Hoisting
    author: Brandon Morelli
    link: https://www.w3schools.com/js/js_hoisting.asp
    publisher: W3Schools
---

### Variable Hoisting

`var` declarations and value assignments can be placed anywhere on a page. However, the variable declarations are "hoisted" automatically to the top of the page. This means that any `var` doesn't necessarily need to be declared, since it will be declared when it's hoisted. A computer reading this:

{% highlight javascript %}
y = 5;
{% endhighlight %}

This will change to this once it gets hoisted:

{% highlight javascript %}
var y;
y = 5;
{% endhighlight %}

This is why the first code sample, although it looks invalid, actually becomes valid when it becomes the second version. This isn't necessarily a good thing, since it can create unexpected complexity or bugs in the code.

Avoiding this is easier with ES6, since the new variable declarations `let` and `const` **are not hoisted.**
