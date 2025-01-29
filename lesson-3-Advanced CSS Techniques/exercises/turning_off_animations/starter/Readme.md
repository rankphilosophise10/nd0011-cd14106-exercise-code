# **Turning off Animations**

## **Summary**

In this exercise, will be turning off the background animation from our last exersise.

---

### **Resources**

- [prefers-reduced-motion](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion)

---

## **Instructions**

No changes are needed in the `index.html`. All code changes should be made in `style.css`.

---

### **1. Remove animations for mobile devices**

- Use a media query to remove the animation from `.circle` for mobile devices with a screen width of less than 750px.
- Use the `.circle` selector within the media query to turn off the animation by setting `animation` to `none`.

```
@media (max-width: 750px) {
  .circle {
    animation: none;
  }
}
```

---

### **2. Turn Off Animations for Prefers Reduced Motion**

- Use a media query to turn off the animations for devices where the user has set a preference to reduce motion by passing the media query `prefers-reduced-motion: reduce`.
- Use the `.circle` selector within the media query to disable the animation by setting `animation` to `none`.

```
@media (prefers-reduced-motion: reduce) {
  .circle {
    animation: none;
  }
}
```

---

### **3. Test Your Code with Dev Tools**

- Run the code in the browser using Live Server.

- Open Chrome DevTools and click the device icon in the upper right-hand corner. Select a device with a screen width under 750px and observe if the animation stops for the `.circle`.

- Return the screen to its normal size. Click the three dots in the upper right-hand corner of DevTools, select **More Tools**, and then **Rendering**. A **Rendering** tab will appear at the bottom of DevTools. Scroll down and select **Emulate CSS media feature prefers-reduced-motion** and observe if the animation stops for the `.circle`.

---
