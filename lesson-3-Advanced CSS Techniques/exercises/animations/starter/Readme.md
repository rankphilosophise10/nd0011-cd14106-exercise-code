# **Animated Backgrounds**

## **Summary**

In this exercise, you’ll create a cool transition that makes a square grow and change color when you hover over it, and an animation that makes a ball roll back and forth.

---

### **Resources**

- [CSS Animation](https://developer.mozilla.org/en-US/docs/Web/CSS/animation)
- [CSS Transtion](https://developer.mozilla.org/en-US/docs/Web/CSS/transition)

---

## **Instructions**

No changes are needed in the `index.html`. All code changes should be made in `style.css`.

---

### **1. On hover Transition**

- Add the `transition` property to the `.square` selector. This will let the square scale up and change color on hover.

- Set the transition duration with `transition-duration: 0.5s;`. This makes the transition last half a second.

- Add `transition-property: all, background-color;`.

  - The first part applies to all animatable properties.
  - The second specifically targets the `background-color`.

- Use `transition-duration: 0.5s, 0.5s;` to set the duration for both transitions.

- Add `transition-timing-function: ease, ease-in-out;`.

  - Notice the difference in how these easing functions change the animation speed.
  - If it’s hard to see, try increasing the duration.

- Target the `:hover` pseudo-class on the `.square` selector.

- Add `transform: scale(3);` to make the square grow to 3x its size when hovered.

- Change the `background-color` to `purple` on hover.

- Test it out in your browser (use Live Server if available) and see how it looks!

---

```
.square {
  width: 100px;
  height: 100px;
  margin: 20%;
  background-color: aqua;
  transition-property: all, background-color;
  transition-duration: 0.5s, 0.5s;
  transition-timing-function: ease-in-out, ease-in-out;
}

.square:hover {
  transform: scale(3);
  background-color: purple;
}


```

---

### **2. Adding Keyframes Animation**

- Use `@keyframes` to create an animation called `roll`.

- At the **start (0%)** and **end (100%)** of the animation, the element should be positioned at `-200px` from its default location. Use `transform: translateX(-200px);` for this.

- At **50%** of the animation, the element should be positioned at `200px` from its default location. Use `transform: translateX(200px);` for that.

---

```
@keyframes roll {
  0%,
  100% {
    transform: translateX(-200px);
  }
  50% {
    transform: translateX(200px);
  }
}
```

---

### **3. Add the Animation to the Circle**

- Apply the animation to the `.circle` selector using the keyframe name `roll`.

- Set the **animation duration** to 6 seconds by adding `animation-duration: 6s;`.

- Make the animation repeat indefinitely by setting `animation-iteration-count: infinite;`.

- Use a constant speed for the animation by setting the **animation-timing function** to `linear`.

---

### Example Code

```
.circle {
  /* ... other styles */
  animation-name: roll;
  animation-duration: 6s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
}
```

-
