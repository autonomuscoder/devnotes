You can use JavaScript to check the size of the screen a website is being viewed on and implement different logic based on that size. Here's how:

**Using `window.innerWidth` and `window.innerHeight`:**

These properties provide the width and height of the browser window (usable viewport area, excluding toolbars).

JavaScript

```
function checkScreenSize() {
  const width = window.innerWidth;
  const height = window.innerHeight;

  // Define your breakpoints for different screen sizes (in pixels)
  const isMobile = width <= 600; // Example breakpoint for mobile

  if (isMobile) {
    // Set logic for mobile screens (e.g., simpler animation)
    console.log("Mobile screen detected, using simpler animation");
  } else {
    // Set logic for larger screens (e.g., more complex animation)
    console.log("Larger screen detected, using complex animation");
  }
}

// Call the function on page load or resize event
checkScreenSize();
window.addEventListener("resize", checkScreenSize);
```

**Explanation:**

1. The `checkScreenSize` function gets the window width and height.
2. You define breakpoints (ranges) for different screen sizes (e.g., mobile <= 600px).
3. An `if` statement checks if the width is less than or equal to the mobile breakpoint.
4. Based on the condition, you can implement different logic for mobile and larger screens.

**Alternative: Using Media Queries**

Media queries are a CSS feature that allows you to define styles based on screen size and other characteristics. This approach keeps your JavaScript cleaner:

CSS

```
/* Styles for mobile screens */
@media only screen and (max-width: 600px) {
  .animation {
    animation: simplerAnimation 2s ease-in-out infinite;
  }
}

/* Styles for larger screens */
@media only screen and (min-width: 601px) {
  .animation {
    animation: complexAnimation 4s ease-in-out infinite;
  }
}
```

In this example, the CSS defines two animation styles depending on the screen size.

**Choosing the right approach:**

- If you need dynamic logic based on screen size that goes beyond just styling (e.g., showing/hiding elements), JavaScript with breakpoints is a good choice.
- For purely visual adjustments based on screen size, media queries offer a cleaner separation of concerns and better maintainability.