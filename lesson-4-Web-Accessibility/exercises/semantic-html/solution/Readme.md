# **Semantic HTML and ARIA Attributes**

## **Summary**

In this exercise, you will update an HTML document to use Semantic HTML and ARIA attributes to improve accessibility.

---

### **Resources**

- [MDN: HTML - A Good Basis for Accessibility](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Accessibility/HTML)
- [MDN: WAI-ARIA Basics](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Accessibility/WAI-ARIA_basics)

---

## **Instructions**

The `index.html` file contains the starter code for this exercise. Follow the steps below to update the file.

---

### **1. Update All the Divs with Semantic HTML**

Replace all `<div>` elements with semantic HTML elements, such as `<article>`, `<main>`, `<nav>`, `<footer>`, `<p>`, etc. Here's an example of how your updated code might look:

```html
<h1>News News News!</h1>
<ul class="main-menu">
  <li>Home</li>
  <li>Sports</li>
  <li>World Events</li>
  <li>Entertainment</li>
</ul>
<main>
  <h2>Articles</h2>
  <article class="article-container">
    <h3>Breaking News: New Fruit Discovered!</h3>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam consequat
      placerat sem sed gravida. Donec in cursus nibh, eu varius sapien. Nullam
      arcu libero, iaculis non auctor non, sagittis ac nulla. Aenean ligula
      purus, sodales eu lectus vitae, venenatis consectetur turpis. In sit amet
      urna nec ligula suscipit viverra. In accumsan ultrices magna et tincidunt.
      Morbi dui lorem, tristique at semper eu, rhoncus varius ex. Sed semper,
      tellus nec interdum tempor, velit enim maximus sem, quis ornare tortor est
      elementum tellus. Praesent ultrices varius nunc lobortis blandit. Ut odio
      est, sodales at pellentesque sit amet, condimentum ut metus. Sed in congue
      mi. Integer dignissim felis vel lacus vehicula consequat. Aenean cursus
      urna eu eros blandit volutpat. Maecenas quis scelerisque sem.
    </p>
  </article>
  <article class="article-container">
    <h3>Today in Sports: Home Team Wins Big!</h3>
    <img src="sports" alt="Sports news image" />
    <p>
      Aliquam ut metus interdum, posuere magna mattis, hendrerit ex. Proin sit
      amet neque non ipsum elementum vehicula semper pellentesque odio. Aenean
      mattis fringilla eros, et tristique libero mattis sollicitudin. Quisque
      rutrum mauris at velit semper, nec varius dui pellentesque. Morbi congue
      viverra ligula in viverra. Curabitur et arcu tempor, efficitur eros nec,
      rhoncus tellus. Nullam ut hendrerit turpis. Suspendisse molestie quis
      lectus vel vestibulum. Maecenas purus felis, finibus at fringilla in,
      mattis accumsan magna.
    </p>
  </article>
</main>
<footer>&copy; 2025 News News News!</footer>
```

---

### **2. Add ARIA Attributes**

Use ARIA attributes to enhance accessibility for assistive technologies.

- Add an `aria-label` to the navigation menu to describe its purpose:
  - Label it as "Main navigation menu."
- Add a `role="article"` to explicitly define the articles.

```html
<ul class="main-menu" aria-label="Main navigation menu">
  <li>Home</li>
  <li>Sports</li>
  <li>World Events</li>
  <li>Entertainment</li>
</ul>

<article class="article-container" role="article">
  <h3>Breaking News: New Fruit Discovered!</h3>
  <p>Lorem ipsum dolor sit amet...</p>
</article>
<article class="article-container" role="article">
  <h3>Today in Sports: Home Team Wins Big!</h3>
  <img src="sports" alt="Sports news image" />
  <p>Aliquam ut metus interdum...</p>
</article>
```

---
