# 📄 Sriram - Full Stack Developer Resume

Welcome to my resume repository! A modern, single-file, responsive resume hosted on GitHub with an embedded PDF download feature.

## 🌟 Features

- ✨ **Modern Design** - Professional gradient header with clean typography
- 📱 **Fully Responsive** - Adapts perfectly to desktop, tablet, and mobile devices
- 📥 **One-Click PDF Export** - Download as PDF directly from the browser
- 🎨 **Single-File** - All HTML, CSS, and JavaScript in one file (no dependencies except html2pdf CDN)
- 🚀 **Fast Loading** - Lightweight and optimized for performance
- 🖨️ **Print-Optimized** - Perfect print styling to avoid blank pages
- 💼 **ATS-Friendly** - Clean semantic HTML for applicant tracking systems

## 📋 What's Inside

The resume includes the following sections:

- **Header** - Name, title, and contact information (email, phone, GitHub)
- **Professional Summary** - Brief overview of your experience and expertise
- **Experience** - Detailed job history with achievements and responsibilities
- **Skills** - Organized by categories (Frontend, Backend, Databases, DevOps)
- **Education** - Academic background and achievements
- **Certifications** - Professional credentials and certifications

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

### 3. Customize Colors

The design uses a purple gradient (`#667eea` to `#764ba2`). To change colors, find the `.header` style rule:

```css
.header {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

Replace with your preferred colors. Other key colors:

```css
:root {
    --accent: #0066ff;  /* Main accent color (blue links, buttons) */
    --text: #1a202c;    /* Body text color */
    --muted: #718096;   /* Secondary text color */
}
```

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

## 📥 PDF Download Options

### Method 1: Browser Button (Recommended)
- Click the **"📥 Download as PDF"** button on the resume
- PDF is generated client-side using html2pdf.js
- No file uploads or server required
- Works offline once the page loads

### Method 2: Browser Print Dialog
1. Press `Ctrl+P` (Windows) or `Cmd+P` (Mac)
2. Select "Save as PDF"
3. Choose your download location
4. Click "Save"

### Method 3: Headless Browser (Node.js)

For automated PDF generation, use Puppeteer:

```bash
npm install puppeteer
```

Create a `generate-pdf.js` file:

```javascript
const puppeteer = require('puppeteer');

(async () => {
  const browser = await puppeteer.launch();
  const page = await browser.newPage();
  await page.goto('file://' + __dirname + '/index.html', { waitUntil: 'networkidle2' });
  await page.pdf({ path: 'Sriram_Resume.pdf', format: 'A4' });
  await browser.close();
})();
```

Run it:

```bash
node generate-pdf.js
```

## 🎨 Design Customization Examples

### Color Schemes

#### Professional Blue
```css
.header {
    background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
}
:root {
    --accent: #0052cc;
}
```

#### Modern Dark
```css
.header {
    background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
}
:root {
    --accent: #ff6b6b;
}
```

#### Green Tech
```css
.header {
    background: linear-gradient(135deg, #0d3b66 0%, #06d6a0 100%);
}
:root {
    --accent: #06d6a0;
}
```

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

The resume includes special CSS rules for printing:

```css
@media print {
    body { background: white; }
    .resume { box-shadow: none; border-radius: 0; }
    .download-btn { display: none; }
    .footer { display: none; }
}
```

**Print Tips:**
- Margins are set to 12mm for standard printing
- The download button is hidden when printing
- No unnecessary shadows or decorations appear in print
- Professional, clean output suitable for job applications

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

### Other Hosting Options

- **Vercel** - Instant deployment: `vercel.com` (supports GitHub integration)
- **Netlify** - Drag & drop or GitHub: `netlify.com`
- **Personal Website** - Host on your own domain
- **Heroku** - Free tier available (no longer free as of 2024)

### Custom Domain

To use your own domain (e.g., `resume.yourname.com`):

1. Set up your domain DNS to point to GitHub Pages
2. Add a `CNAME` file to your repo with your domain
3. Enable "Enforce HTTPS" in settings

**For more details:** [GitHub Pages Documentation](https://docs.github.com/en/pages)

## 💡 Best Practices

### Resume Tips

1. **Keep It Concise** - One page is ideal; most recruiters spend < 6 seconds reviewing
2. **Use Metrics** - Quantify achievements: "improved performance by 40%" instead of "improved performance"
3. **Action Verbs** - Start bullet points with strong verbs: Led, Built, Designed, Implemented
4. **Tailor Content** - Customize for each job application; match keywords from job description
5. **Proofread** - Check for typos, grammar, and consistency
6. **Recent First** - List experience in reverse chronological order
7. **Keep It Updated** - Refresh regularly with new projects and skills

### Technical Optimization

- Test in multiple browsers (Chrome, Firefox, Safari, Edge)
- Test PDF download on different devices
- Verify print output looks professional
- Check mobile responsiveness
- Ensure all links work correctly
- Use semantic HTML for accessibility

### Git Best Practices

```bash
# Create feature branch for major changes
git checkout -b update/skills

# Commit with clear messages
git commit -m "Update skills section and add new certification"

# Keep history clean
git push origin update/skills

# Create pull request for review before merging
```

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

- **HTML5** - Semantic markup
- **CSS3** - Modern styling with Grid and Flexbox
- **Vanilla JavaScript** - No frameworks, lightweight
- **html2pdf.js** - Client-side PDF generation

### Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Android)

**Note:** PDF download requires JavaScript enabled in your browser.

## 🤝 Contributing

Found an improvement or bug? Feel free to fork this repository and submit a pull request!

### How to Contribute

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## � Contact & Social

- **Email**: email@example.com
- **GitHub**: [@sriram981998](https://github.com/sriram981998)
- **LinkedIn**: [Your LinkedIn Profile](https://linkedin.com/in/yourprofile)
- **Website**: [Your Personal Website](https://yourwebsite.com)

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

**Last Updated**: November 14, 2025

**Happy Job Hunting! 🎯**