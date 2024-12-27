---
icon: database
---

# Connecting MySQL Database

> Pre-requisite: Ensure that you have MySQL server running in your local device. If not, download it from [here](https://dev.mysql.com/downloads/installer/).

* As you download MySQL, setup the environment and open MySQL workbench.

![](https://i.imgur.com/isM3v3j.jpeg)

* Create a database in SQL.

![](https://i.imgur.com/C6XbFhM.png)

* Install `mysqlclient` in the terminal using `pip`.

> Ensure that you have activated the virtual environment.

![](https://i.imgur.com/WQjxH1b.png)

* An error occurs here which says,

```bash
note: This error originates from a subprocess, and is likely not a problem with pip.
error: subprocess-exited-with-error

× Getting requirements to build wheel did not run successfully.
│ exit code: 1
╰─> See above for output.

note: This error originates from a subprocess, and is likely not a problem with pip.

[notice] A new release of pip is available: 24.0 -> 24.3.1
[notice] To update, run: pip install --upgrade pip
```

This may occur If you haven't already installed the MySQL client libraries properly.

To resolve this use,

```bash
brew install mysql
```

* Now you can download `sqlclient` using the `pip` command.

![](https://i.imgur.com/0jBY4IU.png)

* To verify the installation, use the `pip list` command.

![](https://i.imgur.com/aFIG9R6.png)

***

* In Django, the default database is configured as `sqlite`.

![](https://i.imgur.com/9NaN0vU.png)

* Change the parameters as follows.

![](https://i.imgur.com/wTQkSQt.png)
