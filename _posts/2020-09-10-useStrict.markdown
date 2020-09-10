---
layout: post
title:  "'use strict'"
date:   2020-09-10 12:39:45 +0300
categories: JS notes
---
'use strick' allow to use strict version of javascript. Let's check what difference beetwin funcion with and without use strict with `this` in function.
With 'use strict' `this` does't have context:
{% highlight javascript %}
'use strict'
function strict(){
    console.log(this);
}
{% endhighlight %}

And without 'use strict' `this` have context:
{% highlight javascript %}
function regular(){
    console.log(this);
}
{% endhighlight %}