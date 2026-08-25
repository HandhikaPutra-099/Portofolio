# Personal Portfolio Website

A modern, professional, and responsive personal portfolio website for **Handhika Putra Wijaya Kesuma**.

## 🎯 Overview

This portfolio showcases web development and backend development skills with a clean, minimalist design. Built using pure HTML, CSS, and JavaScript without any heavy frameworks.

## 📁 Folder Structure

```
portfolio/
├── index.html          # Main HTML file
├── css/
│   └── style.css       # All styling and animations
├── js/
│   └── script.js       # Interactive features and animations
├── assets/
│   ├── images/         # Project screenshots and images
│   │   ├── admin-dashboard.png
│   │   ├── calculator.png
│   │   ├── etch-a-sketch.png
│   │   └── rock-scissors-paper.png
│   └── icons/          # Custom icons (if needed)
└── README.md           # This file
```

## 🚀 Features

### Design
- **Modern Dark Theme**: Navy/charcoal background with light text and blue accent color
- **Clean Typography**: Inter font family for professional appearance
- **Responsive Layout**: Works on desktop, tablet, and mobile devices
- **Smooth Animations**: Fade-in effects, hover animations, and scroll reveals

### Sections
1. **Hero**: Introduction with name, title, description, and CTA buttons
2. **About Me**: Personal introduction and background
3. **Projects**: Project cards with thumbnails, descriptions, technologies, and links
4. **Skills**: Organized skill categories (Frontend, Backend, Database, Tools, UI/UX)
5. **Contact**: Contact information with clickable links
6. **Footer**: Copyright and social media links

### Interactions
- Mobile hamburger menu navigation
- Smooth scrolling to sections
- Active navigation highlighting
- Project card hover effects with image zoom
- Skill badge hover animations
- Button ripple effects
- Scroll-triggered reveal animations
- Parallax effect on hero section

## 🛠️ Customization Guide

### 1. Adding Your Profile Photo

To add your profile photo in the hero section:

1. Place your photo in `assets/images/` folder (e.g., `profile.jpg`)
2. Open `index.html`
3. Find the `.hero-image-placeholder` div (around line 47-54)
4. Replace it with:
```html
<div class="hero-visual">
    <img src="assets/images/profile.jpg" alt="Handhika Putra Wijaya Kesuma" class="hero-profile-image">
</div>
```
5. Add this CSS to `style.css`:
```css
.hero-profile-image {
    width: 350px;
    height: 350px;
    object-fit: cover;
    border-radius: 50%;
    border: 3px solid var(--color-accent);
}
```

### 2. Adding or Editing Projects

To add a new project:

1. Open `index.html`
2. Find the Projects section (around line 75)
3. Copy an existing project card structure
4. Modify the following fields:
   - `src` attribute of the `<img>` tag (project thumbnail)
   - `alt` attribute (project name for accessibility)
   - `<h3>` project title
   - `<p>` project description
   - Tech badges in `.project-tech`
   - Live Demo URL (if available)
   - GitHub URL

**Example Project Card:**
```html
<article class="project-card">
    <div class="project-image">
        <img src="assets/images/your-project.png" alt="Your Project Name">
    </div>
    <div class="project-content">
        <h3 class="project-title">Your Project Name</h3>
        <p class="project-description">Your project description here.</p>
        <div class="project-tech">
            <span class="tech-badge">HTML</span>
            <span class="tech-badge">CSS</span>
            <span class="tech-badge">JavaScript</span>
        </div>
        <div class="project-links">
            <a href="[LIVE DEMO URL]" class="btn btn-small" target="_blank" rel="noopener noreferrer">Live Demo</a>
            <a href="[GITHUB URL]" class="btn btn-small btn-outline" target="_blank" rel="noopener noreferrer">GitHub</a>
        </div>
    </div>
</article>
```

**Note:** If a project only has GitHub (no live demo), simply remove the Live Demo button.

### 3. Adding Project Images

1. Take screenshots of your projects (recommended size: 1280x720px or 16:9 ratio)
2. Save them in `assets/images/` folder
3. Name them appropriately (e.g., `project-name.png`)
4. Update the `src` attribute in the corresponding project card

### 4. Updating Contact Information

All contact information is located in the Contact section of `index.html` (around line 200):

- **Email**: Change the `href="mailto:your-email@gmail.com"` and display text
- **Phone**: Change the `href="tel:+6285640488817"` and display text
- **LinkedIn**: Update the LinkedIn URL
- **GitHub**: Update the GitHub URL

Also update the footer social links accordingly.

### 5. Modifying Skills

To add or remove skills:

1. Open `index.html`
2. Find the Skills section (around line 160)
3. Add or remove `<span class="skill-badge">Skill Name</span>` elements within each category

### 6. Changing Colors

To customize the color scheme, edit the CSS variables in `style.css` (lines 7-20):

```css
:root {
    --color-bg-primary: #0f172a;      /* Main background */
    --color-bg-secondary: #1e293b;    /* Section backgrounds */
    --color-bg-tertiary: #334155;     /* Cards and badges */
    --color-text-primary: #f8fafc;    /* Main text */
    --color-text-secondary: #cbd5e1;  /* Secondary text */
    --color-text-muted: #94a3b8;      /* Muted text */
    --color-accent: #38bdf8;          /* Accent color (buttons, highlights) */
    --color-accent-hover: #0ea5e9;    /* Accent hover state */
    --color-border: #475569;          /* Borders */
}
```

## 🌐 Deployment to GitHub Pages

### Step 1: Prepare Your Repository

1. Create a new repository on GitHub (e.g., `portfolio`)
2. Initialize Git in your portfolio folder (if not already done):
   ```bash
   cd portfolio
   git init
   ```

### Step 2: Add and Commit Files

```bash
git add .
git commit -m "Initial commit: Portfolio website"
```

### Step 3: Connect to GitHub

```bash
git remote add origin https://github.com/HandhikaPutra-099/portfolio.git
git branch -M main
git push -u origin main
```

### Step 4: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on **Settings** tab
3. In the left sidebar, click on **Pages**
4. Under "Source", select:
   - Branch: `main`
   - Folder: `/ (root)`
5. Click **Save**

### Step 5: Access Your Website

After a few minutes, your website will be live at:
```
https://handhikaputra-099.github.io/portfolio/
```

### Alternative: Deploy from Root

If you want to deploy directly from the root of your repository:

1. Move all files from the `portfolio/` folder to the repository root
2. Follow steps 2-5 above

## 📱 Responsive Breakpoints

The website is optimized for the following screen sizes:

- **Desktop**: 992px and above
- **Tablet**: 768px - 991px
- **Mobile**: Below 768px

## ✨ Animation Details

### Included Animations:
- **Fade-in on scroll**: Elements appear as you scroll down
- **Hover effects**: Buttons, cards, and badges animate on hover
- **Image zoom**: Project images subtly zoom when hovering over cards
- **Parallax**: Hero visual element moves slightly on scroll
- **Ripple effect**: Buttons show a ripple when clicked
- **Navigation underline**: Animated underline on nav link hover

### Performance Notes:
- Scroll events are debounced for better performance
- CSS transitions are hardware-accelerated
- No external animation libraries used

## 🔧 Browser Support

The website works on all modern browsers:
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 📝 License

© 2026 Handhika Putra Wijaya Kesuma. All rights reserved.

## 🤝 Contact

- **Email**: putrajayasuma@gmail.com
- **Phone**: +62856-4048-8817
- **LinkedIn**: www.linkedin.com/in/handhikaputra
- **GitHub**: https://github.com/HandhikaPutra-099

---

Built with ❤️ by Handhika Putra Wijaya Kesuma
