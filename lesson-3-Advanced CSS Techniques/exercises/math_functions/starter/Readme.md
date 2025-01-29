# **CSS Math Functions**

## **Summary**

In this exercise, you will use CSS math functions to control the size of HTML elements.

---

### **Resources**

- [CSS Math Functions MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)

---

## **Instructions**

No changes are needed in the `index.html`. All code changes should be made in `style.css`.

---

### **1. Using `calc()`**

- Use the `calc()` function to reduce the size of the middle box by 30% of its parent.
- Use `calc()` again to reduce the size of the innermost box to 50% of its container (the middle box).
- Open the code in the browser and observe the results.

```
.middle-box {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #ff7f50;
  width: calc(100% - 30%);
  height: calc(100% - 30%);
}

.inner-box {
  background-color: #ffd700;
  width: calc(100% - 50%);
  height: calc(100% - 50%);
}
```

---

### **2. Using `min()`**

- Use `min()` on the width of the middle box to choose between the calculated size from the last step and another size like `800px`.
- Resize the browser window to observe what happens when the width of the box grows or shrinks.

```
.middle-box {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #ff7f50;
  width: min(800px, calc(100% - 30%));
  height: calc(100% - 30%);
}

.inner-box {
  background-color: #ffd700;
  width: calc(100% - 50%);
  height: calc(100% - 50%);
}
```

---

### **3. Using `max()`**

- Use `max()` on the height of the middle box to choose between the calculated size from the last step and another size like `200px`.
- Resize the browser window to observe what happens when the height of the box grows or shrinks.

```
.middle-box {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #ff7f50;
  width: min(800px, calc(100% - 30%));
  height: max(200px, calc(100% - 30%));
}

.inner-box {
  background-color: #ffd700;
  width: calc(100% - 50%);
  height: calc(100% - 50%);
}
```

---
