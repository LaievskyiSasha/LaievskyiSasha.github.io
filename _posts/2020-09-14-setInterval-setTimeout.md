---
layout: post
title:  "setInterval() and setTimeout()"
date:   2020-09-14 01:01:01 +0300
categories: JS notes
---
`setTimeout()` runs a `function` after delay.
{% highlight javascript %}
let timerId = setTimeout(func|code, [delay], [arg1], [arg2], ...)
{% endhighlight %}

{% highlight javascript %}
function testSetTimeout(){
    return 'function run after delay';
}
setTimeout(testSetTimeout, 10000);
{% endhighlight %}

`setInterval()` runs a `function` after interval and repeating with interval.
{% highlight javascript %}
let timerId = setInterval(func|code, [delay], [arg1], [arg2], ...)
{% endhighlight %}

{% highlight javascript %}
function testSetInterval(){
    return 'function will runs after interval';
}
let intervalId = setInterval(testSetInterval, 1000,)
{% endhighlight %}

To stop execution of setTimeout and setInterval we have the methods `clearTimeout(id)` and `clearInterval(id)`.