# Aya's Personal Profile (Nuxt + Tailwind CSS)

Two-page personal profile website: Home (`/`) and Profile (`/profile`).

## Run it
```bash
npm install
npm run dev      # http://localhost:3000
```

## Structure
```
app/
  app.vue
  assets/css/main.css      Tailwind v4 + theme colors
  components/AppNav.vue    navigation menu
  components/AppFooter.vue
  layouts/default.vue      nav + page + footer
  pages/index.vue          homepage
  pages/profile.vue        profile page
public/aya.jpg             profile picture
nuxt.config.ts
```
