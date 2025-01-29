# **Parallax Scroll Effect**

## **Summary**

In this exercise you will be creating a landing page for a restraunt with a modern looking layout using a Parallax Scoll.

---

## **Instructions**

No changes are needed in the `index.html`. All code changes should be made in `style.css`.

---

### **1. Add Images for the Parallax Effect**

- First, review the HTML. Do not make any changes, but take note of the order and layout of the `div` elements. There are six `div`s alternating between the classes `parallax` and `content`. Images will be applied to the `parallax` class elements.

- Using the `.parallax` selector and child pseudo-selectors, target each `parallax` `div` and assign an image from the `images` folder:

```
.parallax:first-child {
  background-image: url("./images/food.png");
}

.parallax:nth-child(3) {
  background-image: url("./images/restaurant.png");
}

.parallax:nth-child(5) {
  background-image: url("./images/livemusic.png");
}
```

---

### **2. Adjust Content Section for Parallax Effect**

- Run Live Server and take a look at the content in the browser. The content is visible, but we need to ensure each section takes up the full viewport height.

- Use the `.content` selector to set the height to `100vh`. This is crucial for creating the parallax effect.

- Add additional styling to make the content visually appealing:
  - Use `flex` and `text-align` to center the items.
  - Set a background color of `#f4f4f4`, a soft pinkish-gray.

```
.content {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: #f4f4f4;
  text-align: center;
}
```

---

### **3. The Parallax Styling**

- Observe the changes in the HTML. The content looks correct, but now we need to add the parallax effect to the images.

- Using the `.parallax` selector:

  - Set `height: 100vh` to make each parallax section take up the full height of the viewport.
  - Use `background-size: cover` to ensure the image fills the section without stretching.
  - Set `background-position: center` to center the image within the section.
  - Apply `background-attachment: fixed` to make the image stay in place as you scroll, creating the parallax effect.

- Add additional styling to center and align the content, and make it visually appealing.

```css
.parallax {
  height: 100vh;
  background-size: cover;
  background-attachment: fixed;
  background-position: center;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
}
```

---
