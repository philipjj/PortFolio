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

- Replace the hero placeholder in `src/components/Hero.vue` with your actual image (use `<img src="/assets/your-image.png" alt="">`).
- This template uses `client:visible` on the Hero so animations run when visible. You can change hydration directives as needed for performance.
- To deploy to Vercel: push to GitHub and import the repo in Vercel. The project uses `astro build` by default.

Integration tips

- shadcn/ui is React-first; for Vue you can port the Tailwind patterns or use a Vue-native UI kit. This scaffold uses Tailwind utility patterns so you can apply shadcn-inspired styles.
- For advanced motion, combine `gsap` for timeline control and `@motionone/dom` for small interactive gestures.

CI / Deploy

- Add project to GitHub, and connect to Vercel. Vercel will detect the build step `npm run build` and output directory from Astro.
