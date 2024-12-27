---
icon: blog
---

# Using logger for debugging

* Iterate through the posts and sent it to the detail page

![](https://i.imgur.com/GlaJAco.png)

> \[!note] To use logging, you have to use `import logging`

![](https://i.imgur.com/U3leONv.png)

* Go to the official documentation of Django and move to the [logging](https://docs.djangoproject.com/en/5.1/topics/logging/) section

![](https://i.imgur.com/xOo2h8F.png)

* paste the copied code at the end of `myapp/settings.py` file.

![](https://i.imgur.com/eNUBzRk.png)

* Set the level as `DEBUG`.

![](https://i.imgur.com/wOQ23cL.png)

* The log information will be displayed in the console.

![](https://i.imgur.com/WMdMfi1.png)

* Just to make sure everything works fine, convert the `post_id` into `int` type.

![](https://i.imgur.com/tpdf7Q2.png)

***

* For now, we'll turn off the logger. We can use it later incase of requirement.

![](https://i.imgur.com/sUY2SaY.png)

**Before we move on to the next, Let's make the post content dynamic**

![](https://i.imgur.com/1Bvwk2D.png)

![](https://i.imgur.com/orUZbln.png)
