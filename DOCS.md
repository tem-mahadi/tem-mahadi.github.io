# Developer Documentation

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [File Descriptions](#file-descriptions)
- [Setup Instructions](#setup-instructions)
- [Customization Guide](#customization-guide)
- [Code Architecture](#code-architecture)
- [Browser Compatibility](#browser-compatibility)
- [Performance Optimization](#performance-optimization)
- [Troubleshooting](#troubleshooting)

---

## 🎯 Project Overview

This is a modern, responsive personal portfolio website built with vanilla HTML, CSS, and JavaScript. The project showcases a mobile app developer's work, skills, and achievements with smooth animations and an intuitive user interface.

### Key Features

- **Theme Switching**: Dark/Light mode toggle with localStorage persistence
- **Responsive Design**: Mobile-first approach with breakpoints at 968px and 480px
- **Interactive Animations**: Typing effect, scroll animations, parallax effects
- **Performance**: Lightweight with minimal dependencies
- **SEO Optimized**: Proper meta tags and semantic HTML

---

## 📂 Project Structure

```
MyPortfolio/
├── index.html              # Main HTML file
├── css/
│   └── styles.css         # All styles and animations
├── js/
│   └── script.js          # All JavaScript functionality
├── assets/
│   ├── images/            # Portfolio images (add your images here)
│   └── icons/             # Custom icons (if any)
├── README.md              # Project documentation
├── CONTRIBUTING.md        # Contribution guidelines
├── CHANGELOG.md           # Version history
├── LICENSE                # MIT License
└── .gitignore            # Git ignore file
```

---

## 🛠️ Technologies Used

### Core Technologies

- **HTML5**: Semantic markup, accessibility features
- **CSS3**:
  - CSS Grid & Flexbox for layouts
  - CSS Custom Properties (variables) for theming
  - CSS Animations and Transitions
  - Media queries for responsiveness
- **JavaScript (ES6+)**:
  - DOM manipulation
  - Event handling
  - Local storage API
  - Intersection Observer API

### External Libraries

- **Font Awesome 6.4.0**: Icons
- **Google Fonts**: Poppins font family

---

## 📄 File Descriptions

### `index.html`

Main HTML structure containing:

- Navigation bar with theme toggle
- Hero section with animated introduction
- About section with personal info and stats
- Skills section organized by categories
- Projects showcase with 4 featured projects
- GitHub statistics section
- Contact form and social links
- Footer with site links

**Key Sections:**

```html
<nav>
  <!-- Navigation -->
  <section#hero>
    <!-- Hero/Landing -->
    <section#about>
      <!-- About Me -->
      <section#skills>
        <!-- Skills & Tech -->
        <section#projects>
          <!-- Featured Projects -->
          <section#github-stats>
            <!-- GitHub Stats -->
            <section#contact>
              <!-- Contact Form -->
              <footer><!-- Footer --></footer></section#contact
            ></section#github-stats
          ></section#projects
        ></section#skills
      ></section#about
    ></section#hero
  >
</nav>
```

### `css/styles.css`

Complete styling document organized by:

1. **CSS Variables** (Lines ~1-25)

   - Color scheme definitions
   - Theme-specific variables

   ```css
   :root {
     --primary-color: #00d9ff;
     --secondary-color: #ff6b6b;
     /* ... */
   }
   ```

2. **Reset & Base Styles** (Lines ~26-50)

   - Universal reset
   - Base body styles
   - Typography

3. **Components** (Lines ~51+)

   - Navigation
   - Hero section
   - About section
   - Skills section
   - Projects section
   - Contact section
   - Footer

4. **Utilities**
   - Animations (@keyframes)
   - Responsive breakpoints
   - Helper classes

### `js/script.js`

JavaScript functionality including:

**Main Features:**

1. **Theme Toggle** - Dark/Light mode with localStorage
2. **Mobile Navigation** - Hamburger menu functionality
3. **Scroll Effects** - Navbar hide/show, active link highlighting
4. **Typing Animation** - Rotating text in hero section
5. **Form Handling** - Contact form submission
6. **Smooth Scrolling** - Anchor link navigation
7. **Back to Top Button** - Scroll to top functionality
8. **Animations** - Scroll-triggered animations (AOS-like)
9. **Stats Counter** - Animated number counting
10. **Easter Egg** - Konami code implementation

**Key Functions:**

```javascript
// Theme management
updateThemeIcon(theme);

// Animations
type(); // Typing animation
animateOnScroll(); // Scroll animations
animateCircles(); // Cursor trail
```

---

## 🚀 Setup Instructions

### 1. Clone or Download

```bash
git clone https://github.com/tem-mahadi/portfolio.git
cd MyPortfolio
```

### 2. Open in Browser

**Option A: Direct File Access**

- Double-click `index.html`
- Or right-click → Open with → Browser

**Option B: Local Server (Recommended)**

```bash
# Python
python -m http.server 8000

# Node.js
npx serve

# PHP
php -S localhost:8000
```

### 3. View

Open `http://localhost:8000` in your browser

---

## 🎨 Customization Guide

### Changing Colors

Edit CSS variables in `css/styles.css`:

```css
:root {
  --primary-color: #00d9ff; /* Main accent color */
  --secondary-color: #ff6b6b; /* Secondary accent */
  --accent-color: #4ecdc4; /* Additional accent */
  --bg-primary: #0a0e27; /* Dark background */
  --bg-secondary: #141937; /* Section background */
  --text-primary: #ffffff; /* Main text */
  --text-secondary: #b8b8d1; /* Secondary text */
}
```

### Adding/Removing Sections

1. **HTML Structure:**

```html
<section class="your-section" id="your-section">
  <div class="container">
    <div class="section-header">
      <span class="section-tag">Your Tag</span>
      <h2 class="section-title">Section Title</h2>
      <div class="title-underline"></div>
    </div>
    <!-- Your content -->
  </div>
</section>
```

2. **Add to Navigation:**

```html
<a href="#your-section" class="nav-link">Your Section</a>
```

3. **Style in CSS:**

```css
.your-section {
  padding: 100px 20px;
  background: var(--bg-secondary);
}
```

### Updating Personal Information

**Location: `index.html`**

1. **Name & Title** (Line ~42-48)
2. **Social Links** (Line ~62-78)
3. **About Section** (Line ~103+)
4. **Skills** (Line ~180+)
5. **Projects** (Line ~280+)
6. **Contact Info** (Line ~440+)

### Adding Images

Place images in `assets/images/` and reference:

```html
<img src="assets/images/your-image.jpg" alt="Description" />
```

---

## 🏗️ Code Architecture

### CSS Architecture

**Naming Convention:** BEM-inspired

```css
.block {
}
.block__element {
}
.block--modifier {
}
```

**Example:**

```css
.hero {
} /* Block */
.hero-content {
} /* Element */
.hero-text {
} /* Element */
.btn--primary {
} /* Modifier */
```

### JavaScript Architecture

**Module Pattern:**

- Event listeners at the bottom
- Pure functions for reusability
- No global pollution

**Performance Considerations:**

- Debouncing scroll events
- Request Animation Frame for animations
- Lazy loading for images (can be added)

---

## 🌐 Browser Compatibility

### Supported Browsers

| Browser | Version | Support |
| ------- | ------- | ------- |
| Chrome  | 90+     | ✅ Full |
| Firefox | 88+     | ✅ Full |
| Safari  | 14+     | ✅ Full |
| Edge    | 90+     | ✅ Full |
| Opera   | 76+     | ✅ Full |

### Fallbacks

- CSS Grid → Flexbox fallback
- CSS Variables → Hardcoded colors (can be added)
- Modern JS → Babel transpilation (if needed)

---

## ⚡ Performance Optimization

### Current Optimizations

1. **CSS**

   - Single CSS file (no imports)
   - Minimal specificity
   - Hardware-accelerated animations (`transform`, `opacity`)

2. **JavaScript**

   - Vanilla JS (no framework overhead)
   - Event delegation where possible
   - Debounced scroll handlers

3. **Assets**
   - External images via CDN
   - Font Awesome CDN
   - Google Fonts optimized loading

### Further Improvements (Optional)

```html
<!-- Add to <head> for better loading -->
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://cdnjs.cloudflare.com" />
<link rel="dns-prefetch" href="https://github.com" />
```

---

## 🐛 Troubleshooting

### Images Not Loading

**Problem:** External image URLs broken
**Solution:**

1. Check internet connection
2. Verify URL is still valid
3. Use local images in `assets/images/`

### Theme Toggle Not Working

**Problem:** Theme doesn't persist or change
**Solution:**

1. Check browser console for errors
2. Verify localStorage is enabled
3. Clear browser cache

### Mobile Menu Not Opening

**Problem:** Hamburger menu doesn't work
**Solution:**

1. Check JavaScript is loaded
2. Verify event listeners attached
3. Check browser console for errors

### Animations Not Smooth

**Problem:** Janky animations
**Solution:**

1. Use hardware-accelerated properties
2. Avoid animating `width`, `height`, `left`, `top`
3. Use `transform` and `opacity` instead

### Contact Form Not Working

**Problem:** Form doesn't send email
**Solution:**
Currently uses `mailto:` link. For real form:

1. Add backend (Node.js, PHP, etc.)
2. Use service like Formspree, EmailJS
3. Or integrate with Firebase

---

## 📝 Code Standards

### HTML

- Use semantic tags (`<nav>`, `<section>`, `<article>`)
- Include ARIA labels for accessibility
- Valid HTML5 markup

### CSS

- Mobile-first responsive design
- BEM-like naming convention
- Organized by components
- Use CSS variables for theming

### JavaScript

- ES6+ syntax
- Descriptive function/variable names
- Comments for complex logic
- No inline event handlers

---

## 🔧 Build Tools (Optional Future Enhancement)

Currently, the project uses vanilla code. For scaling:

### Potential Tools

- **Build**: Webpack, Parcel, or Vite
- **CSS Preprocessing**: Sass or PostCSS
- **JS Transpiling**: Babel
- **Minification**: Terser, cssnano
- **Linting**: ESLint, Stylelint
- **Formatting**: Prettier

---

## 📚 Additional Resources

### Learning Resources

- [MDN Web Docs](https://developer.mozilla.org/)
- [CSS-Tricks](https://css-tricks.com/)
- [JavaScript.info](https://javascript.info/)

### Tools

- [Can I Use](https://caniuse.com/) - Browser compatibility
- [PageSpeed Insights](https://pagespeed.web.dev/) - Performance testing
- [Wave](https://wave.webaim.org/) - Accessibility testing

---

## 📞 Support

For questions or issues:

- **Email**: mahadi4uruetcse21@gmail.com
- **GitHub**: [@tem-mahadi](https://github.com/tem-mahadi)
- **LinkedIn**: [hasan-al-mahadi](https://www.linkedin.com/in/hasan-al-mahadi/)

---

**Last Updated:** October 21, 2025
**Version:** 1.0.0
