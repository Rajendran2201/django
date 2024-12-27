---
icon: table-layout
---

# Layouts

Creating layouts in Django involves structuring templates to maintain consistency across multiple pages by using reusable components like headers, footers, navigation bars, and base templates. Django's **template inheritance** makes this process efficient.

### Creating layouts

**Step 1: Create a base template**

The base template defines the overall structure (layout) of your site. Child templates inherit this structure.

* Insert the base content into `base.html` file from the `index.html` file.

![](https://i.imgur.com/0qlcTPz.png)

* Remove the base content from the `index.html` file. Now the `index.html` file will only contain the dynamic content.

![](https://i.imgur.com/S4nRsGN.png)

**Step 2: Extend the base template**

* Now, we have to extend the `index.html` from the `base.html` file.
* Note that the `content` is the block name that we have given for the dynamic block in the `base.html` file

![](https://i.imgur.com/ha9ZA66.png)

* Now, if you to the root URL, `http://127.0.0.1:8000/` you can view the page. This time, the webpage has static and dynamic contents together.

![](https://i.imgur.com/PX1qInW.png)

* Similarly, we can change the contents of `detail.html` file.

![](https://i.imgur.com/2ltkZOr.png)

![](https://i.imgur.com/yhESUqS.png)
