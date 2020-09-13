---
layout: post
title:  ".call and .apply"
date:   2020-09-13 23:07:00 +0300
categories: JS notes
---
The `apply()` method calls a function with a given `this` value, and `arguments` provided as an `array` (or an array-like object).
{% highlight javascript %}
let arr =[1,2,3];
let max = Math.max.apply(null,arr);
}
{% endhighlight %}

The `call()` method calls a function with a given `this` value and `arguments` provided individually.
{% highlight javascript %}
function Person(firstName, lastName, age, gender, interests){
    this.name = `${firstName}, ${lastName}`;
    this.age = age;
    this.gender = gender;
    this.interests = interests;

    this.bio = () => {
        return `${this.name} is ${this.age} years old. They like ${this.interests}`;
    } 

    this.greeting = () => `Hi! I'm ${this.name}`;    
}
function Student(firstName, lastName, age, gender, interests){
    Person.call(this, firstName, lastName, age, gender, interests);
    this.bio = () => {
        return `Yo! I'm ${this.firstName}.`
    }
}
{% endhighlight %}

