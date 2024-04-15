html:
![[carousel-html.png]]


css:
.image-slider {
  height: 100vh;
  position: relative;
  .full-image .images {
    position: absolute;
    inset: 0;
    overflow: hidden;
    opacity: 0;
    transition: all ease 0.5s;
    img {
      height: 100%;
      width: 100%;
      object-fit: cover;
    }
  }
  .images.active {
    opacity: 1;
    z-index: 10;
  }
  .text-wrapper {
    position: absolute;
    left: 5%;
    top: 60%;
    z-index: 1;
  }
}
.full-image .images::after {
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  left: 0;
  bottom: 0;
  background: linear-gradient(to top, #000 40%, transparent);
}




#### javascript:

const imageSlider = document.querySelector('.image-slider');
const images = imageSlider.querySelectorAll('.images');
let currentIndex = 0;

function changeActiveSlide() {
  images.forEach(image => image.classList.remove('active'));
  images[currentIndex].classList.add('active');
  currentIndex = (currentIndex + 1) % images.length;
}

changeActiveSlide(); // Set initial slide

setInterval(changeActiveSlide, 3000); // Change slide every 3 seconds (adjust as needed)

confusion: What does the line <i>currentIndex = (currentIndex + 1) % images.length;"</i> do?

soln: This line of code, `currentIndex = (currentIndex + 1) % images.length;`, is used to update the `currentIndex` variable in a controlled way, ensuring it stays within the valid range for the image elements. Here's a breakdown:

1. **`currentIndex + 1`**: This part calculates the next potential index for the current slide. It simply adds 1 to the current value of `currentIndex`.
    
2. **Modulo (`%`)**: The modulo operator (`%`) calculates the remainder after a division. Here, it's used with `images.length`.
    
3. **`images.length`**: This refers to the total number of image elements (`<div class="images">`) present within the `images` variable (previously selected using `querySelectorAll`).
    

**Putting it together:**

- The code first calculates the potential next index by adding 1 to `currentIndex`.
- Then, it uses the modulo operator (`%`) with `images.length`. This ensures the resulting index is always within the valid range of image elements (from 0 to `images.length - 1`).

**Example:**

- Let's say you have 3 images (so `images.length` is 3).
- If `currentIndex` is currently 2 (representing the last image), adding 1 would result in 3.
- However, `3 % 3` equals 0. This effectively "wraps around" and sets the `currentIndex` back to 0, ensuring it points to the first image again.

**Benefits:**

- This approach avoids potential errors that could occur if `currentIndex` goes beyond the valid image count.
- It allows for smooth cycling through all images without needing to check for specific boundaries.