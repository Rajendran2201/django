---
icon: binary-circle-check
---

# Inserting Data and Custom Commands

### Step 1: create `populate_data.py` file

* We'll begin the process of insertion by creating a new file named `blog/populate_data.py`.
* Add some data on the file.

![](https://i.imgur.com/mE7t8k7.png)

> For image URL's, refer the [lorem picsum](https://picsum.photos/images) website

### Step 2: Install `faker` library

You can use the **`Faker`** library in Python to generate realistic and random data for your blog app.

```bash
pip install faker
```

![](https://i.imgur.com/YZsBAtv.png)

* Iterate through the data and pass individually to create the post.

![](https://i.imgur.com/J4hRjoZ.png)

* We have used `from blog.models import Post`, this actually mean the one we created previously.

![](https://i.imgur.com/NeQpmgH.png)

### Step 3: make some quick advancements

1. Import the BaseCommand

```python
from django.core.management.base import BaseCommand
```

2. Create a class called `Command` extending `BaseCommand`.
3. Write a help variable which tells exactly why this class `Command` has been created.
4. Write a function `handle()` which contains the data and the **iterator** about the posts.

![](https://i.imgur.com/OWjkzo2.png)

5. At the end of the function, include the success prompt.

```python
self.stdout.write(self.style.SUCCESS("Completed Inserting data"))
```

![](https://i.imgur.com/pslWlDT.png)

### Step 4: Changing the directory structure

1. Create a folder and a sub-folder `blog/management` and `management/commands` respectively
2. Include a `__init__.py` file both of these folders.
3. Move the `populate_data.py` file to the `commands` folder.
4. For better understanding, let's rename `populate_data.py` into `populate_posts.py`

Your directory structure should look as below.

![](https://i.imgur.com/Jc8mJe5.png)

### Step 5: Write into the `__init__.py` file

Now go to the `commands/__init__.py` file and import the `Command` class we have written.

```python
from .populate_posts import Command as PopulatePostCommand
```

![](https://i.imgur.com/M7DQDS5.png)

### Step 6: Run the file

Now, it's time to run the file `populate_posts.py`. This can be done by running the command as given below.

```bash
python3 ./manage.py populate_posts
```

![](https://i.imgur.com/wL9scvm.png)

This says that the data has been inserted into our database. Let's go and have a look at our DB.

![](https://i.imgur.com/EQe7gq2.jpeg)

yep, we have our data inserted into the database. But, still our webpage has not been updated yet.

![](https://i.imgur.com/XH6Mzir.png)

***
