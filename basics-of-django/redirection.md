---
icon: reflect-horizontal
---

# Redirection

**What is redirection?**

* In Django, **redirection** refers to sending a user from one URL to another.
* It is commonly used to guide users to a different page after completing an action, such as submitting a form or accessing a deprecated URL.

**How to perform redirection?**

You would need to import `redirect()` for the redirection. You can import this as follows.

```python
from django.shortcuts import redirect
```

![](https://i.imgur.com/W9Y2dRT.png)

![](https://i.imgur.com/mD6TgtO.png)

> When you visit `http://127.0.0.1:8000/old_url`, you would be redirected to `http://127.0.0.1:8000/new_url` and the output would be as follows.

![](https://i.imgur.com/sViCzRm.png)

***
