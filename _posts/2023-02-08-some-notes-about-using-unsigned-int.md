---
title:  "Some notes about using unsigned int"
layout: post
tags: C++
---

The following `for` loop will never stop

{% highlight cpp %}
for (unsigned i = 5; i >= 0; --i) {
    std::cout << i << std::endl;
}
{% endhighlight %}

The reason is that when `i` is `0`, the result of `i-1` is `4294967295 (2^32-1)` since `i` is `unsigned int`.