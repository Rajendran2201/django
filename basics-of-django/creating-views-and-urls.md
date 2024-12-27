---
icon: binoculars
---

# Creating Views and URL's

***

### What are views?

In Django, **views** are Python functions or classes that handle HTTP requests and return HTTP responses. Views connect your app's data (via models) to the user interface (via templates).

### Creating views

You can create your views in the `myapp\blog\views.py` file.

![](https://i.imgur.com/va0WNIX.png)

***

### Adding the URL

* Create a new file called `urls.py` inside the `blog` app.

![](https://i.imgur.com/6v7iZgt.png)

***

### Register the URL

* Now, you have to register your URL. For this, go to `url.py` in the `myapp` folder and add the url here.

![](https://i.imgur.com/54fiTpd.png)

* As you have done this, the website will contain the contents of the view we just created.

![](https://i.imgur.com/acY4scj.png)

***

### Set up a new URL other than the root URL

If you want the view in a new URL other than the root URL, than specify it in the `urlpatterns`.

![](https://i.imgur.com/EoC5qfF.png)

***
