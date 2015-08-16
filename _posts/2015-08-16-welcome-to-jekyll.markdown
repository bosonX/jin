---
layout: post
title:  "MapReduce with MongoDB"
date:   2015-08-16 17:08:23
categories: jekyll update
---
I was working on a e-commerce site lately. As I was processing the raw data from affilitated feeds,
I found out there is an enormous amout of repeated product. However, as my MongoDB instance is already seeded at this point,
there would be impossible to modify the data from the beginning. Map reduce is the tool I come to,

{% highlight javascript %}
db.products.mapreduce(function(){

  return key;
},
function(){

  return {key:key, value:value}
},
{})
{% endhighlight %}
