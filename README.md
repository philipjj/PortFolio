# Portfolio (Astro + Vue 3 + Tailwind)

This is a starter template for a portfolio site using Astro + Vue 3, Tailwind CSS, GSAP and Motion One for animations. It's arranged to match a visual direction like the image you made (hero with artwork, strong typographic heading, subtle motion).

Quick start

1. Install dependencies

```powershell
npm install
```

2. Run dev server

```powershell
npm run dev
```

3. Build for production

```powershell
npm run build
```

Notes

- Replace the hero placeholder in `src/components/Hero.vue` with your actual image (use the responsive files in `src/assets/`).

- Recommended: add optimized responsive variants (480, 768, 1200 widths) and WebP versions.

- Example `ImageMagick` command to generate responsive PNG/WebP variants locally:

```powershell
magick convert "your-image.png" -resize 480x -quality 80 src/assets/artwork-480.png
magick convert "your-image.png" -resize 768x -quality 80 src/assets/artwork-768.png
magick convert "your-image.png" -resize 1200x -quality 82 src/assets/artwork-1200.png
magick convert src/assets/artwork-480.png -quality 80 src/assets/artwork-480.webp
magick convert src/assets/artwork-768.png -quality 80 src/assets/artwork-768.webp
magick convert src/assets/artwork-1200.png -quality 82 src/assets/artwork-1200.webp
```

- The project currently includes placeholder SVG variants (`src/assets/artwork-480.svg`, `artwork-768.svg`, `artwork-1200.svg`) and an OG placeholder (`src/assets/og-image.svg`). Replace or overwrite these files with your exported images.
- This template uses `client:visible` on the Hero so animations run when visible. You can change hydration directives as needed for performance.
- To deploy to Vercel: push to GitHub and import the repo in Vercel. The project uses `astro build` by default.

Integration tips

- shadcn/ui is React-first; for Vue you can port the Tailwind patterns or use a Vue-native UI kit. This scaffold uses Tailwind utility patterns so you can apply shadcn-inspired styles.
- For advanced motion, combine `gsap` for timeline control and `@motionone/dom` for small interactive gestures.

CI / Deploy

- Add project to GitHub, and connect to Vercel. Vercel will detect the build step `npm run build` and output directory from Astro.
