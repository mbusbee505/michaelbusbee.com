# Quick Start Guide

## Step 1: Install Node.js

You need Node.js to run this project. Install it from:

**🔗 https://nodejs.org/**

Download the **LTS version** (Long Term Support) - currently v20 or v18.

### Verify Installation

After installing, open a new terminal and run:

```bash
node --version
npm --version
```

You should see version numbers for both.

---

## Step 2: Install Dependencies

Navigate to the project directory and install all dependencies:

```bash
cd /Users/mbusbee505/Documents/GitHub/michaelbusbee.com
npm install
```

This will download all required packages (~200MB total).

---

## Step 3: Start Development Server

```bash
npm run dev
```

The site will be available at: **http://localhost:4321**

You should see:
- 🏠 Homepage with cyberpunk design
- 📁 Sidebar with "Easy" → "Sample-Challenge"
- ⚡ Live reload when you make changes

---

## Step 4: Add Your Content

1. **Remove the sample:**
   ```bash
   rm -rf src/Lets-Defend/Easy/Sample-Challenge
   rm src/Lets-Defend/README.md
   ```

2. **Copy your Obsidian vault:**
   ```bash
   # Copy your Lets-Defend folders into src/Lets-Defend/
   # Example:
   cp -r ~/path/to/your/Lets-Defend/* src/Lets-Defend/
   ```

3. **Folder structure should look like:**
   ```
   src/Lets-Defend/
   ├── Easy/
   │   ├── Challenge1/
   │   │   ├── Challenge-1.md
   │   │   └── Attachments/
   │   └── Challenge2/
   │       └── Challenge-2.md
   └── Medium/
   ```

4. **Images in Markdown:**
   ```markdown
   ![Screenshot](./Attachments/screenshot.png)
   ```

---

## Step 5: Deploy to GitHub

### First Time Setup:

```bash
# Initialize git
git init
git add .
git commit -m "Initial commit: Astro blog portfolio"

# Create branch and push
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/michaelbusbee.com.git
git push -u origin main
```

### After First Push:

```bash
git add .
git commit -m "Add new writeups"
git push
```

### Enable GitHub Pages:

1. Go to your repo on GitHub
2. **Settings** → **Pages**
3. Source: **"GitHub Actions"**
4. Wait 2-3 minutes for deployment
5. Visit: `https://YOUR-USERNAME.github.io/michaelbusbee.com`

---

## Customization Tips

### Change Colors

Edit `tailwind.config.mjs`:

```javascript
colors: {
  'cyber-dark': '#YOUR-COLOR',
  'neon-pink': '#YOUR-COLOR',
  // ...
}
```

### Change Site Title

Edit `src/components/RecursiveSidebar.astro`:

```astro
<h1>YOUR NAME</h1>
```

And `src/pages/index.astro`:

```astro
<h1>YOUR-SITE.COM</h1>
```

### Disable Effects

Edit `src/styles/global.css`:

- Remove `body::before` (lines 17-30) to disable scanlines
- Remove `body::after` (lines 32-45) to disable grid
- Comment out `.glitch` styles to disable glitch effect

---

## Troubleshooting

### "npm: command not found"

👉 Install Node.js from nodejs.org and restart terminal

### Build errors

```bash
# Clear cache and reinstall
rm -rf node_modules package-lock.json
npm install
```

### Images not showing

- Ensure images are in `Attachments/` folder
- Use relative path: `./Attachments/image.png`
- Check file name matches exactly (case-sensitive)

### Port already in use

```bash
# Change port
npm run dev -- --port 3000
```

---

## Commands Reference

| Command | Description |
|---------|-------------|
| `npm install` | Install dependencies |
| `npm run dev` | Start dev server (http://localhost:4321) |
| `npm run build` | Build for production |
| `npm run preview` | Preview production build locally |
| `npm run astro -- --help` | See all Astro commands |

---

**🚀 Ready to build! Start with `npm install` after installing Node.js.**
