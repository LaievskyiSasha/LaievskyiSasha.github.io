---
layout: post
title:  "'use strict'"
date:   2020-09-10 12:39:45 +0300
categories: JS notes
---
`'use strict'` allows us to use a strict version of javascript. Let's check the difference with and without '`use strict'` in a function that has `this` in it.
With `'use strict'` `this` does't have context:
{% highlight javascript %}
'use strict'
function strict(){
    console.log(this);
}
{% endhighlight %}

And without `'use strict'` `this` has context:
{% highlight javascript %}
function regular(){
    console.log(this);
}
{% endhighlight %}