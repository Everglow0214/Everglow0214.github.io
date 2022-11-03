---
title:  "Detect contours in a 3D NumPy array"
layout: post
tags: Python NumPy
---

The following mophological method can be used to detect the contours in a 3D NumPy array.

{% highlight python %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')

import numpy as np
from skimage import morphology

arr = np.zeros((5,5,5))
arr[1:4, 1:4, 1:4] = 1

dila = morphology.dilation(arr!=1, morphology.cube(3))

res = np.argwhere((a==1) & (dila==True))
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}
