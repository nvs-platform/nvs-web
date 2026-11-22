# Hravé reflexy – web projektu

Projektová stránka aplikace Hravé reflexy: projekt vznikající v rámci mentoringu
ReactGirls, na cestě ke startupu. Stránka je určená hlavně terapeutickým centrům,
odborníkům a sponzorům, na konci je výzva pro nové členy týmu a odkaz na prototyp pro Android.

Čistý statický web bez sestavování: `index.html`, `styles.css` a obrázky v `assets/`.

## Náhled

Otevřete `index.html` v prohlížeči, nebo spusťte jednoduchý server:

```bash
npx serve .
```

## Nasazení

- **GitHub Pages:** Settings → Pages → Deploy from a branch → `main`, složka `/ (root)`.
  U soukromého repozitáře vyžaduje GitHub Pages placený plán.
- **Netlify:** nový web z repozitáře, build command prázdný, publish directory `.`.

## Co ještě doplnit

- fotky týmu (zatím je jen fotka autorky)
- ověřit přesný název kurzu u paní Volemanové
- smyčku z aplikace a video z domácího cvičení (dítě zezadu)
- APK prototypu a QR kód na něj
- po nasazení doplnit plnou adresu do `og:image` v `index.html` (obrázek je v `assets/og-image.png`)
- doladit mobilní verzi

Plán a texty stránky vznikly v repozitáři aplikace (`docs/PROMO_PAGE_PLAN.md`,
`docs/PROMO_PAGE_TEXTS.md`).
