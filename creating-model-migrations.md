---
icon: hammer-brush
---

# Creating Model, Migrations

Creating models in Django is a crucial part of building a database-driven application. Models in Django are Python classes that define the structure of your database tables. Django uses these models to create, retrieve, update, and delete records from the database.

### Creating a model

![](https://i.imgur.com/cFLJVyX.png)

> \[!Note] `blank` is not working. Instead use `null` for allowing the field to use null values. Example: `img_url = models.URLField(null=True)`

### Creating migrations

* To create a migration, change the directory to `myapp` and run the following command

```bash
python3 manage.py makemigrations
```

![](https://i.imgur.com/1skrezU.png)

* You could see that a file `0001_initial.py` has been created in the `migrations` folder.
* The `0001_initial.py` file will look as follows.
* It creates the `id` field by default.

![](https://i.imgur.com/MR7upYn.png)

* To create the table, you have to run the following command

```bash
python3 manage.py migrate
```

![](https://i.imgur.com/RpJqGnc.png)

* The table is now created.
* A lot of other tables would also been created, which belongs to the default Django files.

![](https://i.imgur.com/GpDqpau.png)

* Right click the table and select `table inspector`.

![](https://i.imgur.com/bZIBrYe.png)

* here the `img_url` is not nullable. This is because we have to use `null` instead of `blank`.
* I have made the changes in the `models.py` file.

![](https://i.imgur.com/9S3gjSq.png)

**What should we do now to reflect the changes in the table?**

* Use the command `python3 manage.py makemigrations` again.
* This time a new file named `0002_alter_post_img_url.py` will be created

![](https://i.imgur.com/ZsW9Ksx.png)

* The `0002_alter_post_img_url.py` will look as follows.
* it consists the statement which tells what changes have been made in comparison to the previous model.

![](https://i.imgur.com/ja6fnDV.png)

* Now you have to migrate the changes.
* For this, use `python3 ./manage.py migrate`.

![](https://i.imgur.com/s3xx2eB.png)

* Now the changes would have been reflected in the database.

![](https://i.imgur.com/1wRAOd7.png)

***

### Let's try doing another change

* Now, We are going to create a new field in the model as `created_at`.

![](https://i.imgur.com/UQCWCuB.png)

* Since, we are using `auto_now_add`, It is quite concerned.
* This is because, incase if we already had any data in the database, the `created_at` field will have no values on the creating of this field.
* For this, it raises a warning and gives you two option.
* For demonstration, I have choosed `1`.
* Again it asks for timezone, just press `return` or `Enter`.

![](https://i.imgur.com/4Brdrly.png)

* Now the file `0003_post_created_at.py` would be created and looks as below.

![](https://i.imgur.com/ZwY4RPS.png)

* Now run the command `python3 ./manage.py migrate` to make the changes reflect in the database.

![](https://i.imgur.com/8d24dYq.png)

* The database has been changed as follows.

![](https://i.imgur.com/bShXiJU.png)

***

> **Note:** -> The advantage of using `migrations` over mere SQL command to create or make changes is that you can easily log the changes made in the app using migrations. -> The `migrations` folder will contain all the changes made in the app. ![](https://i.imgur.com/DEk4ouP.png)
