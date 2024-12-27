---
icon: table
---

# Creating category model for Models

* We have a problem. the category of every blog is same as it was hard-coded / static. We have to fix this.

![](https://i.imgur.com/lxVZZhW.jpeg)

* In order to do this, I have created a new model named `Category`.

![](https://i.imgur.com/N7N1zZw.png)

![](https://i.imgur.com/RSaFGr8.png)

* This will create a new table called `blog_category`.

![](https://i.imgur.com/kXXz2x9.png)

* Let's add some categories. For the tutorial purpose, we are going to add some random categories into it.

![](https://i.imgur.com/IB0Z84t.png)

* Insert the command into the `__init__.py` file.

![](https://i.imgur.com/iaaFoKy.png)

* Let's insert the values into the table `blog_category`

![](https://i.imgur.com/JXznI4y.png)

![](https://i.imgur.com/Zet4paI.jpeg)

* We have to link the post to the categories as `many-to-one` relationship and we are going to do it a very random way.

![](https://i.imgur.com/5IvaUTd.png)

![](https://i.imgur.com/ve3wQMc.jpeg)

![](https://i.imgur.com/VmU4KcH.png)

![](https://i.imgur.com/wV5GcQG.png)

![](https://i.imgur.com/UoBwmEt.jpeg)

We are done with the linking process. Now, each post is linked with an individual category.

***

### Showing category in the posts

![](https://i.imgur.com/nBG5Gvf.png)

![](https://i.imgur.com/2NPpjpf.jpeg)
