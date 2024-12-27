---
icon: shield-cross
---

# Partial Templates

**Partial templates** in Django refer to reusable snippets of HTML that can be included in multiple templates. This helps you adhere to the **DRY (Don't Repeat Yourself)** principle, reducing redundancy and making your templates easier to maintain.

**Why Use Partial Templates?**

1. **Reusability**: Share common components like headers, footers, or sidebars across multiple pages.
2. **Consistency**: Ensure uniformity in design by using the same partials for shared elements.
3. **Maintainability**: Update a single file, and the changes reflect wherever it's used.

### Step 1: Curate the `base.html` file

* Remove the **header** and **footer** part from the `base.html` file and create new files named `header.html` and `footer.html` and place them in these files.
* The new files are created in the location `templates\includes\`

![](https://i.imgur.com/cGCUNXz.png)

* The `header.html` files looks as follows.

![](https://i.imgur.com/dbndtTW.png)

* The `footer.html` file is as follows.

![](https://i.imgur.com/jmjkg8i.png)

### Step 2:

* Include the newly created files into the `base.html` file

![](https://i.imgur.com/iaj36CB.png)

* Now if you visit `http://127.0.0.1:8000/`, the website would look still.

![](https://i.imgur.com/0yp3UcD.png)
