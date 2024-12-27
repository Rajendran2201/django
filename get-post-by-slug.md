---
icon: plug-circle-check
---

# Get post by slug

**Basic Retrieval in Views**

```python
# views.py
from django.shortcuts import get_object_or_404
from .models import Post

def post_detail(request, slug):
    # Method 1: Simple retrieval with 404 if not found
    post = get_object_or_404(Post, slug=slug)
    
    return render(request, 'blog/post_detail.html', {'post': post})
```

![](https://i.imgur.com/LK6u1G8.png)

![](https://i.imgur.com/beJI6a6.png)

![](https://i.imgur.com/0k8obAM.png)

### An error occured

```bash

Internal Server Error: /
```

This was because, I have changed the name as `post_id` but forgot to change the data type.

![](https://i.imgur.com/eiSfnKx.png)

Now, it should work fine.

![](https://i.imgur.com/NHnGgdk.jpeg)

***
