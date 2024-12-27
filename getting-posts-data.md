---
icon: apostrophe
---

# Getting posts data

* We would no longer need the static data . So let's remove it.

![](https://i.imgur.com/txRylWM.png)

* Replace the static data with the dynamic data.
* For this import `Post` class from `models`.
* Extract the data using the `all()` method.

![](https://i.imgur.com/c6x6Ele.png)

Now the webpage looks as follow.

![](https://i.imgur.com/kp3NHEk.png)

You could notice, there is a problem with the images. Let's fix it.

To fix this, we have to use the variable `post.img_url` instead of static image URL.

![](https://i.imgur.com/zyvwFdl.png)

Now, the webpage contains the images as well.

![](https://i.imgur.com/dDcErT4.jpeg)

For a better UI, we have to use the proper sizing of the images. So, the sizes are adjusted.

![](https://i.imgur.com/iaiKmJ4.png)

***
