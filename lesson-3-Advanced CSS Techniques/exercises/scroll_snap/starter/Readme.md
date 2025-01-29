# **CSS Scroll Snap**

## **Summary**

In this exercise, you will use CSS scroll snap to guide your user's focus to specific elements.

---

### **Resources**

- [CSS Scroll Snap](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_scroll_snap)

---

## **Instructions**

No changes are needed in the `index.html`. All code changes should be made in `style.css`.

---

### **1. Preparing the container**

- To use scroll snap, we need to allow the container to scroll horizontally so it only shows one element at a time.
- Add `overflow-x: auto;` to the `.scroll_container` selector. The selector already includes code to size the content to show one element at a time.

  ```
  .scroll_container {
    display: flex;
    flex-direction: row;
    width: 20vh;
    height: 20vh;
    overflow-x: auto;
  }
  ```

---

### **2. Adding Scroll Snap Properties**

- Add the rule `scroll-snap-type: x mandatory;` to the `.scroll_container` selector. This ensures horizontal scroll snapping to the nearest snapping point.
- Add the rule `scroll-snap-align: start;` to the `.scroll_container div`. This defines where each scroll snap aligns — in this case, at the start of the element.

  ```
  .scroll_container {
    /* Existing styles */
    scroll-snap-type: x mandatory;
  }

  .scroll_container div {
    /* Existing styles */
    scroll-snap-align: start;
  }
  ```

---

### **3. Experiment with the Properties**

- Try changing `scroll-snap-type` to see the differences in behavior. Experiment with values like `x proximity` and `x mandatory`.
- Add `scroll-padding` or `margin` to see how they impact the scroll snapping behavior.
- Once you're satisfied with your experiments, return the scroll snap values to those listed in Step 2 to complete the exercise.
