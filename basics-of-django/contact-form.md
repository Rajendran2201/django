---
icon: address-book
---

# Contact form

We shall begin the process by creating a function named `contact_view` in the `views.py` file.

![](https://i.imgur.com/vqo4d2v.png)

* Set up the template for contact form.

![](https://i.imgur.com/oEDbOWj.png)

* Setup the path in the `urls.py` file.

![](https://i.imgur.com/3j2Vf2g.png)

* When you redirect to the link `http://127.0.0.1:8000/contact`, the contact form will be displayed.

![](https://i.imgur.com/fEWmwT2.png)

* Specially for creating forms, Django offers a package called `forms`. So, let's create a new file named `forms.py`.

![](https://i.imgur.com/0eC1kWU.png)

* Ensure that the form method is set as `post`.

![](https://i.imgur.com/8Oyx0Hl.png)

> \[!tip] for displaying the footer in the bottom of the webpage, use the following css snippet.

```css
footer {
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
}
```

![](https://i.imgur.com/uwBhfwL.png)

* When you try to submit the form, you'll encounter an error as follows.

![](https://i.imgur.com/iKfDMIz.png)

* This is because whenever you try to submit a form in Django, you need to send a cookie called CSRF for security purposes. This prevents the hackers from performing data theft.
* For dealing with this, we have to augment a a `csrf_token` in our code right below the form tag.

![](https://i.imgur.com/chSQ8yE.png)

* This will create a hidden element in the form which you can view by inspecting the page.

![](https://i.imgur.com/GR7GKmD.png)

* Now, if you try submitting the page, it would cause no error. This is because the `csrfmiddlewaretoken` tells the webpage that the user is authenticated.

***

Once this process is done, we have to fetch the data entered in the fields of the contact form. For this, we have to import the `Contactform`.

```python
from .forms import ContactForm
```

![](https://i.imgur.com/GeRKAH8.png)

![](https://i.imgur.com/IaO8Jij.png)

![](https://i.imgur.com/LiZNEb8.png)

* Now it is evident that the data given in the form can be fetched at the backend.=
