---
layout: post
title: Post dos
subtitle: Subtitol ok
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [test]
comments: true
mathjax: true
math: true
author: Bill Smith
---

{: .box-success}
Si aixo esta be flipo heavy

**Aqui posa noseque en negreta**

## I aqui un atre titul

[This is a link to a different site](https://deanattali.com/) and [this is a link to a section inside this page](#local-urls).

Here's a table:

| Number | Next number | Previous number |
| :------ |:--- | :--- |
| Five | Six | Four |
| Ten | Eleven | Nine |
| Seven | Eight | Six |
| Two | Three | One |


How about a yummy crepe?

![Crepe](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRqaBhunyxT_z5UsaajDEavzVGIUu-C230yWLVDEsf4_gXDE4qPLdidItz7&s=10)

It can also be centered!

![Crepe](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRqaBhunyxT_z5UsaajDEavzVGIUu-C230yWLVDEsf4_gXDE4qPLdidItz7&s=10){: .mx-auto.d-block :}

Here's a code chunk:

~~~
var foo = function(x) {
  return(x + 5);
}
foo(3)
~~~

And here is the same code with syntax highlighting:

```javascript
var foo = function(x) {
  return(x + 5);
}
foo(3)
```


And here is the same code yet again but with line numbers:

{% highlight javascript linenos %}
var foo = function(x) {
  return(x + 5);
}
foo(3)
{% endhighlight %}

## Boxes
You can add notification, warning and error boxes like this:

### Notification

{: .box-note}
**Note:** This is a notification box.

### Warning

{: .box-warning}
**Warning:** This is a warning box.

### Error

{: .box-error}
**Error:** This is an error box.

## Local URLs in project sites {#local-urls}

When hosting a *project site* on GitHub Pages (for example, `https://USERNAME.github.io/MyProject`), URLs that begin with `/` and refer to local files may not work correctly due to how the root URL (`/`) is interpreted by GitHub Pages. You can read more about it [in the FAQ](https://beautifuljekyll.com/faq/#links-in-project-page). To demonstrate the issue, the following local image will be broken **if your site is a project site:**

![Crepe](/images/crepe.jpg)

If the above image is broken, then you'll need to follow the instructions [in the FAQ](https://beautifuljekyll.com/faq/#links-in-project-page). Here is proof that it can be fixed:

![Crepe]({{ '/images/crepe.jpg' | relative_url }})

This is also incorrect:

![Crepe]('/images/crepe.jpg')
