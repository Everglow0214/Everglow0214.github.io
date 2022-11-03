---
title:  "Extract contours in a 3D NumPy array"
layout: post
tags: Python NumPy
---

The following mophological method can be used to extract the contours in a 3D NumPy array. The idea comes from [here](https://stackoverflow.com/questions/51696326/extracting-boundary-of-a-numpy-array).

{% highlight python %}
import numpy as np
from skimage import morphology

arr = np.zeros((5,5,5))
arr[1:4, 1:4, 1:4] = 1

dila = morphology.dilation(arr!=1, morphology.cube(3))

res = np.argwhere((a==1) & (dila==True)) # indices of the contours
{% endhighlight %}

Note that in this case, if all elements of `arr` is 1, the result `res` will be empty.
