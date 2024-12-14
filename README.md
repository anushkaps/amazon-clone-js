# Amazon Home Page Clone
[LIVE DEMO](https://anushkaps.github.io/amazon-clone-js/)

## Overview
This project is a single-page clone of the Amazon homepage. I created it to practice and enhance my HTML, CSS, and basic JavaScript skills. It is a visually accurate replica of Amazon's homepage, focusing on layout, design, and interactivity.

---

## Features

### Design Features
- **Responsive Layout**: Ensures the page adjusts well to different screen sizes.
- **Dynamic Product Sliders**: Multiple horizontally scrollable product sections with navigation buttons.
- **Sticky Back-to-Top Button**: Smooth scroll functionality to bring the user back to the top of the page.

### Interactive Elements
- **Sidebar Menu**: A collapsible sidebar for navigation, activated by a button.
- **Sign-In Dropdown**: A dropdown menu triggered by the sign-in button.

---

## Technologies Used
- **HTML**: For structuring the content of the page.
- **CSS**: For styling and layout.
- **JavaScript**: For adding interactivity and enhancing the user experience.

---

## JavaScript Highlights
Below are the key functionalities implemented using JavaScript:

1. **Horizontal Scrolling for Product Sliders**:
   ```javascript
   const leftBtn = document.querySelector(".l-btn");
   const rightBtn = document.querySelector(".r-btn");

   rightBtn.addEventListener("click", function(event) {
       const content = document.querySelector(".product-slide");
       content.scrollLeft += 1100;
       event.preventDefault();
   });

   leftBtn.addEventListener("click", function(event) {
       const content = document.querySelector(".product-slide");
       content.scrollLeft -= 1100;
       event.preventDefault();
   });
   ```
   - Similar logic is applied to other product sliders to enable seamless horizontal scrolling.

2. **Back-to-Top Button**:
   ```javascript
   const backtop = document.querySelector(".backtop");

   backtop.addEventListener("click", () => {
       window.scrollTo({
           top: 0,
           behavior: "smooth"
       });
   });
   ```

3. **Sidebar Menu**:
   ```javascript
   const sidebar = document.querySelector(".sidebar");
   const cross = document.querySelector(".fa-xmark");
   const black = document.querySelector(".black");
   const sidebtn = document.querySelector(".second-1");

   sidebtn.addEventListener("click", () => {
       sidebar.classList.add("active");
       cross.classList.add("active");
       black.classList.add("active");
       document.body.classList.add("stop-scroll");
   });

   cross.addEventListener("click", () => {
       sidebar.classList.remove("active");
       cross.classList.remove("active");
       black.classList.remove("active");
       document.body.classList.remove("stop-scroll");
   });
   ```

4. **Sign-In Dropdown**:
   ```javascript
   const sign = document.querySelector(".ac");
   const tri = document.querySelector(".triangle");
   const signin = document.querySelector(".hdn-sign");

   sign.addEventListener("click", () => {
       black.classList.toggle("active-1");
       signin.classList.toggle("active");
       tri.classList.toggle("active");
       document.body.classList.toggle("stop-scroll");
   });
   ```

---

## Challenges Faced
- Ensuring the layout is responsive across all devices.
- Accurately replicating the design of the original Amazon homepage.
- Implementing smooth scrolling and interactive elements.

---

## What I Learned
- Improved understanding of HTML structure and semantics.
- Advanced CSS techniques for layout and responsiveness.
- Utilizing JavaScript for DOM manipulation and event handling.

---

## Future Enhancements
- Add more interactivity, such as live search and filtering options.
- Optimize the JavaScript for better performance.
- Include more pages like product details and checkout.

---

## How to Run the Project
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/amazon-homepage-clone.git
   ```
2. Open the `index.html` file in any modern browser.
3. Explore the design and functionality.

---

## Screenshots
### Homepage View
![image](https://github.com/user-attachments/assets/027f29d1-25a6-4f01-89db-73cf493126cd)

![image](https://github.com/user-attachments/assets/19875fd0-951a-4662-9a59-9289572767fe)


---

## Acknowledgments
This project was inspired by Amazon's homepage. It was built solely for educational purposes and to practice front-end development skills.

