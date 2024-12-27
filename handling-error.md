---
icon: message-exclamation
---

# handling Error

When we try to access an invalid webpage, it returns an error as below.

![](https://i.imgur.com/Pv4urEO.png)

To handle this, we have to include the potentially error causing block of code in `try...except` block.

```python

from django.http import Http404

try:

# getting data by id from the model

post = Post.objects.get(pk=post_id)

except Post.DoesNotExist:

raise Http404("The Post Doesn't Exist")
```

![](https://i.imgur.com/OELWutd.png)

We have set the `DEBUG` option as `False`, so the custom error page will be displayed.

![](https://i.imgur.com/iWoRbmV.png)

![](https://i.imgur.com/770mAh2.png)

Incase if we set, `DEBUG = True`, the we'll receive our error message.

![](https://i.imgur.com/srHboZ4.png)

![](https://i.imgur.com/79gqEpj.png)

***
