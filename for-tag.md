---
icon: hashtag
---

# For tag

The `<div data-gb-custom-block data-tag="for"></div>` tag in Django templates is used to loop over a sequence (like a list, tuple, or queryset) and render its elements. It's one of the most commonly used template tags for dynamic content.

### Replacing dynamic content with static content

* We are going to send the dynamic content from `views.py` to the `index.html` file.

![](https://i.imgur.com/bwgtgTR.png)

* So, we no longer need the repetitive code in `index.html`, just removing the unwanted containers.

![](https://i.imgur.com/B2rBVkN.png)

* Now, the webpage might look like this.

![](https://i.imgur.com/LbKV1ap.png)

### Using the for tag

* By using the `for` tag here, we'll be iterate through the posts that were sent from the `views.py` file through `render()` function.

![](https://i.imgur.com/HwoGfs5.png)

* So, the output looks as below.

![](https://i.imgur.com/dC8ZCLT.png)

### Using the variable interpolation for displaying the dynamic content

* Now, we can display the text in the passed dictionary through the variable interpolation method.

![](https://i.imgur.com/R7CThKS.png)

* As we do this, the output webpage would look as below.

![](https://i.imgur.com/LrCAlQE.png)

***

### What if we don't pass any data?

![](https://i.imgur.com/LXzh6o6.png)

* In such case, we won't have any data in the webpage.

![](https://i.imgur.com/3L9OKS2.png)

* This is not to be appreciated. We need to fix this.

> \[!TIP] To fix this, we need to use Conditional Variable Interpolation.

![](https://i.imgur.com/BvVcvzX.png)

![](https://i.imgur.com/WGD4Z7y.png)

***
