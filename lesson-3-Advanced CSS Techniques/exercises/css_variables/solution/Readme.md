# **CSS Variables**

## **Summary**

In this exercise, you will be using CSS variables to color boxes in HTML.

---

### **Resources**

- [CSS Variables MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)

---

## **Instructions**

Nothing in the `index.html` needs to be updated. All code changes should be contained in `style.css`.

---

### **1. Create a Variable**

- Select the class `.primary`.
- Add a variable called `--primary-color` and set it to `#2596be`.
- Use the `var()` function to apply the variable as the background color for the `.primary` class.
- Open the file in the browser to observe the result.

```
.primary {
  --primary-color: #2596be;
  background-color: var(--primary-color);
}
```

---

### **2. Observe the Limitations of Variables Defined Within a Selector**

- Select the class `.primary-two`.
- Attempt to use the `var()` function to set the background color to `--primary-color`.
- Observe in the browser that the background color is not applied. Variables defined within a selector are only accessible in that selector and its descendants.
- Add a second variable called `--secondary-color` and assign it a color.
- Add a selector for `.primary-child`, give it a width of `50px`, height of `50px`, and margin of `25px`. Use the `var()` function to apply `--secondary-color` as its background color.
- Unlike the `.primary-two` selector, which is a sibling of `.primary`, `.primary-child` is nested inside `.primary` and has access to the variables defined in `.primary`.

```
.primary {
  --primary-color: #2596be;
  --secondary-color: #eeeeee;
  background-color: var(--primary-color);
}

.primary-two {
  background-color: var(--primary-color); /* This will not work */
}

.primary-child {
  width: 50px;
  height: 50px;
  margin: 25px;
  background-color: var(--secondary-color);
}
```

---

### **3. Set Variables Globally Using the `:root` Pseudo-Selector**

- Use the `:root` pseudo-selector and move the variables `--primary-color` and `--secondary-color` from `.primary` to `:root`.
- Add an additional variable, `--call-to-action`, and assign it a contrasting color.
- Use the `var()` function to set the background color of each box in the HTML file to match its class name:
  - `.primary` and `.primary-two` should use `--primary-color`.
  - `.secondary` and `.secondary-two` should use `--secondary-color`.
  - `.call-to-action` and `.call-to-action-two` should use `--call-to-action`.

```
:root {
  --primary-color: #2596be;
  --secondary-color: #eeeeee;
  --call-to-action: #e28743;
}

body {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
}

div {
  width: 100px;
  height: 100px;
}

.primary {
  background-color: var(--primary-color);
}

.primary-two {
  background-color: var(--primary-color);
}

.primary-child {
  width: 50px;
  height: 50px;
  margin: 25px;
  background-color: var(--secondary-color);
}

.secondary {
  background-color: var(--secondary-color);
}

.secondary-two {
  background-color: var(--secondary-color);
}

.call-to-action {
  background-color: var(--call-to-action);
}

.call-to-action-two {
  background-color: var(--call-to-action);
}
```

---
