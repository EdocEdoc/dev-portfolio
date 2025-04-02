# Customization Guide

This document provides detailed instructions for customizing the portfolio template to fit your personal brand and information.

## 🎨 Styling Customization

### Color Scheme

The portfolio uses CSS variables to manage the color scheme. To change colors, edit the `:root` section in the CSS:

```css
:root {
  --primary-purple: #646cff;
  --primary-purple-hover: #747bff;
  --gradient-1: linear-gradient(45deg, #bd34fe 30%, #41d1ff);
  --gradient-2: linear-gradient(45deg, #ffdb4d, #ff7730);
  --dark-bg: #242424;
  --light-text: rgba(255, 255, 255, 0.87);
  --card-bg: #1a1a1a;
  --border-color: rgba(255, 255, 255, 0.1);
}
```

### Typography

To change fonts, modify the font-family property in the CSS. The current setup uses the system font stack:

```css
* {
  font-family: "Inter", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}
```

To use a custom web font:

1. Add the font import at the top of your CSS file:

   ```css
   @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap");
   ```

2. Update the font-family property:
   ```css
   * {
     font-family: "Poppins", sans-serif;
   }
   ```

## 📝 Content Customization

### Personal Information

Update your personal information in the header section of `index.html`:

```html
<header>
  <div class="profile">
    <img src="path/to/your/photo.jpg" alt="Your Name" />
  </div>
  <h1 class="name">Your Name</h1>
  <h2 class="title">Your Title</h2>
  <div class="contact">
    <!-- Contact information -->
  </div>
</header>
```

### Profile Summary

Modify the summary section to reflect your professional profile:

```html
<section class="section">
  <p class="summary">Your professional summary goes here...</p>
</section>
```

### Work Experience

Each work experience is contained in a card. To add or modify experience:

```html
<div class="card">
  <div class="card-header">
    <div>
      <h3 class="card-title">Position Title</h3>
      <p class="card-subtitle">Company Name</p>
    </div>
    <p class="card-date">Duration</p>
  </div>
  <div class="card-content">
    <ul>
      <li>Achievement or responsibility</li>
      <!-- More list items -->
    </ul>
  </div>
  <div class="skill-tags">
    <span class="skill-tag">Skill 1</span>
    <!-- More skill tags -->
  </div>
</div>
```

### Projects

Projects follow a similar structure to work experience:

```html
<div class="card project-card">
  <div class="card-header">
    <div>
      <h3 class="card-title">Project Name</h3>
      <p class="card-subtitle">Client or Context</p>
    </div>
    <p class="card-date">Date</p>
  </div>
  <div class="card-content">
    <!-- Project description -->
  </div>
  <div class="skill-tags">
    <!-- Technologies used -->
  </div>
</div>
```

### Skills

Update the skills sections according to your expertise:

```html
<div class="skills-category">
  <h3>Category Name</h3>
  <ul class="skills-list">
    <li>Skill 1</li>
    <!-- More skills -->
  </ul>
</div>
```

## 🖼️ Images

### Profile Photo

Replace the placeholder with your actual photo:

1. Add your photo to an `images` folder
2. Update the image path in the header section:
   ```html
   <img src="images/your-photo.jpg" alt="Your Name" />
   ```

For best results, use a square image of at least 300x300 pixels.

### Project Screenshots

To add project screenshots:

1. Create a card for your project
2. Add an image within the card content:

   ```html
   <div class="card-content">
     <img
       src="images/project-screenshot.jpg"
       alt="Project Name"
       class="project-image"
     />
     <p>Project description...</p>
   </div>
   ```

3. Add appropriate CSS for the project image:
   ```css
   .project-image {
     width: 100%;
     border-radius: 6px;
     margin-bottom: 1rem;
   }
   ```

## 📱 Responsive Customization

The portfolio is already responsive, but you can further customize the behavior at different screen sizes:

```css
@media (max-width: 768px) {
  /* Tablet customizations */
}

@media (max-width: 480px) {
  /* Mobile phone customizations */
}
```

## 🔌 Adding Interactive Elements

### Smooth Scrolling

Add smooth scrolling to internal links:

```css
html {
  scroll-behavior: smooth;
}
```

### Animation on Scroll

To add animations when elements enter the viewport, you can:

1. Add this simple JavaScript at the end of your HTML file:

   ```html
   <script>
     document.addEventListener("DOMContentLoaded", function () {
       const observer = new IntersectionObserver((entries) => {
         entries.forEach((entry) => {
           if (entry.isIntersecting) {
             entry.target.classList.add("show");
           }
         });
       });

       const hiddenElements = document.querySelectorAll(".hidden");
       hiddenElements.forEach((el) => observer.observe(el));
     });
   </script>
   ```

2. Add these CSS classes:

   ```css
   .hidden {
     opacity: 0;
     transform: translateY(20px);
     transition: all 0.6s;
   }

   .show {
     opacity: 1;
     transform: translateY(0);
   }
   ```

3. Add the `hidden` class to elements you want to animate:
   ```html
   <div class="card hidden">
     <!-- Content -->
   </div>
   ```

## ⚙️ Advanced Customization

For more advanced customization, consider:

1. Adding a light/dark mode toggle
2. Implementing a project filter system
3. Creating a contact form with form validation
4. Adding a blog section with categorized posts

Remember to keep your website's loading time minimal by optimizing images and minimizing unnecessary scripts or resources.

---

If you need further assistance with customization, feel free to contact me at vagenodipa@gmail.com.
