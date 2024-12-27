---
icon: brackets-curly
---

# URL Tag and Dynamic URLs

URL tags are used in Django templates to generate URLs dynamically. The most commonly used URL tag in Django is the `<div data-gb-custom-block data-tag="url"></div>` tag, which is used to reverse resolve URLs by their view names.

**Step 1: We shall begin with giving an id to the posts in `views.py`.**

![](https://i.imgur.com/5a9vnJF.png)

**Step 2: Use the given id in the URL part.**

![](https://i.imgur.com/WUeDNDA.png)

* Now, when you click at `Read more` in the root URL of post 2, you will be redirected to `http://127.0.0.1:8000/post/2`. Similarly, when you click at `Read more` in the root URL of post 3, you will be redirected to `http://127.0.0.1:8000/post/3` and the same applies to all posts.

![](https://i.imgur.com/KaRDvv4.png)

***

> \[!NOte] This isn't a good practice to hardcode in the template.

### Using the URL tag

To make this process more efficient, we are going to use the URL tag.

* You can see that we have already linked the path and named it as `detail` in the `urls.py` file.

![](https://i.imgur.com/fxqKYf6.png)

* Use the URL tag applying the following syntax.

```html

<a href="<div data-gb-custom-block data-tag="url" data-0='app_name:url_name'></div>">View Post</a>

```

![](https://i.imgur.com/wIAA5bL.png)

***
