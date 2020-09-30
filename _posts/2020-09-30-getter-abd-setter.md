---
layout: post
title:  "'use strict'"
date:   2020-09-30 19:09:45 +0300
categories: JS notes
---
Getter and setter is a property for objects. Getter `get` used for read properties and setter `set` used for set up properties.
{% highlight javascript %}
let user = {
    name: "John",
    surname: "Smith",
  
    get fullName() {
      return `${this.name} ${this.surname}`;
    },
  
    set fullName(value) {
      [this.name, this.surname] = value.split(" ");
    }
  };
  
  // set fullName is executed with the given value.
  user.fullName = "Alice Cooper";
  
  alert(user.name); // Alice
  alert(user.surname); // Cooper
  for(let key in user) alert(key); // name, surname

{% endhighlight %}