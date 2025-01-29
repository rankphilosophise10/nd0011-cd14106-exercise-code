# **Backdrop Filters and Color Scheme**

## **Summary**

In this exercise, you will use CSS to apply backdrop filters to highlight text on an image and use a media query to implement a dark theme color scheme.

---

### **Resources**

- [backdrop-filter](https://developer.mozilla.org/en-US/docs/Web/CSS/backdrop-filter)

---

## **Instructions**

No changes are needed in the `index.html`. All code changes should be made in `style.css`.

---

### **1. Adding a backdrop-filter`**

- Add `backdrop-filter: invert(30%);` to the `h1` selector:

```
h1 {
  ...
  backdrop-filter: invert(30%);
}
```

---

### **2. Try Different Filters**

- Switch the `backdrop-filter` property to experiment with different options. Pick the one that leaves the text readable.

**Backdrop Filters to Try**:

- blur() (e.g., px, em, rem, %)
- brightness() (e.g., number or %)
- contrast() (e.g., number or %)
- grayscale() (e.g., %)
- opacity() (e.g., number or %)
- drop-shadow(offset-x-axis, offset-y-axis, color) (e.g., px, em, rem)

### **3. Add Dark Mode Option**

- Use a media query to add a dark mode option.
- Apply the media query `prefers-color-scheme: dark` as shown below:

```css
@media (prefers-color-scheme: dark) {
  body,
  header {
    background-color: black;
    color: #e0e0e0;
  }

  nav {
    border-bottom: 3px solid #e0e0e0;
  }

  li {
    color: #e0e0e0;
  }
}
```

---

### **4. Test Dark Mode Option with Dev Tools**

- Open the project in Live Server.
- Open Chrome DevTools and click the three dots in the top-right corner.
- Select **Rendering** from the dropdown menu.
- A new **Rendering** tab will appear at the bottom. Scroll down to the **Emulate CSS media feature** section.
- Select `prefers-color-scheme: dark` to verify the results.
