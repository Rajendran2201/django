---
icon: file-code
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Returning HTML

If you wish to augment HTML files/templates to the app, you have to store them all in one folder. For this, I have saved my `index.html` file at `myapp/blog/templates` location.

![](https://i.imgur.com/fKYFGsy.png)

Now, Our task is to display this template in the root URL. First you have to import `render`.

```python
from django.shortcuts import render

render(request, template_path)
```

### Adding a template

In the `views.py` file, link the template to `index` function as it is set to the root URL path.

![](https://i.imgur.com/KVRiUUf.png)

Now, go to `http://127.0.0.1:8000/`. Here, you could view the template has been insert.

![](https://i.imgur.com/Ed9xsQ4.png)

***

### Exercise

Now, we'll try to add one more template `detail.html` to the project

![](https://i.imgur.com/fk6yXtE.png)

When I visit `http://127.0.0.1:8000/post/10`, I could view the detail webpage along with its template.

![](https://i.imgur.com/O2WD6Wc.png)

***
