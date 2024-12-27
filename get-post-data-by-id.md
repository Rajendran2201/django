---
icon: fingerprint
---

# Get post data by ID

Even though we have our posts in the root webpage, when we navigate to the post page, it throws an error.

![](https://i.imgur.com/xT2DWjm.png)

This is because we haven't worked on this part yet.

* Make the necessary changes. use the `get()` method to search among the data in the database.

![](https://i.imgur.com/gIdRogO.png)

* Change the static data into dynamic ones in the `detail.html` file.

![](https://i.imgur.com/2rkny7p.png)

* Now each post page will look below.
* You can format the posted on as just display the date using filters

```html
<p class="text-muted">Posted on {{post.created_at | date:"F j, Y"}}</p>
```

![](https://i.imgur.com/9HZp9Qk.jpeg)

![](https://i.imgur.com/99lv3Lk.jpeg)

**After filtering the date**

![](https://i.imgur.com/ZjE7z6x.jpeg)

***

### Another filter

You can also use another filter `truncatechars` in the `index.html` file.

![](https://i.imgur.com/A3p54n9.png)

Upon the usage, the output would look as below.

![](https://i.imgur.com/idcoB1u.jpeg)

***
