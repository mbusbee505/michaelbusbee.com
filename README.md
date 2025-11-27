# michaelbusbee.com

A cyberpunk-themed static blog portfolio built with Astro and Tailwind CSS, featuring automated deployment to GitHub Pages.

## 🚀 Prerequisites

Before you begin, ensure you have the following installed:
- **Node.js** (v18 or higher) - [Download here](https://nodejs.org/)
- **npm** (comes with Node.js)

## 📦 Installation

1. **Install Dependencies:**
   ```bash
   npm install
   ```

2. **Run Development Server:**
   ```bash
   npm run dev
   ```
   
   The site will be available at `http://localhost:4321`

3. **Build for Production:**
   ```bash
   npm run build
   ```

4. **Preview Production Build:**
   ```bash
   npm run preview
   ```

## 📁 Project Structure

```
michaelbusbee.com/
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Actions CI/CD pipeline
├── public/
│   └── favicon.svg             # Site favicon
├── src/
│   ├── components/
│   │   └── RecursiveSidebar.astro  # Dynamic navigation component
│   ├── layouts/
│   │   ├── BaseLayout.astro    # Base HTML structure
│   │   └── MainLayout.astro    # Main layout with sidebar
│   ├── pages/
│   │   ├── index.astro         # Homepage
│   │   └── [...slug].astro     # Dynamic page for all Markdown files
│   ├── styles/
│   │   └── global.css          # Global styles with cyberpunk effects
│   └── Lets-Defend/            # 📝 YOUR CONTENT GOES HERE
│       ├── Easy/
│       │   └── Sample-Challenge/
│       │       └── Sample-Challenge.md
│       └── Medium/
├── astro.config.mjs            # Astro configuration
├── tailwind.config.mjs         # Tailwind CSS configuration
├── tsconfig.json               # TypeScript configuration
└── package.json                # Project dependencies
```

## ✍️ Adding Your Content

### Content Structure

Place your Markdown files in `src/Lets-Defend/` following this pattern:

```
src/Lets-Defend/
├── Easy/
│   ├── Challenge1/
│   │   ├── Challenge-1.md
│   │   └── Attachments/
│   │       └── screenshot.png
│   └── Challenge2/
│       ├── Challenge-2.md
│       └── Attachments/
│           └── diagram.png
└── Medium/
    └── Challenge3/
        ├── Challenge-3.md
        └── Attachments/
```

### Image References

Reference images in your Markdown files using:

```markdown
![Screenshot description](./Attachments/screenshot.png)
```

The site will automatically resolve these paths during build.

### Example Markdown File

```markdown
# Challenge Title

## Overview

Description of the challenge...

## Tools Used

- Tool 1
- Tool 2

## Investigation Steps

1. First step
2. Second step

![Evidence Screenshot](./Attachments/evidence.png)

## Conclusion

Summary of findings...
```

## 🎨 Design Features

- **Cyberpunk Theme**: Dark mode with neon pink, cyan, and purple accents
- **CRT Effects**: Scanline overlay and grid background
- **Glitch Animations**: Hover effects on titles and navigation
- **Responsive Design**: Works on desktop, tablet, and mobile
- **Automatic Navigation**: Sidebar dynamically populates from folder structure

## 🚀 Deployment to GitHub Pages

### Initial Setup

1. **Create a GitHub repository** named `michaelbusbee.com` (or your preferred name)

2. **Configure GitHub Pages:**
   - Go to repository Settings → Pages
   - Set Source to "GitHub Actions"

3. **Push your code:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/michaelbusbee.com.git
   git push -u origin main
   ```

4. **Automatic Deployment:**
   - The GitHub Actions workflow will automatically build and deploy on every push to `main`
   - Check the Actions tab in your repository to monitor deployments

### Custom Domain (Optional)

If you have a custom domain:

1. Add a `CNAME` file in the `public/` directory:
   ```
   michaelbusbee.com
   ```

2. Configure DNS at your domain registrar:
   - Add an A record pointing to GitHub Pages IPs:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - Or add a CNAME record pointing to `YOUR-USERNAME.github.io`

3. In GitHub repository settings → Pages, enter your custom domain

## 🛠️ Customization

### Colors

Edit `tailwind.config.mjs` to customize the color palette:

```javascript
colors: {
  'cyber-dark': '#0a0a12',
  'neon-pink': '#ff00ff',
  'neon-cyan': '#00ffff',
  'electric-purple': '#a855f7',
}
```

### Fonts

Change fonts in `tailwind.config.mjs`:

```javascript
fontFamily: {
  mono: ['"Space Mono"', 'Courier', 'monospace'],
  sans: ['Your-Font', 'sans-serif'],
}
```

Update the Google Fonts import in `src/styles/global.css`.

### Effects

Modify or disable effects in `src/styles/global.css`:
- Remove `body::before` for no scanlines
- Remove `body::after` for no grid
- Adjust `.glitch` styles for different hover effects

## 📝 Development Tips

- **Hot Reload**: Changes auto-refresh in dev mode
- **Type Safety**: TypeScript is configured for better development experience
- **Markdown Syntax**: Supports GFM (GitHub Flavored Markdown)
- **Code Highlighting**: Automatic syntax highlighting with Dracula theme

## 🐛 Troubleshooting

### Images Not Loading

- Ensure images are in an `Attachments/` folder
- Use relative paths: `![alt](./Attachments/image.png)`
- Check file extensions match (case-sensitive)

### Build Errors

- Run `npm run build` to see detailed error messages
- Check all Markdown files have valid frontmatter
- Ensure no circular imports in components

### Navigation Not Updating

- Restart dev server after adding new folders
- Check folder/file names don't have special characters
- Ensure `.md` files are properly formatted

## 📄 License

MIT License - feel free to use this template for your own portfolio!

## 🙏 Credits

Built with:
- [Astro](https://astro.build/) - Static site generator
- [Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS framework
- [unified](https://unifiedjs.com/) - Markdown processing
- [Space Mono](https://fonts.google.com/specimen/Space+Mono) - Monospace font

---

**SYSTEM STATUS:** ✅ ONLINE | **SECURITY LEVEL:** 🔒 MAXIMUM | **THEME:** 🌆 CYBERPUNK
