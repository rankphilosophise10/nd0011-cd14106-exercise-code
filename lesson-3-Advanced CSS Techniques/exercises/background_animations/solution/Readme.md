# **Animated Backgrounds**

## **Summary**

In this exercise, will be adding a animated background to an application for meditation. The background is slow circle that eases in and out to match a breathing pattern.

---

### **Resources**

- [CSS Animation](https://developer.mozilla.org/en-US/docs/Web/CSS/animation)

---

## **Instructions**

No changes are needed in the `index.html`. All code changes should be made in `style.css`.

---

### **1. Position Absolute**

- Add `position: absolute` to `.text-content` and `.circle` to remove them from the normal document flow.

- Assign a `z-index` of `1` to `.text-content` and `-1` to `.circle`. This will layer the circle underneath the text content. This will assure the content is in the background.

```
.text-content {
  ...
  position: absolute;
  z-index: 1;
}

.circle {
  ...
  position: absolute;
  z-index: -1;
}
```

---

### **2. Adding Keyframes Animation**

- Add `@keyframes` and name it `breathe`.
  - At `0%` and `100%`, the animation starts and ends with the circle at its normal size. Use `transform` with `scale(1)` to keep it at 100% of its width and height.
- At `50%`, the circle will be at its largest size. Use `transform` with `scale(1.5)` to increase its size by 50% in both width and height.

```
@keyframes breathe {
  0%,
  100% {
    transform: translate(-50%, -50%) scale(1);
  }

  50% {
    transform: translate(-50%, -50%) scale(1.5);
  }
}

```

---

### **3. Add the Animation to the Circle**

- Apply the animation to the `.circle` selector using the keyframe name `breathe`.
- Set the duration of the animation to `10 seconds`.
- Use the `ease-in-out` timing function for a smooth start and end.
- Make the animation run indefinitely by setting it to `infinite`.
- Run the application in live server to see the results!

```
.circle {
  ...
  animation: breathe 10s ease-in-out infinite;
}
```

-
