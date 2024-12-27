---
icon: arrows-rotate-reverse
---

# Dynamic URL's

* Dynamic URLs allow you to pass parameters directly in the URL to handle requests for specific data.
* For example, instead of having separate URLs for each blog post, like `/blog/post1`, `/blog/post2`, etc., you can use a dynamic URL such as `/blog/post/<id>/`.
* Here, `<id>` acts as a placeholder that Django dynamically replaces with the actual value when handling the request.

**Syntax**

```python
path('path_name/<parameter:id_name>', view_function, name='route_name')
```

**Example**

![](https://i.imgur.com/Cy0mAx5.png)

![](https://i.imgur.com/y9aBUx7.png)

When you do the domain `http://127.0.0.1:8000/post/10` , you could see the webpage as below.

![](https://i.imgur.com/FBY3v28.png)

Similarly, When you do the domain `http://127.0.0.1:8000/post/43` , you could see the webpage as below.

![](https://i.imgur.com/JRPIDll.png)

***

**Exercise**

> Exercise: Create an another dynamic URL using string instead of integers

![](https://i.imgur.com/pgq7WKs.png)

![](https://i.imgur.com/afmaLjj.png)

So, now if i look into the link `http://127.0.0.1:8000/delivery/chennai`, my webpage would look something like this.

![](https://i.imgur.com/a5nbWDq.png)

***

#### Built-in Converters for Dynamic URLs

Django provides several converters for dynamic URLs:

| Converter | Description                                                 | Example URL                                   |
| --------- | ----------------------------------------------------------- | --------------------------------------------- |
| `<int>`   | Matches integers                                            | `/post/42/`                                   |
| `<str>`   | Matches any string (default)                                | `/post/hello/`                                |
| `<slug>`  | Matches a slug (letters, numbers, hyphens, and underscores) | `/post/my-post/`                              |
| `<uuid>`  | Matches a UUID                                              | `/post/550e8400-e29b-41d4-a716-446655440000/` |
| `<path>`  | Matches a string including `/`                              | `/post/my/path/`                              |

***
