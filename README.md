# 📄 Resume - Sriram

Welcome to my resume repository! This is a modern, responsive resume hosted on GitHub and available as a downloadable PDF.

## 🌟 Features

- ✨ **Modern Design** - Clean, professional layout with gradient header
- 📱 **Fully Responsive** - Works perfectly on desktop, tablet, and mobile devices
- 📥 **PDF Download** - Download your resume as a PDF with one click
- 🎨 **Customizable** - Easy to modify colors, content, and styling
- 🚀 **Lightweight** - Fast loading with no external dependencies (except for PDF export)
- 💼 **Professional** - Perfect for job applications and portfolio websites

## 📋 Sections Included

- **Professional Summary** - Quick overview of your experience
- **Professional Experience** - Detailed job history with achievements
- **Skills** - Organized by categories (Frontend, Backend, Databases, DevOps, etc.)
- **Education** - Academic background and achievements
- **Projects** - Showcase your best work
- **Certifications** - Professional credentials

## 🚀 Getting Started

### Option 1: View Online
Simply open `index.html` in your web browser to view the resume online.

```bash
# If you have Python installed, you can run a local server
python -m http.server 8000
# Then visit http://localhost:8000 in your browser
```

### Option 2: Clone the Repository
```bash
git clone https://github.com/sriram981998/Resume.git
cd Resume
```

## 📝 Customizing Your Resume

### Edit Content
Open `index.html` and update the following sections:

1. **Personal Information**
   - Name: Change "SRIRAM" in the `<h1>` tag
   - Title: Update the professional title
   - Contact Info: Update email, phone, LinkedIn, and GitHub links

2. **Experience Section**
   - Modify job titles, company names, dates, and responsibilities
   - Add or remove jobs as needed

3. **Skills**
   - Update skill categories and technologies
   - Organize by your expertise areas

4. **Education**
   - Add your university, degree, graduation year, and achievements

5. **Projects**
   - List your notable projects with descriptions and tech stack

6. **Certifications**
   - Add your professional certifications

### Customize Styling
Edit `styles.css` to change:
- **Colors**: Modify the CSS variables at the top
- **Fonts**: Change font families
- **Spacing**: Adjust padding and margins
- **Layout**: Modify grid and flex properties

### CSS Variables
```css
:root {
    --primary-color: #2c3e50;      /* Main color */
    --secondary-color: #3498db;    /* Accent color */
    --accent-color: #e74c3c;       /* Highlight color */
    --text-color: #2c3e50;         /* Text color */
    --light-text: #7f8c8d;         /* Light text */
    --light-bg: #ecf0f1;           /* Light background */
}
```

## 📥 Download as PDF

### Method 1: Using HTML2PDF (Recommended)
1. The download button includes html2pdf library integration
2. Click the "📥 Download as PDF" button to save your resume

### Method 2: Browser Print Dialog
1. Press `Ctrl+P` (Windows) or `Cmd+P` (Mac)
2. Select "Save as PDF"
3. Choose your preferred settings
4. Click "Save"

### Method 3: Using Command Line (Node.js)
Install dependencies:
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

## 🎨 Color Schemes

You can easily switch between different color schemes by modifying the CSS variables:

### Professional Blue
```css
--primary-color: #2c3e50;
--secondary-color: #3498db;
```

### Modern Dark
```css
--primary-color: #1a1a1a;
--secondary-color: #ff6b6b;
```

### Tech Green
```css
--primary-color: #0d3b66;
--secondary-color: #06d6a0;
```

## 📱 Responsive Design

The resume is fully responsive and includes:
- **Desktop**: Full layout with optimal spacing
- **Tablet**: Optimized for medium screens
- **Mobile**: Stacked layout for small screens

## 🔍 SEO & Meta Tags

Update meta tags in the `<head>` section for better SEO:
- `<title>` - Your name and title
- Meta description
- Open Graph tags for social sharing

## 📊 Print Styles

The resume includes optimized print styles that:
- Hide unnecessary elements (buttons, footer)
- Optimize for PDF export
- Maintain professional appearance

## 🔗 Deploy Your Resume

### GitHub Pages
1. Enable GitHub Pages in repository settings
2. Choose main branch as source
3. Your resume will be available at `https://github.com/sriram981998/Resume`

### Other Hosting Options
- **Vercel**: Deploy with one click
- **Netlify**: Drop and deploy
- **Your own server**: Use any web hosting service

## 💡 Tips

1. **Keep it concise** - One page is ideal for most positions
2. **Use keywords** - Include relevant industry terms for ATS optimization
3. **Quantify achievements** - Use numbers and metrics where possible
4. **Regular updates** - Keep your resume current with latest projects and skills
5. **Test on multiple browsers** - Ensure consistency across Chrome, Firefox, Safari, Edge

## 📄 Template Information

- **Format**: HTML5 + CSS3 + JavaScript
- **Responsive**: Yes, mobile-friendly
- **Browser Support**: All modern browsers (Chrome, Firefox, Safari, Edge)
- **PDF Export**: Yes, multiple methods available
- **Customizable**: Fully editable HTML, CSS, and JavaScript

## 🤝 Contributing

Feel free to fork this repository and customize it for your own use!

## 📞 Contact

- 📧 Email: email@example.com
- 💼 LinkedIn: [Your LinkedIn](https://linkedin.com/in/yourprofile)
- 💻 GitHub: [Your GitHub](https://github.com/yourusername)

## 📄 License

This resume template is free to use and modify for personal purposes.

---

**Last Updated**: November 14, 2025

**Happy Job Hunting! 🚀**