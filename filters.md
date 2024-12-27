---
icon: filter
---

# Filters

* Django templates support **filters** to modify the displayed value of a variable.
* **Filters** in Django templates are tools that transform the output of variables before rendering.
* They allow you to format, manipulate, or modify data directly within the template without altering the data in the view.

***

#### Basic Syntax

Apply a filter to a variable using the pipe (`|`) character:

```html
{{ variable|filter_name }}
```

You can chain multiple filters:

```html
{{ variable|filter1|filter2 }}
```

***

#### Commonly Used Filters

**1. Text Manipulation**

*   **`lower`**: Converts text to lowercase.

    ```html
    {{ "HELLO"|lower }}  <!-- Output: hello -->
    ```
*   **`upper`**: Converts text to uppercase.

    ```html
    {{ "hello"|upper }}  <!-- Output: HELLO -->
    ```
*   **`title`**: Capitalizes the first letter of each word.

    ```html
    {{ "hello world"|title }}  <!-- Output: Hello World -->
    ```
*   **`truncatechars`**: Truncates the string after a specific number of characters.

    ```html
    {{ "Django templates are powerful"|truncatechars:10 }}  <!-- Output: Django t... -->
    ```

**2. Date and Time Formatting**

*   **`date`**: Formats a date object.

    ```html
    {{ current_date|date:"F d, Y" }}  <!-- Output: December 12, 2024 -->
    ```

    Common date formats:

    * `"Y-m-d"`: 2024-12-12
    * `"D M j"`: Thu Dec 12
    * `"F d, Y"`: December 12, 2024
*   **`time`**: Formats a time object.

    ```html
    {{ current_time|time:"H:i" }}  <!-- Output: 14:30 -->
    ```

**3. List and String Operations**

*   **`join`**: Joins a list into a string using a separator.

    ```html
    {{ ["a", "b", "c"]|join:", " }}  <!-- Output: a, b, c -->
    ```
*   **`length`**: Returns the length of a string or list.

    ```html
    {{ "hello"|length }}  <!-- Output: 5 -->
    {{ [1, 2, 3]|length }}  <!-- Output: 3 -->
    ```
*   **`slice`**: Slices a list or string (similar to Python slicing).

    ```html
    {{ "abcdefg"|slice:":3" }}  <!-- Output: abc -->
    ```

**4. Default and Conditional Filters**

*   **`default`**: Specifies a default value if the variable is empty.

    ```html
    {{ username|default:"Guest" }}  <!-- Output: Guest if username is None -->
    ```
*   **`default_if_none`**: Similar to `default`, but only applies if the value is `None`.

    ```html
    {{ age|default_if_none:"Unknown" }}  <!-- Output: Unknown if age is None -->
    ```

**5. Math and Numeric Filters**

*   **`add`**: Adds a value to a variable.

    ```html
    {{ 5|add:3 }}  <!-- Output: 8 -->
    ```
*   **`divisibleby`**: Checks if a number is divisible by a given value (used in conditionals).

    ```html
    <div data-gb-custom-block data-tag="if" data-0='3' data-1='3' data-2='3' data-3='3' data-4='3' data-5='3' data-6='3' data-7='3' data-8='3' data-9='3' data-10='3' data-11='3' data-12='3' data-13='3' data-14='3' data-15='3' data-16='3' data-17='3' data-18='3' data-19='3'>

        {{ number }} is divisible by 3.

    ```

\`\`\`

**6. Boolean and Comparison Filters**

*   **`yesno`**: Converts a boolean value to specified text.

    ```html
    {{ True|yesno:"yes,no,maybe" }}  <!-- Output: yes -->
    {{ False|yesno:"yes,no,maybe" }}  <!-- Output: no -->
    ```

**7. Escaping and Safe Content**

*   **`safe`**: Marks a string as safe (disables auto-escaping).

    ```html
    {{ "<b>bold</b>"|safe }}  <!-- Output: <b>bold</b> -->
    ```
*   **`escape`**: Escapes HTML characters.

    ```html
    {{ "<b>bold</b>"|escape }}  <!-- Output: &lt;b&gt;bold&lt;/b&gt; -->
    ```

***

#### Chaining Filters

You can chain multiple filters to transform a variable in stages.

Example:

```html
{{ "  hello world  "|trim|title|escape }}
```

Output:

```html
Hello World
```

***

### Let's try using them

**`upper`**

![](https://i.imgur.com/j1uWQ3C.png)

![](https://i.imgur.com/HJ6Kw69.png)

**`length`**

![](https://i.imgur.com/mVXTD4v.png)

![](https://i.imgur.com/dNkuemy.png)

**`truncatewords`**

![](https://i.imgur.com/PcAle1d.png)

![](https://i.imgur.com/0DnaT1W.png)

* Here it is showed as `Raj ...`, this is called as **Text Ellipsis**. It is usually used when displaying long descriptions.

***

### Exercise: Variable interpolation for `details.html`

* The webpage of `index.html` shows `Raj's Blog Posts` as we have sent it through the `render()` in `views.py`.

![](https://i.imgur.com/3AO9YwF.png)

![](https://i.imgur.com/gfDpi9N.png)

* But for `details.html`, we are not providing it explicitly.

![](https://i.imgur.com/rUKzPpF.png)

![](https://i.imgur.com/cr9NTwo.png)

* We have a filter for this to display the default value when we don't receive it from the `views.py`. For doing this, we have a filter called `default`.

![](https://i.imgur.com/xOqf2Gz.png)

![](https://i.imgur.com/WiirsLV.png)

> Note: there should be no space after the colon symbol in `default` filer -> valid: `default:"base title"` -> invalid: `default: "base title"`

* It results in `TemplateSyntaxError` if there's any space after the colon symbol.

![](https://i.imgur.com/kvj0YJv.png)

![](https://i.imgur.com/fVfJWAL.png)

***

#### Best Practices

1. **Use Built-in Filters**: Django provides many useful filters, reducing the need for custom ones.
2. **Keep Templates Lightweight**: Avoid using filters for complex logic; handle that in views or models.
3. **Test Filters Thoroughly**: Ensure your filters handle edge cases, such as `None` values or empty strings.

***
