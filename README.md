# Brendon Earl - Personal Website

A modern, fast personal CV/portfolio site built with **Astro** and **Tailwind CSS**.

## 🚀 Quick Start

```bash
# Install dependencies
npm install

# Start dev server (http://localhost:4321)
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## 📁 Project Structure

```
/
├── public/
│   ├── favicon.ico      # Add your favicon
│   └── resume.pdf       # Add your resume PDF here
├── src/
│   ├── components/      # Reusable Astro components
│   │   ├── Header.astro
│   │   ├── Hero.astro
│   │   ├── About.astro
│   │   ├── Skills.astro
│   │   ├── Experience.astro
│   │   ├── Contact.astro
│   │   └── Footer.astro
│   ├── layouts/
│   │   └── Layout.astro # Main HTML template
│   └── pages/
│       ├── index.astro  # Homepage
│       └── 404.astro    # 404 page
├── astro.config.mjs
├── tailwind.config.mjs
└── package.json
```

## 🌐 Deploy to Cloudflare Pages

### Option 1: GitHub Integration (Recommended)

1. **Push to GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/YOUR_USERNAME/brendon-site.git
   git push -u origin main
   ```

2. **Connect to Cloudflare Pages**
   - Go to [Cloudflare Dashboard](https://dash.cloudflare.com/) → Pages
   - Click **"Create a project"** → **"Connect to Git"**
   - Select your repository
   - Configure build settings:
     - **Framework preset:** Astro
     - **Build command:** `npm run build`
     - **Build output directory:** `dist`
   - Click **"Save and Deploy"**

3. **Add Custom Domain**
   - In your Pages project → **"Custom domains"**
   - Add `brendonearl.com`
   - Cloudflare will provide DNS records

4. **Update Squarespace DNS**
   - Log into Squarespace Domains
   - Point nameservers to Cloudflare:
     - `ada.ns.cloudflare.com` (or similar - Cloudflare will tell you)
     - `bob.ns.cloudflare.com`
   - Wait for propagation (up to 48 hours, usually much faster)

### Option 2: Direct Upload

1. Build locally: `npm run build`
2. Go to Cloudflare Pages → Create project → **"Upload assets"**
3. Drag the `dist/` folder

## ✏️ Customization

### Update Your Info

Most content lives in the component files under `src/components/`:

| File | What to edit |
|------|-------------|
| `Hero.astro` | Headline, tagline, social links |
| `About.astro` | Bio, highlights |
| `Skills.astro` | Technical skills & years of experience |
| `Experience.astro` | Work history |
| `Contact.astro` | Contact methods, availability status |
| `Header.astro` | Navigation links |
| `Footer.astro` | Footer content |

### Add Your Resume

Drop your PDF at `public/resume.pdf` - it will be available at `/resume.pdf`

### Change Colors

Edit `tailwind.config.mjs` to customize the color palette:
- `primary` - accent color (currently green)
- `surface` - background grays

## 🔧 Tech Stack

- **[Astro](https://astro.build)** - Fast static site framework
- **[Tailwind CSS](https://tailwindcss.com)** - Utility-first CSS
- **[Font Awesome](https://fontawesome.com)** - Icons

## 📝 Why Astro?

Coming from PHP, you'll find Astro familiar:
- `.astro` files are like enhanced PHP templates
- Components replace your PHP partials
- Zero JavaScript shipped by default = blazing fast
- Built-in Tailwind integration
- Perfect for static/content sites

## 🆚 Comparing to Your Old PHP Setup

| Old (PHP/Laravel) | New (Astro) |
|-------------------|-------------|
| `partials/header.php` | `components/Header.astro` |
| `require('view.php')` | `import Component from './Component.astro'` |
| `<?= $variable ?>` | `{variable}` |
| `foreach ($items as $item)` | `{items.map(item => ...)}` |
| Apache + PHP-FPM | Cloudflare CDN (edge) |
| EC2 $10+/month | Cloudflare Pages FREE |

## 📄 License

MIT - do whatever you want with it!

---

Built with ☕ by Brendon Earl
