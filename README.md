# mirlanium

Personal website. Astro, static, minimal.

## Setup

```bash
npm install
npm run dev       # localhost:4321
npm run build     # outputs to dist/
npm run preview   # preview the build
```

## Deploy

### Cloudflare Pages
1. Push to GitHub
2. Connect repo in Cloudflare Pages dashboard
3. Build command: `npm run build`
4. Output directory: `dist`
5. Point your domain via Cloudflare DNS

### Vercel
1. Push to GitHub
2. Import in Vercel dashboard
3. Framework preset: Astro (auto-detected)
4. Deploy

## Content

- **Blog posts**: Add `.md` files to `src/content/blog/` with frontmatter (`title`, `date`, `excerpt`)
- **Research/Experience**: Edit data arrays in `src/pages/research.astro` and `src/pages/experience.astro`
- **CV**: Drop your PDF in `public/cv.pdf`
- **Music**: Replace placeholder players in `src/pages/music.astro` with SoundCloud/Bandcamp embeds

## Structure

```
src/
  content/blog/     ← markdown blog posts
  components/       ← Nav, Footer, ThemeToggle
  layouts/          ← Base layout
  pages/            ← all routes
  styles/           ← global CSS
public/             ← static assets (favicon, CV, images)
```
