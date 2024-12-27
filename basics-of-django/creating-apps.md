---
icon: browser
---

# Creating apps

### How to create apps in django?

In Django, an **app** is a modular unit that handles a specific functionality of your project. For example, if you're building an e-commerce website, you might have separate apps for managing products, orders, and user accounts.

You can start creating a new app in your project using the following command

```bash
python3 manage.py startapp app-name
```

![](https://i.imgur.com/S4H3PPK.png)

This creates a new directory named `blog/` with the following structure:

```bash
blog/
    __init__.py  -----> indicates that the directory is a python package
    admin.py ---------> Register models here to makes them manageable
    apps.py ----------> contains the metadata about the app
    migrations/ ------> it represents database scheme changes
        __init__.py 
    models.py --------> define database models
    tests.py ---------> contains unit tests
    views.py ---------> fefine the logic to handle HTTP requests

```

***

#### Register your app

You have to register to your app in the `setting.py` file. Only then, django can recognise your app.

**Steps to add app to your project:**

* Open your project's `settings.py`.
* Locate the `INSTALLED_APPS` list.
* Add your app to the list

![](https://i.imgur.com/25jwUCk.png)
