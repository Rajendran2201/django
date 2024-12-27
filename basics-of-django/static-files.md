---
icon: css3
---

# Static files

**Static files** are assets like CSS, JavaScript, images, fonts, and other non-dynamic resources needed for your web application's frontend

**Using Static Files in Templates**

To include static files in your templates:

1. Load the static template tag:

```html

<div data-gb-custom-block data-tag="load"></div>

```

2. Reference the file using \`

\`:

```html
<link rel="stylesheet" href="<div data-gb-custom-block data-tag="static" data-0='myapp/style.css'></div>">

<script src="<div data-gb-custom-block data-tag="static" data-0='myapp/script.js'></div>"></script>

<img src="<div data-gb-custom-block data-tag="static" data-0='myapp/logo.png'></div>" alt="Logo">

```

***

### Linking `style.css` file

**Augmenting static template tag**

![](https://i.imgur.com/KaODJBS.png)

**Configuring Static Files**

In your Django project's `settings.py`, configure the following settings:

![](https://i.imgur.com/a3KClUd.png)

You could see that the `style.css` file has been linked.

![](https://i.imgur.com/mfknGcH.png)

***
