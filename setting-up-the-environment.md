---
icon: envira
---

# Setting up the environment

***

### Install Django

We shall begin the process by installing Django in out system. The commands in this tutorial will be applicable for macOS.

Step 1: Install [Python](https://www.python.org/downloads/). Ensure python has been installed in your system.

![](https://i.imgur.com/ae9frKA.png)

Step 2: Install Django. I am gonna install using pip3 here. You can redirect to the [installation guide](https://docs.djangoproject.com/en/5.1/topics/install/#installing-distribution-package) and follow those steps to install it.

![](https://i.imgur.com/dOybbwz.png)

You can also verify your installation using the command `django-admin --version`.

![](https://i.imgur.com/8qNmwB6.png)

By this, you have successfully installed django in your system. We can now start working on the projects.

***

### Setting up a virtual environment

1. Create a folder in your desired location and open it in the terminal.

![](https://i.imgur.com/ywMkKFR.png)

2. Create a virtual environment using the command

```bash
python3 -m venv myenv

```

3. Activate the environment

```bash
source myenv/bin/activate
```

4. Install Django in the virtual environment:

```bash
pip install django
```

![](https://i.imgur.com/TaQp3jM.png)

> In case, if you want to deactivate the virtual environment when done, use the command `deactivate`.

***

### Creating a django project

1. You can create a django project using the following command.

```bash
django-admin startproject project-name
```

![](https://i.imgur.com/IPoUmAB.png)

2. You can now start the server with the following command.

```bash
python3 manage.py runserver
```

![](https://i.imgur.com/5H5ZNjb.png)

* Now, the server has been locally hosted.

![](https://i.imgur.com/1NKCExl.png)

***

### Project Structure

![](https://i.imgur.com/xb9Y8h5.png)

```plaintext
projectname/
    manage.py
    db.sqlite3
    projectname/
        __init__.py
        asgi.py
        settings.py
        urls.py
        wsgi.py
```

**1. `manage.py`**

* **Purpose**: A command-line utility that lets you interact with the Django project.
* **Usage**:
  * Start the development server: `python manage.py runserver`
  * Create database migrations: `python manage.py makemigrations`
  * Apply migrations: `python manage.py migrate`
  * Create a superuser: `python manage.py createsuperuser`

***

**2. Project Package (`projectname/`)**

This folder contains the core configuration files for the Django project.

**`__init__.py`**

* **Purpose**: An empty file that indicates this directory is a Python package.
* **Usage**: Required for importing modules from the `projectname` package.

**`settings.py`**

* **Purpose**: Contains all the settings and configuration for your Django project.
* **Key Sections**:
  * **`INSTALLED_APPS`**: A list of apps activated in the project.
  * **`MIDDLEWARE`**: A list of middleware for processing requests and responses.
  * **Database configuration**: Specifies the database used by the project.
  * **Static files and templates**: Configuration for serving static files and templates.

**`urls.py`**

* **Purpose**: Maps URLs to their corresponding views.
* **Structure**:
  * A list of URL patterns that define how URLs are routed.
  * Typically includes references to app-specific URLs.
  *   Example:

      ```python
      from django.contrib import admin
      from django.urls import path, include

      urlpatterns = [
          path('admin/', admin.site.urls),
          path('app/', include('appname.urls')),  # Include app-specific URLs
      ]
      ```

**`asgi.py`**

* **Purpose**: Configures the project for ASGI (Asynchronous Server Gateway Interface).
* **Usage**: Required for deploying Django with asynchronous servers like Daphne or Uvicorn.

**`wsgi.py`**

* **Purpose**: Configures the project for WSGI (Web Server Gateway Interface).
* **Usage**: Required for deploying Django with traditional web servers like Gunicorn or uWSGI.

**`db.sqlite3`**

The file **`db.sqlite3`** is the default database file created when you start a new Django project and run the initial migration commands. It is a **SQLite database file** that stores all the data for your project, including user information, application data, and admin interface data.

***
