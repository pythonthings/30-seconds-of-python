---
title: group_by
tags: list,object,beginner
---

Groups the elements of a list based on the given function.

Use `map()` and `fn` to map the values of the list to the keys of an object.
Use list comprehension to map each element to the appropriate `key`.

```py
def group_by(lst, fn):
    return {key : [el for el in lst if fn(el) == key] for key in map(fn,lst)}
```

```py
import math
group_by([6.1, 4.2, 6.3], math.floor) # {4: [4.2], 6: [6.1, 6.3]}
group_by(['one', 'two', 'three'], len) # {3: ['one', 'two'], 5: ['three']}
```
