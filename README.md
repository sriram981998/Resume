# 📄 Sriram - Full Stack Developer Resume

Welcome to my resume repository! A modern, single-file, responsive resume hosted on GitHub with an embedded PDF download feature.

## 🌟 Features

- ✨ **Modern Design** - Professional gradient header with clean typography
- 📱 **Fully Responsive** - Adapts perfectly to desktop, tablet, and mobile devices
- 📥 **One-Click PDF Export** - Download as PDF directly from the browser with full color preservation
- 🎨 **Single-File** - All HTML, CSS, and JavaScript in one file (no external dependencies)
- 🚀 **Fast Loading** - Lightweight and optimized for performance
- 🖨️ **Print-Optimized** - Perfect print styling with theme-aware colors (dark/light mode support)
- 💼 **ATS-Friendly** - Clean semantic HTML for applicant tracking systems

## 📋 What's Inside

The resume includes the following sections:

- **Home/Welcome** - Introduction and overview
- **Professional Summary** - Brief overview of expertise with key highlights
- **Experience** - Detailed work history with achievements and technologies used
- **Projects** - Portfolio of significant projects with descriptions
- **Skills** - Organized by categories with visual tags
- **Education** - Academic background and achievements

## 🚀 Quick Start

### View Online

Open `index.html` in any modern web browser:

```bash
# Clone the repository
git clone https://github.com/sriram981998/Resume.git
cd Resume

# Open in browser (Linux/Mac)
open index.html

# Or use Python to run a local server (recommended)
python -m http.server 8000
# Then visit http://localhost:8000
```

### Download as PDF

Simply click the **"📥 Download as PDF"** button on the resume. The PDF will be saved as `Sriram_Resume.pdf`.

**Note:** The PDF download uses the [html2pdf](https://ekoopmans.github.io/html2pdf.js/) library, which runs entirely in your browser. No server processing needed!

## 🎨 Customization Guide

Since this is a single-file resume, all edits happen in `index.html`. Follow these steps to personalize it:

### 1. Update Your Information

Open `index.html` in your text editor and find the `<div class="header">` section:

```html
<h1>Sriram</h1>
<p class="title">Full Stack Developer</p>
<div class="contact">
    <span>📧 email@example.com</span>
    <span>📱 +1 (555) 123-4567</span>
    <span>💻 <a href="https://github.com/yourusername">github.com/yourusername</a></span>
</div>
```

Update with your name, title, email, phone, and GitHub URL.

### 2. Edit Content Sections

Each section is clearly labeled:

- **Professional Summary** - Update the description paragraph
- **Experience** - Add/remove job entries with accomplishments
- **Skills** - Update skill categories and technologies
- **Education** - Add your university, degree, and GPA
- **Certifications** - List your professional certifications

## 🎨 Interactive Features

### 🌓 Dark/Light Mode Toggle
- **Smart Theme Switching** - Toggle between dark and light modes with a click
- **Persistent Preference** - Your theme choice is saved in browser storage
- **Theme-Aware Printing** - When you download as PDF:
  - Dark mode prints with dark background and light text
  - Light mode prints with white background and dark text
  - All colors are preserved exactly as displayed

### 📱 Responsive Sidebar Navigation
- **Mobile-Friendly** - Hamburger menu on smaller screens
- **Smooth Scrolling** - Click any navigation item to smoothly scroll to that section
- **Active Highlighting** - Current section is highlighted as you scroll
- **Fixed Sidebar** - Navigation always accessible on desktop

### 📥 Advanced PDF Download
- **No External Libraries** - Uses native browser print functionality
- **Full Color Preservation** - All colors, gradients, and styling preserved in PDF
- **Theme-Aware Output** - PDF respects your current dark/light mode preference
- **Professional Formatting** - Cards, tags, and highlights render perfectly
- **Client-Side Generation** - No server uploads, completely private

### 4. Modify Typography

Change font sizes, weights, or families in the CSS section. For example:

```css
.header h1 {
    font-size: 32px;  /* Change to your preferred size */
}

body {
    font-family: /* your font here */;
}
```

### 5. Adjust Layout

The resume uses CSS Grid and Flexbox. Key layout classes:

- `.container` - Main wrapper (max-width: 840px)
- `.resume` - Card container with shadow
- `.two-col` - Two-column grid for skills section
- `.content` - Main content area with padding

### 6. Add/Remove Sections

To add a new section, copy this template:

```html
<section class="section">
    <h2>Section Title</h2>
    <p>Your content here...</p>
</section>
```

To remove a section, simply delete the entire `<section>` block.

## 📥 PDF Download Guide

### How to Download

1. **Click the "Download Resume" button** in the sidebar (or on mobile, in the hamburger menu)
2. **Choose "Save as PDF"** in the print dialog that appears
3. **Your resume downloads** with all colors and formatting preserved

### What You Get

✅ **Colors & Styling Preserved** - All gradients, card colors, and text colors render perfectly
✅ **Theme-Aware** - If you're in dark mode, the PDF prints in dark mode; light mode prints light
✅ **Professional Formatting** - Cards, tags, icons, and spacing all look professional
✅ **No Dependencies** - Uses browser's native print function (no external PDF libraries)
✅ **Completely Private** - Generated entirely in your browser; nothing uploaded to servers

### Print Quality Tips

- **Use Chrome/Edge** - Best print output quality
- **Disable Headers/Footers** - In print settings, turn off header/footer for cleaner output
- **Save as PDF** - Select "Save as PDF" instead of printing to paper
- **Check Preview** - Most browsers show a preview before saving; verify it looks good

## 🎨 Design & Customization

### Color Scheme

The resume uses a modern blue gradient design with theme support:

- **Primary Accent**: #0066ff (Blue)
- **Secondary Accent**: #ff0066 (Pink/Magenta)
- **Light Mode Text**: #333 (Dark Gray)
- **Dark Mode Text**: #e8e8e8 (Light Gray)
- **Dark Mode Background**: #1a1a1a (Almost Black)

To customize colors, find the CSS variable definitions near the top of the style block:

```css
:root {
    /* Update these color values */
    --primary: #0066ff;
    --primary-dark: #0052cc;
    --secondary: #ff0066;
    --text: #333;
    --bg: #ffffff;
}

body.dark-mode {
    /* Dark mode colors */
    --text: #e8e8e8;
    --bg: #1a1a1a;
}
```

### Gradient Effects

The design includes smooth gradients on:
- **Sidebar background** - Subtle gradient with transparency
- **Section icons** - Bold gradient backgrounds
- **Links and hover states** - Smooth transitions

To adjust gradients, search for `linear-gradient` in the CSS.

### Responsive Breakpoints

The resume is optimized for:
- **Desktop** (1024px+) - Full layout with two-column skills
- **Tablet** (768px - 1023px) - Adjusted padding and font sizes
- **Mobile** (< 768px) - Single-column layout, responsive typography

All changes are in the `@media` queries in the CSS.

## 📱 Responsive Design

The resume automatically adapts to different screen sizes:

- **Desktop (1024px+)**: Full layout with comfortable spacing, two-column skills section
- **Tablet (768px - 1023px)**: Adjusted padding, responsive typography
- **Mobile (< 768px)**: Single-column layout, optimized font sizes, full-width sections

The design uses CSS Grid and Flexbox for maximum flexibility. Test responsiveness by:
1. Opening `index.html` in your browser
2. Pressing `F12` to open Developer Tools
3. Clicking the device toolbar icon (Ctrl+Shift+M)
4. Selecting different device sizes

## 🔍 SEO & Optimization

To optimize your resume for search engines and applicant tracking systems:

### Meta Tags

Update the `<head>` section for better SEO:

```html
<title>Sriram — Your Title | Resume</title>
<meta name="description" content="Full-stack developer specializing in React, Node.js, and modern web technologies.">
<meta name="keywords" content="developer, full-stack, react, node.js, javascript">
```

### Tips for Better Visibility

1. **Use Semantic HTML** - The template uses proper heading hierarchy and semantic tags
2. **Include Keywords** - Add industry-relevant terms in your skills and summary
3. **Optimize for ATS** - Keep formatting simple (the single-file approach helps)
4. **Use Standard Fonts** - Stick with system fonts for better compatibility
5. **Clear Structure** - Use proper sections and bullet points for readability

## 📊 Print Optimization

The resume includes comprehensive CSS rules for printing with:

- **Color Preservation** - All colors, gradients, and styling are preserved in PDF
- **Theme-Aware Output** - Dark/light mode colors are applied to the PDF based on your current preference
- **Professional Formatting** - Proper spacing, page breaks, and card styling
- **Optimized Margins** - Standard printing margins for professional presentation

## 🔗 Deploy Your Resume

### GitHub Pages (Recommended)

Make your resume live on the internet in minutes:

1. **Ensure you're on the `main` branch**
   ```bash
   git branch
   ```

2. **Go to repository settings**
   - Click "Settings" in your GitHub repository
   - Scroll to "Pages" section

3. **Enable GitHub Pages**
   - Under "Source", select "Deploy from a branch"
   - Select `main` branch and `/(root)` folder
   - Click "Save"

4. **Access your resume**
   - Your resume will be available at: `https://sriram981998.github.io/Resume/`
   - Share this link with employers!

## 📄 Technical Details

### Architecture

- **Single File** - Everything (HTML, CSS, JavaScript) is in `index.html`
- **No Build Tools** - No webpack, npm, or compilation needed
- **No Server Required** - Runs entirely in the browser
- **CDN Dependencies** - Only external dependency is html2pdf.js from CDN

### File Structure

```
Resume/
├── index.html          # Main resume file (HTML + CSS + JS)
├── README.md          # Documentation (this file)
├── .gitignore         # Git ignore rules
└── .git/              # Git repository
```

### Technologies Used

- **HTML5** - Semantic markup with proper structure
- **CSS3** - Modern styling with CSS Grid, Flexbox, and CSS Variables
- **Vanilla JavaScript** - No frameworks, lightweight (~300 lines)
- **Google Fonts** - Professional typography (Merriweather, Inter)
- **Font Awesome 6** - High-quality icons


## � Contact & Social

- **Email**: srirampushpa1998@gmail.com
- **GitHub**: [@sriram981998](https://github.com/sriram981998)
- **LinkedIn**: [Your LinkedIn Profile](www.linkedin.com/in/sridhar-sriram-3a369718b)

## 📄 License

This resume template is free to use and modify for personal use.

---

## 🚀 Quick Commands Reference

```bash
# Clone the repository
git clone https://github.com/sriram981998/Resume.git
cd Resume

# Run local server (Python)
python -m http.server 8000

# Run local server (Node.js)
npx http-server

# Commit changes
git add .
git commit -m "Your message"
git push origin main

# Generate PDF with Puppeteer (if installed)
node generate-pdf.js
```

---

**Last Updated**: December 21, 2025

**Version**: 2.0 - Complete Interactive Resume with Advanced PDF Export
