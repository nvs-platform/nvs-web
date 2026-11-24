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

Web běží na GitHub Pages: https://nvs-platform.github.io/nvs-web/ (každý push do `main` se nasadí sám).
Při změně adresy upravte v `index.html` také `og:url` a `og:image`.

- **GitHub Pages:** Settings → Pages → Deploy from a branch → `main`, složka `/ (root)`.
  U soukromého repozitáře vyžaduje GitHub Pages placený plán.
- **Netlify:** nový web z repozitáře, build command prázdný, publish directory `.`.

## Jak se stránka chová

Pro další vývojáře: co je na stránce interaktivní a jak se mění podle šířky.

- **Šířky:** do 900 px se sloupce skládají pod sebe a menu se schová pod tlačítko
  (hamburger). Do 600 px platí mobilní stupnice písma a odsazení (viz níže).
  Úvodní obrázek se pod 375 px a 345 px ještě zmenšuje přes `zoom`.
- **Menu:** tlačítko `.menu-btn` přepíná třídu `.open` na hlavičce a `aria-expanded`.
  Zavře se kliknutím na odkaz nebo klávesou Esc.
- **Náš příběh:** na mobilu se ukážou jen první dva odstavce a tlačítko
  „Číst celý příběh“ zbytek rozbalí. Na počítači je příběh celý.
- **Co to přinese:** na mobilu přepínač Terapeutům / Rodinám (`role="tablist"`),
  na počítači jsou obě karty vedle sebe.
- **Časté otázky:** na mobilu rozbalovací `<details>`, na počítači otevřené.
- **Tmavý režim:** teď je vypnutý, web je vždy světlý (`data-theme="light"` na `<html>` a `<meta name="color-scheme" content="light">`).
  Tmavé barvy zůstávají připravené: stačí `data-theme="light"` smazat a web se zase řídí nastavením systému (`prefers-color-scheme`).
  V tmavém režimu se pak logo vymění za tmavou verzi z aplikace (`assets/logo-dark.webp`, z `nvs-app/assets/img/logo_dark.png`) a logo ReactGirls se invertuje.
- **Omezené animace:** respektuje `prefers-reduced-motion` (smyčka z aplikace se pak nespustí sama, dostane ovládání).
- **Smyčka z aplikace** (sekce Ukázky): `assets/app-loop.mp4` (540×960, bez zvuku, ~13 s) a náhled `assets/app-loop-poster.jpg`.
  Nahráno v Android emulátoru (`adb shell screenrecord`), sestříháno ve ffmpeg; tlačítko „dev“ v hlavičce je ve videu zakryté a kolečka klepnutí jsou dokreslená. Hraje, jen když je vidět (IntersectionObserver).

### Mobilní stupnice (do 600 px)

| Prvek | Velikost |
|---|---|
| Hlavní nadpis | 36 px |
| Nadpis sekce | 28 px, mezera pod ním 24 px |
| Nadpis bloku / položky | 20 px / 17 px |
| Úvodní text / text / popisky | 17 / 16 / 15 px |
| Okraj od kraje obrazovky | 20 px |
| Tlačítka a e-maily | výška 48 px |

Nové prvky prosím držte v této stupnici, ať stránka působí jednotně.

## Co ještě doplnit

- fotky mentorů (Veronika Čamborová, Jan Marek)
- text o Dominikovi je zástupný, autor si ho upraví
- ověřit přesný název kurzu u paní Volemanové
- video z domácího cvičení (dítě zezadu)
- APK prototypu a QR kód na něj

Plán a texty stránky vznikly v repozitáři aplikace (`docs/PROMO_PAGE_PLAN.md`,
`docs/PROMO_PAGE_TEXTS.md`).
